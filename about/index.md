---
layout: page
title: About DeanLan
image:
  feature: abstract-5.jpg
  background: triangular.png

comments: false
modified: 2016-12-09
---

<!-- Language Selector -->
<select class="sel-lang" onchange= "onLanChange(this.options[this.options.selectedIndex].value)">
    <option value="0" selected> 英文 English  </option>
    <option value="1"> 中文 Chinese </option>
</select>


<!-- English Version -->

<div class ="en post-container">
      <blockquote>
      <p>
     We should consider every day lost on which we have not danced at least once.
     </p>
     </blockquote>
 <p>Hi, I am <strong>deanlan</strong>, software engineer, I worked as a intern at <a href="http://www.intel.com/">Intel</a>, <a href="http://www.gtja.com/portal/channel/indexen.jhtml"> Guotai Junan Securities</a>, <a href="http://www.weimob.com/"> Weimob</a>.
    I will graduate from <a href="http://www.sjtu.edu.cn/"> SJTU</a> in 2017, and will work at <a href="http://www.tencent.com/">Tencent</a>, as a back-end  software engineer.</p>

</div>   



<!-- Chinese Version -->

<div class="zh post-container">

    <!-- copied from markdown -->
    <blockquote><p>
    怕什么真理无穷，进一步有进一步的欢喜</p></blockquote>

    <p>Hi，我是<strong>兰枫</strong>， 程序员 &amp; 工程师，曾在<a href="http://www.intel.com/">Intel</a>， <a href="http://www.gtja.com/"> 国泰君安</a>，<a href="http://www.weimob.com/"> Weimob</a> 实习。
    将在2017年从<a href="http://www.sjtu.edu.cn/">上海交通大学</a> 毕业，将于2017年加入<a href="http://www.tencent.com/">腾讯</a>，负责后台开发。</p>

    <p>我感兴趣的领域有后台开发，分布式系统，图像处理，机器学习，模式识别 想要成为优秀的架构师！</p>

    <p>我热爱生活，争取认真过好每一天！</p>

   

</div>




<!-- Handle Language Change -->
<script type="text/javascript">
    // get nodes
    var $en = document.querySelector(".en");
    var $zh = document.querySelector(".zh");
    var $select = document.querySelector("select");

    // bind hashchange event
    window.addEventListener('hashchange', _render);

    // handle render
    function _render(){
        var _hash = window.location.hash;
        // en
        if(_hash == "#en"){
            $select.selectedIndex = 0;
            $en.style.display = "block";
            $zh.style.display = "none";
        // zh by default
        }else{
            // not trigger onChange, otherwise cause a loop call.
            $select.selectedIndex = 1;
            $zh.style.display = "block";
            $en.style.display = "none";
        }
    }

    // handle select change
    function onLanChange(index){
        if(index == 0){
            window.location.hash = "#en"
        }else{
            window.location.hash = "#zh"
        }
    }

    // init
    _render();
</script>


<!--

## HPSTR Features:

* Compatible with Jekyll 3 and GitHub Pages.
* Responsive templates for post, page, and post index `_layouts`. Looks great on mobile, tablet, and desktop devices.
* Gracefully degrades in older browsers. Compatible with Internet Explorer 8+ and all modern browsers.  
* Sweet animated menu.
* Background image support.
* Support for large images to call out your favorite posts.
* Optional [Disqus](http://disqus.com) comments.
* Simple and clear permalink structure[^1].
* [Open Graph](https://developers.facebook.com/docs/opengraph/) and [Twitter Cards](https://dev.twitter.com/docs/cards) support for a better social sharing experience.
* [Custom 404 page]({{ site.url }}/404.html) to get you started.
* [Syntax highlighting]({{ site.url }}/code-highlighting-post/) stylesheets to make your code examples look snazzy.

<div markdown="0"><a href="{{ site.url }}/theme-setup/" class="btn btn-info">Theme Setup</a> <a href="https://github.com/mmistakes/hpstr-jekyll-theme" class="btn btn-success">Download HPSTR</a></div>

[^1]: Example: *domain.com/category-name/post-title*

-->
