# AJAX GOTCHAS #

### visual cues ###
* starting 
* ending
* error 
* correct response

#### deep links ####
* bookmarks
* urls
* back button
* seo crawling

#### backwards compatibility ####
* might not work with older browsers
* browser which have js disabled

#### third party access ####
* by default ajax requests are only allowed within the same domain
* create action which returns json/xml to the ajax request

#### user data ####
* never use ajax to handle sensitive data submission
* better if limited to get requests
* batch operations

#### security issues ####
* cross-site scripting
* cross-site request forgery

#### ajax objects ####
* too much makes the browser slow
* remove ajax objects that are with completed requests
* instantiate new objects per request. some browsers do not allow the reuse of ajax objects


##### References:
https://www.owasp.org/images/3/35/Development_Issues_Within_AJAX_Apps-Lars_Ewe.pdf
http://www.webdesignerdepot.com/2009/12/solutions-to-5-common-ajax-problems/
http://coding.smashingmagazine.com/2010/02/10/some-things-you-should-know-about-ajax
https://alexbosworth.backpackit.com/pub/67688
