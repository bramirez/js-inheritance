# AJAX GOTCHAS #

### Visual Cues ###
* Starting a request
* Use a loading cue to signify that the request is being processed
* Display error messages

#### Deep Linking ####
* Direct Links might not work if the site is too dependent on ajax requests
* No history
* Site crawlers may not work as intended

#### Backwards Compatibility ####
* Might not work with older browsers
* Consider users that may have javascript disabled

#### Third Party Data ####
* By default ajax requests are only allowed within the same domain
* Create server actions which return json/xml response to the ajax request

#### Data Handling ####
* As much as possible, never use ajax to handle form submission with a lot of data.
* Better if ajax requests are limited to GET requests
* Prefer batch operations over a lot of repetetive small actions

#### Security Issues ####
* Cross-site scripting
* Cross-site request forgery

#### ajax objects ####
* Too much is not always best. It may become less interactive and more unresponsive
* Instantiate new objects per request. Some browsers do not allow the reuse of ajax objects



##### References:
https://www.owasp.org/images/3/35/Development_Issues_Within_AJAX_Apps-Lars_Ewe.pdf
http://www.webdesignerdepot.com/2009/12/solutions-to-5-common-ajax-problems/
http://coding.smashingmagazine.com/2010/02/10/some-things-you-should-know-about-ajax
https://alexbosworth.backpackit.com/pub/67688
