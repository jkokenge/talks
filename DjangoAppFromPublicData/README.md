**PREMISE**

After I've worked a basic tutorial or two, I often struggle with my next steps with a new framework.  I'm not yet ready for a large, enterprise type application. I still need more practice, but tutorials are often boring, ToDo apps, blogs, a useless demo app, those are no fun. 

**Solution: Public Data!**

Public data is everywhere.  It's about everything. (You can surely find a dataset that piques your interest.)  Working with a dataset that's prebuilt and, essentially, unchanging also lets you focus on specific components of a framework.  In the case of Django, using public data as a starter lets you focus on templates, views, models and basic URL routing (the fundamental basics) while leaving other topics for later.

Also, building an application isn't just about messing around with it's components.  Applications are made to be deployed!  Finding a public dataset that interests you, that's valuable to your community, will give you the motivation to push through to complete deployment of your Django application.  

**History**

2003-2004 Django was built by developers at the Lawrence Journal-World

The first public facing application not associated with the Lawrence Journal-World was the now defunct (RIP) chicagocrime.org built by Django co-founder Adrian Holovaty and launched in May 2005.  The initial public release of Django as a framework followed shortly thereafter in July of 2005.

Ten years later, a list of companies that use Django reads like a Who's Who of the Internet.  Despite that success, many news organizations still use Django to serve public data.

**Examples** 

The common theme running through all public data serving Django applications, from chicagocrime.org through to the present day, is that they essentially digest the raw public data and make it easier for mass consumption.  We'll see this theme again and again as we look at examples of Django applications that serve public data.  The applications will all look different, but their basic functionality is the same regardless of the origin of the data which backs them.

**To Deploy or Not to Deploy?**

Having an application in mind whose scope is manageable, eminently manageable even, as is an application based on public data, lets you devote time and energy to deployment.  And, this step, while sometimes painful, is an important one in the application development process...maybe the most important one.   It's easy to continue to work and rework an application, test, add features, optimize and refactor and never get around to deploying. If you've developed a blog platform, a ToDo list, then it's easy to just keep working on the application and never feel motivated to deploy.  But, no matter how modest your public data driven application, there will be folks in your community who find your application interesting and useful.  I guarantee it.  You'll hear feedback.  You'll get praise, comments and some complaints.  This dialogue will add to your personal sense of satisfaction as well as give you motivation and ideas for enhancements and new features.  

In developing the Express-News' restaurant inspection application, I estimate I spent 50+ hours developing the actual application...maybe a bit more.  But, the deployment process itself was an additional 25+ or so.  I came from a Rails background before and an applications I worked on were deployed by others, so, for me, the deployment process was extremely educational.  I deployed the initial version of the application on AWS Elasticbeanstalk but found this tutorial [Full Stack Python Guide to Deployment](http://www.fullstackpython.com/deployment.html) extremely useful.  It's a great walk-through deploying a Flask application to Linode using [Ansible](http://www.ansible.com/home) and incorporating a CI server with [Jenkins](https://jenkins-ci.org/). 

**Example Django applications made from public data**

[LA Times Homicide Application](http://homicide.latimes.com/)                
This site grew out of the desire to report on every homicide in LA County.  So, it's a database that was built by hand by reporters/developers at the Times.  But, you could do something similar with a FOIA request, made yearly, let's say, or every six months to your local police department.

[Sunlight Foundation Influence Explorer API](http://data.influenceexplorer.com/api/)                                                                      
[Sunlight Foundation Influence Explorer](http://realtime.influenceexplorer.com/race/president/)           
Sunlight is a non-profit, non-partisan foundation that uses technology, open data and traditional journalism to make government more accountable and transparent.  Some tools, among others, include Android/iOS applications for information about Congress, the Open States project that lets you "track state bills, get campaign and contact information for legislators and follow all the action across 50 states, D.C. and Puerto Rico," and, my favorite, the Influence Explorer.  Influence Explorer is a real-time money in politics tracker that aggregates many datasources covering political campaign finance, lobbying money (domestic and foreign) and Federal spending including Federal contracts. The application also includes an API (and bulk data downloads) so you can use the data to power your own Django application.

[Illinois State Board of Education Data](http://www.isbe.net/assessment/report_card.htm)                                 
[Chicago Tribune School Report Card](http://schools.chicagotribune.com/)        
The Chicago Tribune has it's own reprise of chicagocrime.org as well as many other Django offerings, but the one I like most in this context is their School Report Card application.  The raw data from the state of Illinois is an abysmal mishmash of links, PDFs and Excel spreadsheets.  And, the data is important. The application lets users compare one school to another on a couple fundamental demographic points.

[Never Events](http://aidianholder.net/portfolio/projects/neverevents/)         
[Inpatient Prospective Payment System](http://www.cms.gov/Medicare/Medicare-Fee-for-Service-Payment/AcuteinpatientPPS/index.html)                               
Aidian Holder is a developer/journalist who's worked for a number of television stations.  This application deals with what Medicare calls "Never Events", events that should never happen in a hospital setting but nevertheless do happen, for example, leaving surgical tools inside the body.  The data comes from CMS.gov (which is a great place to get alot of data!).  Like the the Illinois school data, the CMS data is pretty much unusable by 'normal' people.  This application lets users quickly and easily find which hospitals have a higher incidents of these "Never Events" compared to their peers.  (This dataset is no longer updated by Medicare. The information has been folded into another dataset and tracked there.)

[Texas Tribune Salaries Explorer](http://salaries.texastribune.org/)            
Every year, Texas Tribune developers request salary data from public offices all over Texas.  They aggregate and normalize this data by office so that users can sift, browse and filter the data on their own.  On the surface, this application is straightforward, like all the others. The real work here is normalizing the many different datasets and compensation structures.  But, you could easily take one office, a large city government, for example, and start there.

[SAEN Application-San Antonio Restaurant Inspections](http://inspections.elasticbeanstalk.com/)                                                        
[San Antonio Restaurant Inspections](http://www.sanantonio.gov/Health/FoodLicensing/FoodEstablishmentInspections.aspx)                     
[San Antonio Restaurant Inspections Raw Feed](http://samhd.tx.gegov.com/San%20Antonio/search.cfm)                                                   
[Restaurant Inspection Full Repo](https://github.com/sa-express-news/food_estab_inspecs)                                                        
The final example is one whose code we'll dig into a bit.  A few reporters in San Antonio started posting screenshots of San Antonio's worst scoring restaurants.  I dug into the data on the Health Department's website and saw that we can a lot better than screenshots.  I wrote a scraper that runs weekly and writes CSVs that feed into a PostgreSQL database.  The data is of interest to the general public but in a terrible format on the city's site.  I wanted to make the data more user friendly and use Django to do it.  

**Public Data Sources**                                                         
[Data.gov](http://www.data.gov/)                                                
The site has tons of datasets, 150,000+, on every topic imaginable.  Data-Journalism types have often bemoaned how this site turned out, but I doubt that any of them have actually tried to use data from it.   (They expected more.)  The site is definitely worth browsing and has many cool datasets.  

[Census Reporter](http://censusreporter.org/)                                 
A Knight-Foundation funded project, this site does what does what the government census site, AmericanFactFinder, doesn't...make Census data useful to the average person in a beautiful and clear way.  If  you're interested in working with Census Data, this site is good place to start browsing.  You can easily see what's available in the data and get some ideas. 

[Raw Census Data](http://census.ire.org/)                                       Another great Census Data resource, this site grew from journalists' collective frustration with the virtually unusable [AmericanFactFinder](http://factfinder.census.gov/faces/nav/jsf/pages/index.xhtml).  The Census Data is presented in a raw format or via API in a clear and easily navigable way.  You can download the raw data, shapefiles or make REST calls.  

[San Antonio GIS Data](http://www.sanantonio.gov/GIS/GISData.aspx)              
Check your local government site to look for data they collect and distribute.  You might have to do some digging, but there's good chance they collect some data and publish it for your use.  San Antonio also distributes shapefiles for public use.  These datasets will cover a variety of topics.  Some city goverments, like San Francisco, [SF Open Data](https://data.sfgov.org/), have large portals along the lines of the Federal government that contain many datasets.  Another good place to look is your local public transportation site.  New York City's Metropolitan Transit Authority (MTA) has all kinds of data about it's subway and bus system, [NYC MTA Data](http://web.mta.info/developers/developer-data-terms.html#data), see if your city has something similar.  

[30 Places for Open Data](http://blog.visual.ly/data-sources)                   
A comprehensive list of "open", public data.  The site has sources for government and political data, city specific data, international data from UNICEF and WHO, well-known data aggregators, social, sports, weather and many others.  Many of these datasets/data sites have various APIs that you could use to build applications around  

[FOIA](https://www.ifoia.org/)                                                 
A 'FOIA' request is a formal request to a government agency asking them to send you a dataset.  It is literally asserting your right as a citizen to access public data that might not be readily available online.  This site walks you through the process of making a FOIA request.  It pre-generates a FOIA letter for you and will even send the letter to the appropriate government agency, if the agency exists within their database.  You can contribute information back to the community if your desired agency doesn't already exist in their database. You don't need to use iFOIA to generate your letter, either.  Having a template to follow does help, but, technically, there is not any required formal style that a FOIA letter must conform too.  

**Notes**

1. [...chicagocrime.org was the first public Django-powered site not run by the Lawrence Journal-World.](http://www.holovaty.com/writing/chicagocrime.org-tribute/)
2. [Not bad for a few nerds hacking in a basement in Lawrence, Kansas, eh?](https://jacobian.org/writing/django-community-2012/)