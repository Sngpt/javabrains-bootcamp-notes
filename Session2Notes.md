1) Learned about what is Dotcom bubble.
2) To become successful software engineer, one needs the Ability to apply technology, solve new problems, empathize with users or audience.
3) This bootcamp improves our ability to become  better backend developer.

1) What exactly meant by java backend engineer? 
Your customers are most often other developers(people who write front ends or other backends).
You are suppling api's. We write code which interfaces with others code.
2) Mostly deals with 3 tier architecture in java applications.
Frontend , Mid and data tier.

Currently most of the applications uses CDN in this way:
 Browser makes the request to CDN.(most of the web applications are rich client applications which are written mainly in javascript and have distinct separation from java side of things)
 u have a webpage loaded.Javascript makes the rest call to the server side.
3) As a backend developer we are goona building API Gateway and services.
4) CDN means Content Delivery Network.

1) What will happen when we type a address in webbrowser?
A: CDN are distributed servers that deliver web content to users based on their geographic location.
Eg: Aws has CDN servers called cloud front. There are other CDN servers called cloud flair.
CDN has two types of servers : Origin Server and Edge Server.

**A web Request:**
Browser sends a request to the DNS(domain name system) Server to resolve the domain name of the URL to its
corresponding IP address.
DNS is basically an aliasing system of domain names to ip address.
The DNS server returns the IP address of the closest CDN edge server to the user's location.
The browser sends the request to the CDN edge server.
The CDN edge server checks its cache.
If found in the cache, the CDN edge server returns the cached version.
If not found in the cache, the CDN edge server sends a request to the origin server.
The origin server returns the requested content to the CDN edge server.
The CDN edge server stores it in cache
The CDN edge server returns the content to the browser.


**A Web Page**

CDN contain ony static content like HTML page,CSS assests,Images, JS assets,Fonts.

To be continued.