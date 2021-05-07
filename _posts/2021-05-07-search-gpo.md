---
title: 'Search a specific entry over all GPO'
date: 2021-05-07
permalink: /posts/2021/05/search-gpo/
tags:
  - powershell
  - GPO
  - GroupPolicy
---

A way to search a specific setting over all GPOs


## Generate a GPO Report over your Domain
You can generate a GPO Report over your Domain either in a XML or HTML file and then search through that file.

To generate a XML use this command:  
{% highlight powershell%}
Get-GPOReport -All -Domain "domain.com" -Server "DC01" -ReportType XML -Path "C:\GPOReports\GPOReportsAll.xml"
{% endhighlight %}

To generate a HTML file you can use this command:
{% highlight powershell%}
Get-GPOReport -All -Domain "domain.com" -Server "DC01" -ReportType HTML -Path "C:\GPOReports\GPOReportsAll.html"
{% endhighlight %}

All GPO settings will be included in this Report file. So you can search through that file and find your settings.
