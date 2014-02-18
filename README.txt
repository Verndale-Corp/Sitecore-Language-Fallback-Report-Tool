Verndale Language Fallback Report Tool for Sitecore

Purpose
Report on the content tree for what items are missing language versions, have explicit content, or having content falling back.

Compatibility
The codebase is compatible with Sitecore 6.6.x releases.  It should work with earlier versions though.
This assumes you are using the latest version of the Partial Language Fallback Module
http://marketplace.sitecore.net/en/Modules/Language_Fallback.aspx

How to build code and deploy the solution
1. When using the fallback module, make sure to compile the source code to get the dll, do not use the one within the package.

2. Download the App_Config folder, there are necessary updates within Sitecore.SharedSource.PartialLanguageFallback.config.example
You can use the whole thing or take the parts from it that you need and add to your fallback.config
It contains an important setting called Fallback.FieldToCheckForReporting which is where you can specify comma-delimited list of fields to use to check for explicit values

3. Download and install the Language Fallback Report Tool-1.zip Sitecore package
This will add an application to core and add a LanguageTools folder to /sitecore modules/web

4. The Verndale.SharedSource.zip class library is included only for your reference for other things you may see in the fallback.config. 
It is not necessary to run this tool

Testing
1. Open up the tool by either going directly to the url and opening via the Sitecore start button and choosing in the right menu column
2. Set a path to a content section of sitecore
3. run the report on different variations including Items with Language Version, Without Version, With Explicit Content, Without Content

Review the blog series about Partial Language Fallback on Sitecore, link TBD
