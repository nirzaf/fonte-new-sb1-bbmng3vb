# fonte-new-sb1-bbmng3vb

[Edit in StackBlitz next generation editor ⚡️](https://stackblitz.com/~/github.com/kamil467/fonte-new-sb1-bbmng3vb)
Location Maps:

Oman :

<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3653.7792392667748!2d58.176206675731095!3d23.68385147871581!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3e8de4cc6d0978f7%3A0x281c53712d20f98!2sBLUE%20BIRD%20TRAVELS%20-%20SEEB!5e0!3m2!1sen!2snl!4v1736248149981!5m2!1sen!2snl" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>

Kerala office :

Edapally , Kochin , Kerala

<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3928.925697226994!2d76.30401307531902!3d10.022990390083564!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3b080da8b1d0f263%3A0x409389047932793d!2sRobodigx!5e0!3m2!1sen!2sqa!4v1736274383560!5m2!1sen!2sqa" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>


#

### Deployment Guide:

Netlify : copy the netlify.toml file during every deployment from source directory to build directory.
The file handles the  server side redirects for single page application without  this file the redirect will not work.

### Issues fixed:
 - Scroll issue in react application:
    implement scroll to top component in react application. 

### Responisve Design Guide for HTML elements:
- top navigation bar  : left menu in mobile view
- grid view image in home page : carousel view in mobile view
- product details page : collapse and expandable tabs in mobile view


### Task To be done:
- [X] Mobile view - Product Details page - Tab Title style change   - Done : spacing required between tab title and tabs
- [X] Mobile view - Product Details page - Image and description spacing adjustment   - Done
- [X] Mobile view - Left Menu - Logo and menu width adjustment
- [X] website link title text and image (logo to be resized)  - Done
- [X] Supabase form integration  : form integration done - additional work( restore previous contents address and maps as it was replaced by AI agent) and make all the fields required. - Done
- [X] Live Chat integration.
- [X] Google Map updated to inline with design of silkwea website: - Done

### Logo Image Requirements:
Different size and with different color variations logo requried throughout the website.
A single logo image cannot meet all the requirements.
- Header logo 
- Footer logo
- website meta header logo - use png images 
- logo for mobile menu/view


### Color Requirements:
- Product Details List Tab BG : #f7f6f6

### Test Google Map Embed URL:

https://jsfiddle.net/591ks6c0/


Improved Data Flow in NavBar

Region Change → 
  Clear Categories/Subcategories →
    Fetch Region Mappings →
      Update Mapping States →
        Trigger useEffect →
          Fetch Categories and Subcategories →
            Update UI

----------------------
Cache Implementation:
- Use React Query for caching data
- Use React Query for caching data

currently disabled due to performance issues, enable for better performance and reduced data fetching. 10 mins cache time.

#

Header and Footer :
  - Pass data from header to footer.
  - When user changes the region on top , the footer should display the content specific to the region. (map, addressm, links, contact details)

 Maps:

  - Global : The map should display all regions.
       use follwoing iframe for global region
          <iframe src="https://www.google.com/maps/d/embed?mid=1jI4jyGGP315oqtd5wlcO0DZ5orD-j_s&ehbc=2E312F&noprof=1&&output=embed&iwloc=near&z=4" width="640" height="480"></iframe>
            To hide map user title and profile picture -   Identity the element css style class and apply display none 
  - Region:  map only display the selected region.
i4ewOd-pzNkMb-haAclf QUIbkc
#
region feature:
Implement the following features:
-  fetch the region code from url parameter if available and set the selected region accordingly.
code are global-en, uae-en, oman-en, india-en

- If region code available in url then fetch user location from browser.
- if their matches (india, Oma or UAE) then set selected region accordingly and update the URL and call the supbase function to fetch region mappings.
- If region code available in url but not matches (india, Oma or UAE) then set selected region to global and update the URL and call the supbase function to fetch region mappings.
-  deciding the region should be done before the component mounts.
- All urls in the website should have region code in the url.


class="fixed left-0 right-0 mt-2 bg-white border-y shadow-sm opacity-0 invisible group-hover:opacity-100 group-hover:visible transition-all duration-200 z-50"



