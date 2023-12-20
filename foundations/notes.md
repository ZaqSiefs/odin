# Notes for 'Foundations'

### Knowledge Check 1

> #### What is a web server?
>
>> A web server is a computer that is directly connected to the internet and contains all files needed for a website.
>
> #### What is a network?
>> A network is a group of computers connected to eachother via cables.
>
> #### What is the internet?
>> The internet is the global network.
>
> #### What is an IP address?
>> An IP address (Internet Protocol Address) is a unique set of 4 to 6 bytes that is assigned to a computer for internet communication.
>
> #### What is a Router?
>> A router is a computer with the sole purpose of routing packages to their proper destination (other computers on the network).
>
> #### What is an ISP?
>> An ISP (Internet Service Provider) is a company who acts as the intermediary between a local network and the internet.  They usually provide the router and/or modem to their clients, and have special routers at their own facilities connected to the internet.
>
> #### What are packets and how are they used to transfer data?
>> Packets are data that have been split into managable chunks to be more efficiently transferred over the internet.  They are reassembled by the requesting client in the proper order that they were sent in.
>
> #### What is a client?
>> A client is a computer that requests information from another computer (server) over a network.
>
> #### What is a server?
>> A server is a computer that sends information to another computer (client) over a network.
>
> #### What is a web page?
>> A web page is a single document (usually html) on the web that is interpretted and viewed by a browser.
>
> #### What is a web browser?
>> A web browser is a piece of software that can interpret webpages via HTTP requests/responses, and allows a user to browse data on the internet.
>
> #### What is a search engine?
>> A search engine is a website that allows users to search data on the internet with their browser.
>
> #### What is a DNS request?
>> A DNS (Domain Name System) request is a query to access the appropriate webpage that is located at the aliased IP address via a browser.
>
> #### Which browser are you currently using?
>> Chrome 120 (as of 12/20/23)
>
> #### Describe the process that takes place when you initiate a search on google in terms of what we discussed.
>> Essentially, after being connected to the internet via a router and my ISP, I have used my web browser to open up Google's 'search engine' website at their domain 'google.com' (an alias for whatever IP address they are using).  When I type in a request string and submit the form, an HTTP request is sent to the appropriate server, and it returns an HTTP response containing the results of my query.  These results are listed on an html webpage that my browser interprets, and contains many hyperlinks to additional websites that are hosted on different servers across the world.  There is far more nuance here, but this expresses the basic premise.

# HTML

## Elements and Tags
```<>``` = Opening tag

```</>``` = Closing tag
```html
<p> Paragraph Text </p>
```

### Knowledge Check 2
> #### What is an HTML Tag?
>> An HTML tag is essentially a wrapper that defines the start and end of HTML elements
>
> #### What are the 3 parts of an HTML element?
>> 1. Opening Tag ```<>```
>> 2. Content ```Usually Text```
>> 3. Closing Tag ```</>```

## HTML Boilerplate

### Files
```index.html``` = root file for all websites.  Browsers will look for this file first, so it is a **must include**

### Elements

#### External:

```<!DOCTYPE>``` = Tells the browser which version of HTML should be rendered

```<html></html>``` = root element of the document. All else descends from here

```<html lang="en">``` = the "lang" attribute denotes the language that this webpage's content is primarily in.

#### Header:

```<head></head>``` = where important meta-information about webpages live.  **Do Not** use for displaying content

```<meta charset="UTF-8">``` = encodes charset so that special symbols can be displayed

```<title></title>``` = gives the webpage a human-readable title displayed on the browser tab.

#### Body:

```<body></body>``` = Where all the content displayed to useres go. This is where a majority of the HTML elements will be located

### Knowledge Check 3
> #### What is the purpose of the doctype declaration?
>> The purpose is to tell the browser which version of html to render
>
> #### What is the HTML element?
>> The HTML element is the parent of all content inside of an HTML document.
>
> #### What is the purpose of the head element?
>> The purpose is to provide metadata about the web page for the browser
>
> #### What is the purpose of the body element?
>> The purpose is to display content to the browser.

## Useful Links
> [Introductory HTTP](https://launchschool.com/books/http/read/background)
>
> [API Documentation](https://devdocs.io/)
>
> [HTML Tags](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)



