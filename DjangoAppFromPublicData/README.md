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

**Links**

[LA Times Homicide Application](http://homicide.latimes.com/)                
This site grew out of the desire to report on every homicide in LA County.  So, it's a database that was built by hand by reporters/developers at the Times.  But, you could do something similar with a FOIA request, made yearly, let's say, or every six months to your local police department.

[Sunlight Foundation Influence Explorer API](http://data.influenceexplorer.com/api/)                                                                      
[Sunlight Foundation Influence Explorer](http://realtime.influenceexplorer.com/race/president/)           
Sunlight is a non-profit, non-partisan foundation that uses technology, open data and traditional journalism to make government more accountable and transparent.  Some tools, among others, include Android/iOS applications for information about Congress, the Open States project that lets you "track state bills, get campaign and contact information for legislators and follow all the action across 50 states, D.C. and Puerto Rico," and, my favorite, the Influence Explorer.  Influence Explorer is a real-time money in politics tracker that aggregates many datasources covering political campaign finance, lobbying money (domestic and foreign), Federal spending including Federal contracts. The application also includes an API (and bulk data downloads) so you the data to power your own Django application.

[Illinois State Board of Education Data](http://www.isbe.net/assessment/report_card.htm)                                 
[Chicago Tribune School Report Card](http://schools.chicagotribune.com/)           





**Links**

[Never Events](http://aidianholder.net/portfolio/projects/neverevents/)

[Inpatient Prospective Payment System](http://www.cms.gov/Medicare/Medicare-Fee-for-Service-Payment/AcuteinpatientPPS/index.html)

[Texas Tribune Salaries Explorer](http://salaries.texastribune.org/)

[San Antonio Restaurant Inspections](restaurants.expressnews.com or some crazy amazon url)

[San Antonio Restaurant Inspectons](http://www.sanantonio.gov/Health/FoodLicensing/FoodEstablishmentInspections.aspx)

[San Antonio Restaurant Inspections Raw Feed](http://samhd.tx.gegov.com/San%20Antonio/search.cfm)

[Data.gov](http://www.data.gov/)

[Census Reporter](http://censusreporter.org/)

[Census Data](http://census.ire.org/)

[SF Open Data](https://data.sfgov.org/)

[NYC MTA Data](http://web.mta.info/developers/developer-data-terms.html#data)

[Sports Football Reference](http://www.pro-football-reference.com/)

[30 Places for Open Data](http://blog.visual.ly/data-sources)

[FOIA](https://www.ifoia.org/)

[Restaurant Inspection Full Repo](https://github.com/sa-express-news/food_estab_inspecs)

[Readme Link](https://github.com/jkokenge/talks/tree/master/DjangoAppFromPublicData)




**Notes**

1. [...chicagocrime.org was the first public Django-powered site not run by the Lawrence Journal-World.](http://www.holovaty.com/writing/chicagocrime.org-tribute/)
2. [Not bad for a few nerds hacking in a basement in Lawrence, Kansas, eh?](https://jacobian.org/writing/django-community-2012/)