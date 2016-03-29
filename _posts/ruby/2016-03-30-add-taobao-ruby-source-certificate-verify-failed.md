---
layout: post
title:  "add taobao ruby source certificate verify failed"
author: runphp
date:   2016-03-30 02:04:12 +0800
category: ruby
tags: certificate taobao ssl
---
添加淘宝ruby镜像时
{% highlight bash %}
gem sources --add https://ruby.taobao.org/ --remove https://rubygems.org/
{% endhighlight %}

出现错误如下:
{% highlight bash %}
Error fetching https://ruby.taobao.org/:
        SSL_connect returned=1 errno=0 state=error: certificate verify failed (https://rubygems-china.oss-cn-hangzhou.aliyuncs.com/specs.4.8.gz)
{% endhighlight %}

处理如下:
{% highlight bash %}
cd /etc/ssl/certs
wget http://curl.haxx.se/ca/cacert.pem
export SSL_CERT_FILE=/etc/ssl/certs/cacert.pem
{% endhighlight %}
