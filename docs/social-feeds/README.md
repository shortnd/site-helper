## Instagram Feed - Hack
```js
  			if($("#instagramfeed").length > 0){
			/**
			 * @param {string} cityName
			 * @param {number} count
			 * @returns {void}
			*/
			function getInstagramPhotos(cityName, count) {
				// MAX AMOUNT IS 12
				var INSTAGRAM_URL = "https://www.instagram.com/";
				$.get(INSTAGRAM_URL+cityName, function (data) {
					var $result = data;
          // console.log(data);
          // If you need to create a container create it here
					$('<div id="instagram"></div>').appendTo($('body'));
					var $el = document.getElementById('instagram');
					$el.innerHTML = $result;
          var $scripts = Array.from($el.querySelectorAll('script'))
          // $scripts.push($el.querySelectorAll('script'));
					// var $scripts = [ ...$el.querySelectorAll('script') ];
					// debugger;
					var data;
					$scripts.filter(function (el) {
						if (el.innerHTML.match(/window\._sharedData\s?=\s?{/, '{')) {
							data = el;
						}
					});
					var $_res = data.innerHTML.split(' = ', 2);
					$_res = $_res[1].replace(/;$/g, '');
					$_res = JSON.parse($_res)
					var $userPage = $_res.entry_data.ProfilePage[0]
					var userPhotos = $userPage.graphql.user.edge_owner_to_timeline_media.edges
					$el.innerHTML = "";
					for(var i = 0; i < count; i++) {
						$('<div class="social-feed-element"><a href="' + INSTAGRAM_URL + '/p/' + userPhotos[i].node.shortcode + '" target="_blank"><img src="' + userPhotos[i].node.display_url + '" alt="' + userPhotos[i].node.accessibility_caption + '" /></a></div>').appendTo($('#instagramfeed'));
					}
				});
			}
      // Replace name of city/url of city account
			getInstagramPhotos('cityoftempletx', 8);
		}
```
