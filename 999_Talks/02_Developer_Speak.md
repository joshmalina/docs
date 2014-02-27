{ "isolate" : "true" }

## Intro

* Susan Buck susan@thewc.co
* Women's Coding Collective <http://thewc.co>
* URL For these notes: <http://thewc.co/s/venturecafe2014>

>> &ldquo; The spread of computers and the Internet will put jobs in two categories, people who tell computers what to do, and people who are told by computers what to do.&rdquo; - Marc Anderson (Created Netscape in 1994, quote from 2012) [source](http://ideas.time.com/2014/02/24/how-i-quit-google/?xid=gonewsedit)


## Expectations

### What this talk is not:
* How to find a good web developer
* The ins/outs of contracts, scope of work, etc.
* The politics of bad developers / bad clients

### What this talk is:
* Learning how we can better speak the same language
* Insight into the mind of a developer


## Complexity

Seemingly simple tasks are not always simple.

Example Task: *&ldquo;We need a page where users can log on to our site&hellip;&rdquo;*

What might this entail?




## Prioritization



Don't cry wolf.


## Which do you need?

Web site vs. web applications.

Roles: 

* Copywriter
* Designer
	
	* Graphic designer
	* Interactive designer
	* Illustrator
	
* Developer



## Platforms

Where I test:

* Mac: Latest Chrome, FireFox and Safari
* PC: IE9, Chrome, Firefox
* Mobile: iPhone
* What other platforms do you need your site to function well on?

Weigh the cost of backwards compatibility.

Look at [general statistics ala StatCounter](http://gs.statcounter.com/) and also statistics relative to your site ala Google Analytics.

Read [37 Signals: Developing for old browsers is (almost) a thing of the past](https://signalvnoise.com/posts/3097-developing-for-old-browsers-is-almost-a-thing-of-the-past).





## Problems

Programming is problem solving.

Software can be a living, breathing thing.

**Reporting issues:**

* Give as many details as possible.
* Don't spend too much time diagnosing, focus on the symptoms.
* [SupportDetails](http://supportdetails.com)
* [Jing: Free, quick, screencasts](http://www.techsmith.com/jing.html)



## Feedback

[The theory of the hairy arm: the tactical benefits of making deliberate mistakes](http://www.oliverburkeman.com/blog/posts/the-theory-of-the-hairy-arm-the-tactical-benefits-of-making-deliberate-mistakes)


## Lingo
* Front-end vs. Back-end
* PHP, Ruby
* SEO 
* Copy
* Version Control
* CMS (Content Management Systems)
* WordPress, Drupal, Joomla
* Responsive Design
* Mobile design
* HTML5 / HTML
* Database
* Framework
* Hardcoded / static
* https/ssl



## Readings

* http://zeek.com/how-to-speak-geek-part-1-interviewing-your-potential-developer/
* http://eternitywebdev.com/pdfs/10-ways-eternity.pdf
* http://informationhighwayman.com/reports/how-to-actually-choose-a-web-designer.pdf





## Sign-up solution

Land on sign-up page

* What to do if they're already logged in
* Make sure it correctly detects user's timezone
* Don't allow duplicate emails
* Verify email is correct
* Make sure minimum password requirements are met

Post sign-up

* Sends you back to the login page, telling you to check your inbox for a verification link
* Receive confirmation email
* Click verification link, and then confirm new login works

	* If they enter a bad email
	* If they enter a bad password
	* If they click Password Reset

Password reset page

* Email not found
* Email is found

	* Sends them an email with reset instructions and link
	* Clicking reset link in email takes them to page where they can reset their password
	* Confirm password meets minimum requires
	* Upon resetting password, send

