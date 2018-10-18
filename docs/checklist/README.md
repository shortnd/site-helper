# Checklist

<checkbox/> Check which plugins that aren't in the design and remove them from the framework, scripts.js, layout.css, and the assets folder.

<checkbox/> Save all the images used in the PSD to the image folder. Make sure that photographs are saved as JPEGs. Make sure that graphics are saved as PNGs with a DPI of 144.

<checkbox/> Make sure the credentials section in the scripts.js and layout.css file is filled in. Check with me (Alec or Richard) if you don't know who designed the site.

## Styles

1. Styles for the homepage should go under the #main comment.

2. Styles for the interior pages should be under the #inner comment.

3. Styles for the slider and the elements inside the slider should be under the #bxslider comment.

4. Make sure you replace the touch-icons-xxx.png images inside the folder with the logo but keep the dimensions.

5. Select all ---'font-family: sans-serif'--- in the css and replace it with the one being used in the center area of the interior/inner page PSD. Same with the color, font-size, and line-height.

6. Make sure all @imports are at the very top part of the layout.css file.

7. Generate the favicon at [https://www.favicon-generator.org/](https://www.favicon-generator.org/)

## Check after finishing site

<checkbox/> Make sure all sections are lined-up on mobile. If the distance between the edge of the window to the sections is 15px, it should be the same for the rest.

<checkbox/> Make sure plugins not being used are deleted from the project and the mark-up.

<checkbox/> Make sure images not being used in the project are deleted.

<checkbox/> Check if there are styles for the mega-menu or the dropdowns. If not, always make sure the dropdown font-size is 1-2 pixels smaller without text-transform: uppercase and letter-spacing.

<checkbox/> Social feed templates should go inside a folder named templates inside the assets folder. Revize's clean-up tool gets rid of those templates for some reason. Files inside the assets folder won't get deleted by the clean-up tool.

<checkbox/> Make sure the skip to content button shows up when you first press on the tab key.

<checkbox/> The skip to content button should scroll the window to the first section inside the main tag.

<checkbox/> When you tab after pressing enter when the skip to content button is focused on, the first content in the main tag should be focused, not the next element after the skip to content button.

<checkbox/> Make sure the navigation is toggleable. If the website is using a mega-menu, only the first toggle button should show up on focus since the second-level dropdown links are visible by default.

<checkbox/> Use the .header and .subheader classes that are in the framework for the header and subheaders in the post.

<checkbox/> Use ternary statements for the items: in the reponsive option of owl carousels carousel.

<checkbox/> Make sure owl carousels have arrows on mobile.

<checkbox/> If the search is visible on desktop and when you toggle hidden the search on mobile, the search should be visible on desktop when you resize the screen.

<checkbox/> Make sure the all buttons on the website are styled. If there are no styles for buttons in the design, make sure it uses the same color scheme as the website.

<checkbox/> Make sure the revize link at the bottom of the website uses the new revize logo.

<checkbox/> If the website uses the weather plugin, make sure to update the zip code in the scripts.js file.

<checkbox/> The share button should be positioned absolutely lower right on mobile.

<checkbox/> Make sure the slider is proportionate to the window on mobile – not too tall, not too short.

<checkbox/> Remove the alert section and the add to homepage button in the freeform pages.

<checkbox/> Don't use img tags for banners. Use inline styles for banners.

<checkbox/> Use the aria-label or the class of sr-only for empty anchor tags and empty buttons.

<checkbox/> Make sure all alt tags in the mark-up are not empty.

<checkbox/> Fill in the credentials in the layout.css and scripts.js files.

<checkbox/> Replace the touch-icons-xxx.png images inside the images folder with the logo but keep the dimensions.

<checkbox/> Styles for the inner/freeform templates should go under the #inner comment in the layout.css file.

<checkbox/> Styles for the homepage should go under the #main comment in the layout.css file.