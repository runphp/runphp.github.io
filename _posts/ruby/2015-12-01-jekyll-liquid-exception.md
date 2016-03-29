---
layout: post
title:  "Jekyll 发生异常 Liquid Exception: SSL_connect"
author: runphp
date:   2015-12-01 15:00:48 +0800
category: ruby
tags: jekyll-gist
---
windows下Jekyll添加jekyll-gist后，启动服务发生异常，异常示例如下：

{% highlight bash %}
Liquid Exception: SSL_connect returned=1 errno=0 state=SSLv3 read server certificate B: certificate verify failed in d:/workspace_php/runphp.github.io/_posts/ruby/2015-11-26-welcome-to-jekyll.md
jekyll 3.0.1 | Error:  SSL_connect returned=1 errno=0 state=SSLv3 read server certificate B: certificate verify failed
{% endhighlight %}

解决方案

1. 下载<http://curl.haxx.se/ca/cacert.pem>
2. 复制到`C:\Windows\`
3. 运行下面命令:
{% highlight bash %}
export SSL_CERT_FILE=c:/windows/cacert.pem
{% endhighlight %}
4. 重新运行`jekyll serve`
