# Introduction
This is an attempt at an open standard. I've only ever read the Gneutella standard and that was a long time ago. Forgive me for any confusion this may cause while I brush up on how to write official standards. This will be a living-standard (like HTML5).

# JSON
JSON is a key-value data storage file format. In this document "key" refers to a javascript pointer and "value" refers to the value javascript would spit out if said pointer were called. Padding is optional for this specification.

# Initial Keys
Each JSON entry needs a unique identifier. As this is a news syndication protocol, said identifier should be a URL link to the article in question. Protocol specifications (https://, ftp://) are optional.

```
{
  "http://example.com/article/5014":{}
}
```

## Sub-keys
Here's where we get into the nitty-gritty. The following sub-keys (and their explanations) are standard in JOSS. All keys should be in lower-case and all readers should be case-agnostic (for the programmers who don't read this).

### title
The article title you'd like to seen by the reader.

### desc
A text description of the article. This is the text preview shown in feed readers.

### img
URL to image you want to appear in the reader.

### author
Article author's name.

```
{
  "https://example.com/article/5014": {
    "title": "This is An Example Article",
    "desc": "It is great to have example articles on the Internet to show off in potential usage cases. Studies have shown that examples provide people with much better understanding than straight communications. Click the Title to learn more.",
    "img": "https://example.com/402.jpg",
    "author": "Sarah Silverman"
    }
}
```

## Header (Optional)
You may include a header key in your JSON which describes your site and content. Its keys are as follows:

### title
Site title

### url
Site URL

### desc
Site description

### icon
Site icon

# Full Example
```
{
  "header":{
    "title":"Eample.com: The example site of the Internet",
    "url":"https://example.com",
    "desc":"The example site of the Internet",
    "icon":"https://example.com/favicon.ico"
  },
  "https://example.com/article/5014": {
    "title": "This is An Example Article",
    "desc": "It is great to have example articles on the Internet to show off in potential usage cases. Studies have shown that examples provide people with much better understanding than straight communications. Click the Title to learn more.",
    "img": "https://example.com/402.jpg",
    "author": "Sarah Silverman"
    }
}
```

# Licensing
![BY-SA Logo](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)  
This work is licensed under a  
[Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).
