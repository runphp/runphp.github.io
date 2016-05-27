---
layout: post
title:  "php上个月时间范围"
author: runphp
date:   2016-05-26 15:08:48 +0800
category: php
---
{% highlight php %}
$day = date('d')-1;
echo strtotime(date("Y-m-d", strtotime('-1 month '.-$day.' day')));
echo "\n";
echo strtotime(date("Y-m-d", strtotime(-$day.' day')));
{% endhighlight %}
