## Instagram Feed - Hack

```js
if ($("#instagramfeed").length > 0) {
  /**
   * @param {string} cityName
   * @param {number} count
   * @returns {void}
   */
  function getInstagramPhotos(cityName, count) {
    // MAX AMOUNT IS 12
    var INSTAGRAM_URL = "https://www.instagram.com/";
    $.get(INSTAGRAM_URL + cityName, function(data) {
      var $result = data;
      // console.log(data);
      // If you need to create a container create it here
      $('<div id="instagram"></div>').appendTo($("body"));
      var $el = document.getElementById("instagram");
      $el.innerHTML = $result;
      var $scripts = Array.prototype.slice.call($el.querySelectorAll("script"));
      // $scripts.push($el.querySelectorAll('script'));
      // var $scripts = [ ...$el.querySelectorAll('script') ];
      // debugger;
      var data;
      $scripts.filter(function(el) {
        if (el.innerHTML.match(/window\._sharedData\s?=\s?{/, "{")) {
          data = el;
        }
      });
      var $_res = data.innerHTML.split(" = ", 2);
      $_res = $_res[1].replace(/;$/g, "");
      $_res = JSON.parse($_res);
      var $userPage = $_res.entry_data.ProfilePage[0];
      var userPhotos =
        $userPage.graphql.user.edge_owner_to_timeline_media.edges;
      $el.innerHTML = "";
      for (var i = 0; i < count; i++) {
        $(
          '<div class="social-feed-element"><a href="' +
            INSTAGRAM_URL +
            "/p/" +
            userPhotos[i].node.shortcode +
            '" target="_blank"><img src="' +
            userPhotos[i].node.display_url +
            '" alt="' +
            userPhotos[i].node.accessibility_caption +
            '" /></a></div>'
        ).appendTo($("#instagramfeed"));
      }
    });
  }
  // Replace name of city/url of city account
  getInstagramPhotos("cityoftempletx", 8);
}
```

## Youtube Feed

```js
/**
 * @param {string} channelId
 * @param {string} ytAPIToken
 * @param {number} resultLimit
 * @param {function} cb
 *
 * to get data from response use JSON.parse(this.responseText)
 */
function get_youtube_feed(channelId, ytAPIToken, resultLimit, cb) {
  if (!channelId) {
    return new Error("Channel ID is missing for youtube feed!");
  }
  if (!ytAPIToken) {
    return new Error("Provide a youtube api token");
  }
  if (!resultLimit) {
    return new Error("Please provide a result limit");
  }
  if (typeof cb !== "function") {
    return new Error("Please provide a valid callback function");
  }
  var request = new XMLHttpRequest();
  var youtube_api_base_url =
    "https://www.googleapis.com/youtube/v3/search?order=date&part=snippet";
  var channel = "&channelId=" + channelId;
  var maxResults = "&maxResults=" + resultLimit;
  var yt_key = "&key=" + ytAPIToken;
  var request_url = youtube_api_base_url + channel + maxResults + yt_key;
  request.addEventListener("loadend", cb);
  request.open("GET", request_url);
  request.send();
}

if ($(".youtube-feed").length) {
  get_youtube_feed("channelId", "youtubeAPIToken", 10, function() {
    // Gets the response back...
    var json = JSON.parse(this.responseText);
    // All items in the response.. (aka Videos)
    var items = json.items;
    if (!items) {
      console.log(JSON.stringify(this.responseText));
      return new Error("Something happened");
    }
    for (var i = 0; i < items.length; i++) {
      var item = items[i];
      var itemStartDate = new Date(item.snippet.publishedAt);
      var itemMonth = itemStartDate.getUTCMonth() + 1;
      if (itemMonth > 12) {
        itemMonth = 12;
      }
      var itemDay = itemStartDate.getUTCDay();
      var itemYear = itemStartDate.getUTCFullYear();
      var itemPublishedDate = itemMonth + "/" + itemDay + "/" + itemYear;
      var itemElement = `
			<div class="social-feed-element">
				<div class="fb-feed-header">
					<i class="fa fa-youtube" aria-hidden="true"></i>
					<span class="author-title">${item.snippet.channelTitle}</span>
					<span class="text-muted">${itemPublishedDate}</span>
				</div>
				<div class="content">
				  <div class="media-body">
				  	<div class="text-wrapper">
					  <iframe style="width:100%;height:250px" width="" height="" src="https://youtube.com/embed/${item.id.videoId}" frameborder="0" allowfullscreen></iframe>
					</div>
				  </div>
				</div>
			</div>
		`;
      $(itemElement).appendTo($(".youtube-feed"));
    }
  });
}
```
