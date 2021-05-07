---
title: 'Run a gpresult on a remote computer'
date: 2021-05-06
permalink: /posts/2021/05/gpresult-remote/
tags:
  - powershell
  - gpresult
  - GPO
  - GroupPolicy
---

## Use the Invoke-Command
You can simply use the Invoke Command to run the gpresult command on a remote computer:
  - Define the ComputerName after the Invoke-Command
  - In the ScriptBlock you can simply run your command
  
{% highlight powershell%}
Invoke-Command -ComputerName 'ComputerName' -ScriptBlock{
    gpresult /r /USER 'username'
}
{% endhighlight %}

## Run gpresult for a specific User in a RDS environment
In the following script you just have to define the username + the RDS ConnectionBroker.
It will automatically find the Remote Desktop Server where the user is logged in an run the gpresult there:

{% highlight powershell%}
# Define User Identity
$User = 'username'
$ConnectionBroker = 'rdsgw.test.com'

# Get SamAccount Name
$userSam = (get-aduser -Identity $User).SamAccountName
# Get RDS Server where user is logged in
$userSession = Get-RDUserSession -ConnectionBroker $ConnectionBroker | Select-Object UserName, HostServer | Where-Object UserName -like $userSam 
$server = $userSession.HostServer

# do a gpresult for the specific user on the correct RDS Server
Invoke-Command -ComputerName $server -ScriptBlock{
    gpresult /r /USER $args[0]
}-ArgumentList $userSam
{% endhighlight %}


You can have many headings - interesting?
======

Aren't headings cool?
------

What happens here?