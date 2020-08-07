# Streaming Analytics docs

Use [Content design and development - Getting started](https://test.cloud.ibm.com/docs/writing) for guidance one writing docs for IBM cloud services.

## Branches
 
 - `draft` - When changes are committed or merged to this branch, IBM Cloud docs automatically rebuilds. Published results are usually available with 30 minutes at [IBM Cloud Docs / Streaming Analytics](https://test.cloud.ibm.com/docs/StreamingAnalytics)  (Test).
 - `production` After verifying changes in test, use a PR to merge from `draft` to `production`. IBM Cloud docs automatically rebuilds. Published results are usually available with 30 minutes at [IBM Cloud Docs / Streaming Analytics](https://cloud.ibm.com/docs/StreamingAnalytics) (Prod).
 
Docs search results might not be available until overnight after publishing.


## Deprecation

Guidance for [service deprecation](https://test.cloud.ibm.com/docs/writing?topic=writing-deprecating-a-service-s-documentation).

When the content can be fully pulled down:
- Go to [Documentation-content repo / issues](https://github.ibm.com/Bluemix/Documentation-content/issues)
- click New issue and use these two options:
    - **Build request: Remove an entire API docs repo**<br>_I want to remove an entire API doc repo and all associated builds_<br><br>
    - **Build Request: Remove a deprecated subcollection**<br>_I want to remove all content for a deprecated subcollection_<br><br>
  


## Migration of Streamsdev to IBM Cloud Docs

### Links to Streamsdev from Cloud Docs

The following links to Streamsdev from Cloud Docs need to be resolved

- [ ] c_getting_app_bluemix.md (2 matches)
  - [ ] https://developer.ibm.com/streamsdev/docs/streaming-analytics-dev-guide/
  - [x] https://developer.ibm.com/streamsdev/docs/getting-spl-application-ready-cloud
- [ ] c_ha.md
  - [x] https://developer.ibm.com/streamsdev/docs/streaming-analytics-dev-guide/#troubleshooting
- [ ] c_starterapps.md (3 matches)
  - [ ] https://developer.ibm.com/streamsdev/docs/starter-sample-apps-v2-plans/
  - [ ] https://developer.ibm.com/streamsdev/videos/getting-started-streaming-analytics-service-using-trades-starter-application/
  - [ ] https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/
- [ ] dev_guide.md (3 matches)
  - [ ] https://developer.ibm.com/streamsdev/docs/streams-quick-start-guide/
  - [ ] https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2019/09/SmackdownSource.zip
  - [ ] https://developer.ibm.com/streamsdev/docs/getting-spl-application-ready-cloud/
- [ ] faq.md (2 matches)
  - [ ] https://developer.ibm.com/streamsdev/docs/streaming-analytics-dev-guide/
  - [ ] https://developer.ibm.com/streamsdev/docs/roadmap-for-streaming-analytics-service-on-bluemix/
- [ ] index.md
  - [ ] https://developer.ibm.com/streamsdev/docs/getting-spl-application-ready-cloud/
- [ ] r_integrating_cloudant_rest.md (4 matches)
  - [ ] https://developer.ibm.com/streamsdev/docs/integrating-with-cloudant-and-many-other-restful-services/
  - [ ] https://developer.ibm.com/streamsdev/docs/spss-in-bluemix-streaming-analytics-service/
  - [ ] https://developer.ibm.com/streamsdev/docs/connect-streaming-analytics-to-your-enterprise/
  - [ ] https://developer.ibm.com/streamsdev/docs/integrating-streams-biginsights-hbase-service-bluemix/
- [ ] related_links.md (3 matches)
  - [ ] https://developer.ibm.com/streamsdev/docs/streaming-analytics-now-available-bluemix 
  - [ ] https://developer.ibm.com/streamsdev/docs/getting-spl-application-ready-cloud
  - [ ] https://developer.ibm.com/streamsdev/docs/streaming-analytics-dev-guide/
- [ ] spl_cloud_ready.md (2 matches)
  - [ ] https://developer.ibm.com/streamsdev/docs/connect-streaming-analytics-to-your-enterprise/
  - [ ] https://developer.ibm.com/streamsdev/docs/connecting-streaming-analytics-ibm-cloud
- [ ] StreamingAnalytics.md
  - [ ] https://developer.ibm.com/streamsdev/docs/streaming-analytics-now-available-bluemix-2/
 
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
