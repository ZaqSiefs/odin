# Knowledge Checks

## Internet

> ### What is a web server?
>
>> A web server is a computer that is directly connected to the internet and contains all files needed for a website.
>
> ### What is a network?
>> A network is a group of computers connected to eachother via cables.
>
> ### What is the internet?
>> The internet is the global network.
>
> ### What is an IP address?
>> An IP address (Internet Protocol Address) is a unique set of 4 to 6 bytes that is assigned to a computer for internet communication.
>
> ### What is a Router?
>> A router is a computer with the sole purpose of routing packages to their proper destination (other computers on the network).
>
> ### What is an ISP?
>> An ISP (Internet Service Provider) is a company who acts as the intermediary between a local network and the internet.  They usually provide the router and/or modem to their clients, and have special routers at their own facilities connected to the internet.
>
> ### What are packets and how are they used to transfer data?
>> Packets are data that have been split into managable chunks to be more efficiently transferred over the internet.  They are reassembled by the requesting client in the proper order that they were sent in.
>
> ### What is a client?
>> A client is a computer that requests information from another computer (server) over a network.
>
> ### What is a server?
>> A server is a computer that sends information to another computer (client) over a network.
>
> ### What is a web page?
>> A web page is a single document (usually html) on the web that is interpretted and viewed by a browser.
>
> ### What is a web browser?
>> A web browser is a piece of software that can interpret webpages via HTTP requests/responses, and allows a user to browse data on the internet.
>
> ### What is a search engine?
>> A search engine is a website that allows users to search data on the internet with their browser.
>
> ### What is a DNS request?
>> A DNS (Domain Name System) request is a query to access the appropriate webpage that is located at the aliased IP address via a browser.
>
> ### Which browser are you currently using?
>> Chrome 120 (as of 12/20/23)
>
> ### Describe the process that takes place when you initiate a search on google in terms of what we discussed.
>> Essentially, after being connected to the internet via a router and my ISP, I have used my web browser to open up Google's 'search engine' website at their domain 'google.com' (an alias for whatever IP address they are using).  When I type in a request string and submit the form, an HTTP request is sent to the appropriate server, and it returns an HTTP response containing the results of my query.  These results are listed on an html webpage that my browser interprets, and contains many hyperlinks to additional websites that are hosted on different servers across the world.  There is far more nuance here, but this expresses the basic premise.

## Elements and Tags
> ### What is an HTML Tag?
>> An HTML tag is essentially a wrapper that defines the start and end of HTML elements
>
> ### What are the 3 parts of an HTML element?
>> 1. Opening Tag ```<>```
>> 2. Content ```Usually Text```
>> 3. Closing Tag ```</>```

## Boilerplate
> ### What is the purpose of the doctype declaration?
>> The purpose is to tell the browser which version of html to render
>
> ### What is the HTML element?
>> The HTML element is the parent of all content inside of an HTML document.
>
> ### What is the purpose of the head element?
>> The purpose is to provide metadata about the web page for the browser
>
> ### What is the purpose of the body element?
>> The purpose is to display content to the browser.

## Text Elements
> ### How do you create a paragraph in HTML?
>> Use the ```<p></p>``` tags in the ```<body>``` element
>
> ### How do yu create a heading in HTML?
>> Use the ```<h(1-6)></h(1-6)>``` tags in the ```<body>``` element
>
> ### How many different levels of headings are there and what is the difference between them?
>> 6...  They are ordered by importance from 1 to 6, getting less big and bold as the numbers ascend.
>
> ### What element should you use to make the text bold and important?
>> ```<strong></strong> or <b></b>```
>
> ### What element should you use to make the text italicized to add emphasis to it?
>> ```<em></em> or <i></i>```
>
> ### What relationship does an element have with any nested elements within it?
>> Parent relationship
>
> ### What relationship do two elements have if they are of the same level of nesting?
>> Sibling
>
> ### How do you create HTML comments?
>> ```<!-- txt -->```

## Lists
> ### What HTML element is used to create an unordered list?
>> ```<ul></ul>```
>
> ### What HTMl element is used to create an ordered list?
>> ```<ol></ol>```
>
> ### What HTML element is used to create list items within both unordered and ordered lists?
>> ```<li></li>```

## Links and Images

> ### What element is used to create a link?
>> ```<a></a>```
>
> ### What is an attribute?
>> An attribute is a tag's variable that we can set 
>
> ### What attribute tells links where to go?
>> ```target```
>
> ### What security considerations must be taken if using ```_blank``` with ```target```?
>> use the ```ref``` attribute and pass "noopener noreferrer" to protect the website from bad actors.
>
> ### What is the difference between an absolute and relative link?
>> - Absolute links point directly to a page or file using the protocol (http).
>> - Relative links point to a page or file in relation to the current directory.
>
> ### Which element is used to display an image?
>> ```<img>```
>
> ### What two attributes do images always need to have?
>> ```src``` and ```alt```
>
> ### How do you access a parent directory in a filepath?
>> ```../```
>
> ### What are the four main image formats that you can use for images on the web?
>> .png, .jpg, .gif, .svg

## Intro to CSS

> ### What is the syntax for class and ID selectors>
>> ```class``` = ```.(class_name)```
>>
>> ```id``` = ```#(ID_name)```
>
> ### How would you apply a single rule to two different selectors?
>
>> Basic combining
>>
>> ```css
>> .one,
>> .two {
>> color: black;
>>}
>> ```
>> chaining
>>
>>```css
>> .one.two{
>> color: black;
>>}
>>```
>> or descendant combinator
>>```css
>>.one .two{
>> color: black
>>}
>>```
>
> ### Given an element that has an id of #title and a class of .primary, how would you use both attributes for a single rule?
>
>> chaining
>
> ### What does the descendant combinator do?
>
>> The descendant combinator selects only the elements with the given parent structure.
>
> ### What are the names of the three ways to add CSS to HTML?
>
>> External, Internal, Inline
>
>> ### What are the differences?
>
>> ```External``` is when a separate CSS file is used for stylingk, and is then linked using the ```<link>``` element inside of the html ```<head>``` element.
>>
>> ```Internal``` is when CSS styling is used inside of a ```<style>``` element in the html ```<head>``` element
>>
>> ```Inline``` is when CSS styling is used inside of the ```style=""``` attribute of any display element.