# Streaming Analytics docs


## Migration of Streamsdev to IBM Cloud Docs

There is no easy path to migrate articles from the Streamsdev Wordpress site
to IBM Cloud docs markdown. A brute force approach:
- View article in Streamsdev in Chrome
- `File -> Save page As...` choosing format `Webpage, Complete`
    This will download the html and all linked images
- Open the downloaded html in an editor and copy the html source for the body of the article, ignoring all the header and footer html.
- Paste html into a new markdown article in this repo
- Edit to convert as much of the html to markdown as possible / reasonable
    Use IBM Cloud docs tags as appropriate.
- Paste IBM Cloud docs boilerplate frontmatter at top of new markdown article 

### Eclipse Find and Replace

Eclipse has a powerful find / replace function that can use regular expressions including capturing groups that can be references in the replacement string.

##### Converting Header html tags to markdown                       
- Find regex: `<h3 id="(.*)">(.*)</h3>`
- Replace regex: `\n### $2\n{: #$1}`                                                    

Changes this:

```
    &lt;h3 id="heading3-id">Heading3 Text</h3>
```

to:

    
```
    ### Heading3 Text                                                                   
    {: #heading3-id}
```

##### Converting List Items 

Assumes entire list item is on a single line   

- Find regex: `<li>(.*)</li>`                                                           
- Replace regex for ordered lists: `1. $1`                                              
- Replace regex for unordered lists: `- $1`                                               


##### Converting image html tags to image markdown. 

Assumes specific formatting of img html tag )

- Find regex: `<img src="(.*)" alt="(.*)" width=".*" height=".*">`
- Replace regex: `\n![$2]($1)\n`
