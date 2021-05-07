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
You can simply use the Invoke Command to run the gpresult command:
  - Define the ComputerName after the Invoke-Command
  - In the ScriptBlock you can simply run your command
  
{% highlight powershell%}
Invoke-Command -ComputerName 'ComputerName' -ScriptBlock{
    gpresult /r /USER 'username'
}
{% endhighlight %}



You can have many headings - interesting?
======

Aren't headings cool?
------

What happens here?