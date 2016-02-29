#XML

++XML (eXtensible Markup Language)++. The strength of XML is that you can extend it. XML is the foundation of many Web technologies such as XHTML, AJAX and many other APIs.

XML has a **tag-based syntax** similar to HTML.

##What is XML Used For?

XML's purpose is to take **information and add structure to it**. XML was designed to be used over the internet. XML can enable communication between different systems, that may have never been possible before.



##Describing Things in XML



```XML
<Student>
	<name>Regan Koopmans</name>
    <studentNumber>15043143</studentNumber>
    <degree year="2">Computer Science</degree>
</Student>
```

###"Valid" XML

An XML document is said to be _well formed_ if it conforms to general rules and basic syntactical rules

But we can set custom rules in addition to standard parsing, to set logical rules for how we want to restrict the data. This can be done in two ways:

- DTD - Document type definitions
	> Simple but not powerful. Written in external language.
- XML Schema
	> Written in XML and more flexible and powerful.

###Advantages of XML

- Content is **separate from presentation.**
- An open format &rarr; can work towards a standard.
- Used on client and server
- Widely supported
- Disparate systems can communicate.

###Disadvantages of XML

- Not suitable for large amounts of data, cannot replace database.
- Lightweight data may be more appropriate for JSON
- Images cannot be represented easily.
- Becomes hard to read quickly.