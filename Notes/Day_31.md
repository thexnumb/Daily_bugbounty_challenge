1. **Review + Learning**
	1. what we do yesterday?
	2. Learning About the Google(or any search engine) Dorking
		1. Alongside of the usage of the search engines for find docs or anything in the research process, we can also use the Advance search for doing Recon
		2. Dorking may leads us to vulnerable information like:
			1. hidden admin portals
			2. unlocked password files
			3. leaked authentication keys
			4. ...
		3. useful operators
			1. `site`
				1. show the results of a certain site only
			2. `inurl`
				1. search for pages with a URL that match the search string
			3. `intitle`
				1. find specific strings in a page's title that allow us to find pages that contains a particular type of content
			4. `link`
				1. searching for web pages that contain links to a specified URL
			5. `filetype`
				1. searches for pages with a specific file extensions
			6. `Wildcard (*)`
				1. in search means 'any character or series of characters'
			7. `Quotes (" ")`
				1. forced to search on exact match
			8. `Or (|)`
				1. use to search for one term or the other or both
			9. `Minus (-)`
				1. exclude certain search result
		4. some useful dorks
			1. `site:*.site.com` -> look for all of a company's subdomains
			2. `site:site.com inurl:route/to/interesting/endpoint` ->look for special endpoints that can leads to vulnerability
			3. `site:s3.amazonaws.com COMPANY_NAME` -> look for company resources that is host on a third-party application like Amazon S3 buckets
			4. `site:site.com ext:php`, `site:site.com ext:log` -> look for special extensions that may leads to a sensitive file
			5. `site:site.com ext:txt password` -> combines search term like looking for `txt` files that contain password
		5. Resource
			1. [Google Hacking Database](https://www.exploit-db.com/google-hacking-database)
2. **Hunting**
	1. 
