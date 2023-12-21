<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:css='false' b:defaultwidgetversion='2' b:js='true' b:layoutsVersion='3' b:responsive='true' b:templateUrl='indie.xml' b:templateVersion='1.3.0' expr:dir='data:blog.languageDirection' expr:lang='data:blog.locale' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>
  <head>
    <link href='https://fonts.googleapis.com/css?family=Fira Sans' rel='stylesheet'/>
    <!-- Meta Umum -->
    <b:include data='blog' name='google-analytics'/>
    <meta content='width=device-width,initial-scale=1' name='viewport'/>
    <link expr:href='data:view.url.canonical' rel='canonical'/>
    <link expr:href='data:blog.blogspotFaviconUrl' rel='icon' type='image/x-icon'/>
    <b:if cond='data:blog.adultContent'><meta content='adult' name='rating'/></b:if>
    <b:tag cond='data:blog.googleProfileUrl' expr:href='data:blog.googleProfileUrl' name='link' rel='publisher'/>
    <link expr:href='data:blog.homepageUrl.canonical' expr:hreflang='data:blog.locale' rel='alternate'/>
    <meta content='blogger' name='generator'/>
    <meta expr:charset='data:blog.encoding'/>
    <meta content='unsafe-url' name='referrer'/>
    <!-- Meta Kata Kunci -->
    <meta expr:content='&quot;bahasa indonesia, manga, manhua, manhwa, komik, online, baca, &quot; + data:blog.pageName' name='keywords'/>
    <meta expr:content='data:blog.title' property='article:tag'/>
    <!-- Meta Deskripsi -->
    <meta expr:content='&quot;Baca Komik &quot; + data:blog.pageName + &quot; Bahasa Indonesia&quot;' property='og:description'/>
    <meta expr:content='&quot;Baca Komik &quot; + data:blog.pageName + &quot; Bahasa Indonesia&quot;' name='description'/>
    <!-- Meta Judul -->
    <b:if cond='data:view.isHomepage'>
      <title><data:view.title.escaped/> - Site Tagline</title>
      <meta expr:content='data:view.title' property='og:title'/>
      <meta expr:content='data:view.title' property='og:image:alt'/>
      <meta expr:content='data:view.title' name='twitter:title'/>
      <meta expr:content='data:view.title' name='twitter:image:alt'/>
      <b:elseif cond='data:view.isPost'/>
      <title><data:blog.pageName/> - Site Tagline</title>
      <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title' property='og:title'/>
      <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title' property='og:image:alt'/>
      <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title' name='twitter:title'/>
      <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title' name='twitter:image:alt'/>
      <b:elseif cond='data:view.isPage'/>
      <title><data:blog.pageName/></title>
      <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title' property='og:title'/>
      <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title' property='og:image:alt'/>
      <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title' name='twitter:title'/>
      <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title' name='twitter:image:alt'/>
      <b:elseif cond='data:view.isMultipleItems and !data:view.isHomepage'/>
      <title>Rekomendasi Komik <data:blog.pageName/> Terbaik</title>
      <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title' property='og:title'/>
      <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title' property='og:image:alt'/>
      <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title' name='twitter:title'/>
      <meta expr:content='data:blog.pageName + &quot; - &quot; + data:blog.title' name='twitter:image:alt'/>
      <b:elseif cond='data:view.isError'/>
      <title>Page Not Found</title>
      <meta expr:content='&quot;Page Not Found - &quot; + data:blog.title' property='og:title'/>
      <meta expr:content='&quot;Page Not Found - &quot; + data:blog.title' property='og:image:alt'/>
      <meta expr:content='&quot;Page Not Found - &quot; + data:blog.title' name='twitter:title'/>
      <meta expr:content='&quot;Page Not Found - &quot; + data:blog.title' name='twitter:image:alt'/>
      <b:else/>
      <title><data:view.title/></title>
      <meta expr:content='data:view.title' property='og:title'/>
      <meta expr:content='data:view.title' property='og:image:alt'/>
      <meta expr:content='data:view.title' name='twitter:title'/>
      <meta expr:content='data:view.title' name='twitter:image:alt'/>
    </b:if>     
    <!-- Meta Image -->
    <b:if cond='data:widgets'>
      <b:loop values='data:widgets.Blog.last.posts where (p =&gt; p.featuredImage) map (p =&gt; p.featuredImage) limit 1' var='imageUrl'>
        <meta expr:content='resizeImage(data:imageUrl,1200,&quot;1200:1200&quot;)' property='og:image'/>
      </b:loop>
    </b:if>
    <meta expr:content='data:view.isHomepage ? &quot;website&quot; : &quot;article&quot;' property='og:type'/>
    <meta expr:content='data:view.url.canonical' property='og:url'/>
    <!-- Meta Robot -->
    <meta content='index/follow' name='robots'/>
    <!-- Feeds -->
    <data:blog.feedLinks/>
    <data:blog.meTag/>

    <b:skin><![CDATA[ 

/*
<Variable name="keycolor" description="Main Color" type="color" default="#ff0000" hideEditor="true"  value="#0b8043"/>
<Group description="Body">
  <Variable name="body.background.color" description="Background color" type="color" default="#fff"  value="#7B1FA2"/>
</Group>
<Variable name="secclr" description="Secondary Color" type="color" default="#7b0000"  value="#5e268c"/>
<Variable name="border.radius" description="Border Radius" type="length"
            min="2px" max="50px" default="2px"  value="3px"/>
<Variable name="b.w" description="Blog Width" type="length"
            min="1000px" max="1300px" default="1180px"  value="1200px"/>
<Variable name="s.w" description="Sidebar Width" type="length"
            min="300px" max="500px" default="315px"  value="339px"/>
<Group description="Status Color">
<Variable name="com" description="Completed Color" type="color" default="#228b22"  value="#7B1FA2"/>
<Variable name="ong" description="Ongoing Color" type="color" default="#ffa500"  value="#00ccea"/>
<Variable name="soo" description="Coming Soon Color" type="color" default="#2f4f4f"  value="#7B1FA2"/>
<Variable name="drp" description="Dropped Color" type="color" default="#ff0000"  value="#00ea70"/>
</Group>
<Group description="New Comment Required - Dont edit">
<Variable name="body.background" description="Background" color="#505050" type="background" default="$(color) none repeat scroll center center"  value="$(color) none repeat scroll center center"/>
<Variable name="body.text.font" description="Font komentar Blogger" type="font" default="$(fontBody)" value="400 14px &#39;Roboto&#39;, sans-serif"/>
<Variable name="body.text.color" description="Color" type="color" default="#505050"  value="#212121"/>
<Variable name="body.link.color" description="Link color" type="color" default="#161617"  value="#5e268c"/>
<Variable name="posts.title.color" description="Post title color" type="color" default="#161617"  value="#5e268c"/>
<Variable name="posts.text.color" description="Post text color" type="color" default="#505050"  value="#212121"/>
<Variable name="posts.icons.color" description="Post info color" type="color" default="#505050" value="#212121"/>
<Variable name="posts.background.color" description="Post background color" type="color" default="#f7f7fc"  value="#fbf7f3"/>
<Variable name="tabs.font" description="Font" type="font" default="400 14px &#39;Roboto&#39;, sans-serif" value="400 14px &#39;Roboto&#39;, sans-serif"/>
<Variable name="tabs.overflow.background.color" description="Popup background color" type="color" default="#ffffff"  value="#ffffff"/>
<Variable name="labels.background.color" description="Labels background color" type="color" default="#fff" value="#ffffff"/>
</Group>
*/
:root {
  --primary-color: $(keycolor);
--v171: #17151b;
--v999: #999;
--hf1f: #f1f1f1;
}
.dark-mode {--hf1f: #333}
*, ::after, ::before {
    box-sizing: border-box;
}
html{height:100%;scrollbar-width: thin;scroll-behavior:smooth;}
::-webkit-scrollbar { -webkit-appearance: none; width: 7px; height: 5px;}
::-webkit-scrollbar-thumb {background: gray;}
body{overflow-x:hidden;height:100%;}
iframe{width:100%;border:0}
svg{width:24px;height:24px}
.svg-1{stroke:white;width:34px;height:34px;}
.svg12 {width: 14px;height: 14px;color: rgba(255,255,255,0.4);}
.svg14 svg{width:14px;height:14px}
.svg12sv svg {width:12px;height:12px}
.dark-mode{background-color:#1a1a1a;color:white}
.modeSwitch{position:relative;display:inline-block;width:32px;height:17px}
.modeSwitch input{opacity:0;width:0;height:0}
.toggleSwitch{position:absolute;cursor:pointer;top:0;left:0;right:0;bottom:0;background-color:rgba(0,0,0,.28);transition:.3s;border-radius:17px}
.toggleSwitch:before{position:absolute;content:"";height:13px;width:13px;left:2px;bottom:2px;background-color:whitesmoke;transition:.4s;border-radius:50%}
input:focus+.toggleSwitch{box-shadow:0 0 1px #2196f3}
.dark-mode input+.toggleSwitch:before{transform:translateX(15px)}
body{font-family:fira sans,sans-serif;counter-reset:section;background-color:#e8ebf5;color:#222d34;font-size:15px;line-height:1.4;}
a{color:#222d34;text-decoration:none}
a:hover,.infolimit a,::marker{color:$(keycolor)}
.link a,.dark-mode .link a,#allert a{color:$(keycolor)}
#sidebar a{color:#222}
.m-0,body,#sidebar .title,.flat,figure,#PopularPosts2 .title,.related.style-2,#main .widget .title,#feed .title,#wpac-rating{margin:0}
.pen .separator a,.page-view .separator a{padding:0 !important}
.max-w,.fw .mx-feed,#notification .widget{max-width:$(b.w)}
.ads img,#sidebar .widget-content img{max-width:100%;height:auto;}
.pv main .max-w{max-width:1080px}
.h-14{height:14px;vertical-align:middle;}
.w-180{width:180px}
.w-50p{max-width:600px}
.w-25{width:25px}
.wh-18-svg svg{width: 18px;height: 18px}
.mra,#notification .widget{margin-right:auto}
.mla,#notification .widget{margin-left:auto}
.mta{margin-top:auto}
.p-y6x12{padding:6px 12px}
.p-y5x20{padding:5px 20px}
.p-y0x15{padding:0 15px}
.p-y7x15-a a{padding:7px 15px}
.p-y10x15{padding:10px 15px;}
.p-y12x15{padding:12px 15px}
.p-15,#disqus_thread{padding:15px}
.p-20,#downloadlist{padding:20px}
.p-10,.prev,.all,.next,.pv .m-GwWBFmbcL{padding:10px}
.p-5,.ofz{padding:5px}
.p-6{padding:6px}
.p-13,#sidebar .widget-content{padding:13px}
.pr-15{padding-right:15px}
.pl-15{padding-left:15px}
.px-5 {padding-left: 5px;padding-right: 5px}
.pr-10{padding-right:10px}
.mr-13{margin-right:13px}
.mr-20{margin-right:20px}
.ml-20,#downloadlist .db{margin-left:20px}
.ml-7{margin-left:7px}
.pv .ml-7{margin-left:auto}
.ml-0{margin-left:0}
.md-ml-0{margin-left:0}
.mr-40{margin-right:40px}
.mr-7,h2 > svg,h3 > svg{margin-right:7px}
.mt-5{margin-top:5px}
.mt-15,.ch-bottom,.ch-top{margin-top:15px}
.mt-35{margin-top:35px}
.mb-2{margin-bottom:2px}
.mx-5{margin-right: 5px;margin-left: 5px}
.mb-6{margin-bottom:6px}
.mt8{margin-top:8px}
.mt-24,#disqus_thread,.svo .mt-sv15{margin-top:24px}
.mt-n100{margin-top:-100px}
.mb-13{margin-bottom:13px}
.mb-20,.not-home-mb20{margin-bottom:20px}
.mb-0{margin-bottom:0}
.mb-15,.ch-top,#disqus_thread,.pv .m-GwWBFmbcL{margin-bottom:15px}
.label-view .mb-20lv, #sidebar .widget:last-child{margin-bottom:20px}
.mr-3{margin-right:3px}
.mt-0{margin-top:0}
#main .widget-content,#slide .widget-content{margin:13px}
.grid,#sidebar,.overlay,.flat,#Blog1,.ChapterNav,.style-2{display:grid}
.flex,#sidebar .list-label-widget-content .label-name,#PageList2,.score,.ofz,.slider-nav,.nextPrev a{display:flex}
.block,.b-img img,.homechapter a,.icon,figure .separator img,.block-a a{display:block}
.header-image-wrapper img{transition:.3s;max-height:50px;max-width: 150px;}
.header-image-wrapper img:hover{transform:scale(1.2);}
.i-mage img{position:absolute;height:100%;left:0;top:0;}
.i-block{display:inline-block}
.i-flex{display:inline-flex}
.hidden,.post .separator,.hi .index-list,.hi #downloadlist,#Viewer-module,#sidebar .item-byline,#notification h3,#recommendations .title,#ecHome,#myUL li:not([data*="Chapter"]),.post #character{display:none}
.gtc-3c {grid-template-columns: auto auto 1fr;gap: 10px;}
.gtr-mc{grid-template-rows:max-content}
.gtc-header{grid-template-columns:auto 1fr auto}
.gtc-main{grid-template-columns:1fr $(s.w)}
.gtc-175fr{grid-template-columns:175px 1fr}
.gtc-1frxa{grid-template-columns:1fr minmax(100px,150px) minmax(100px,150px);border-bottom:solid 1px #eceff5}
.gtc-f141a{grid-template-columns:repeat(auto-fill,minmax(141px,1fr))}
.hfeed{grid-template-columns:repeat(auto-fill,minmax(141px,1fr))}
.gtr-a1fa{grid-template-rows:auto 1fr auto}
.gtc-rx1fr{grid-template-columns:1fr 1fr}
.gtc-100a1fr{grid-template-columns:minmax(100px,auto) 1fr}
.gtc-4x{grid-template-columns:repeat(4, 1fr);padding:5px}
.gtc-101{grid-template-columns:101px auto}
.gtc-142{grid-template-columns:repeat(auto-fill,minmax(114px,1fr))}
.gtc-4460{grid-template-columns:repeat(auto-fill,minmax(170px,1fr))}
.a1{grid-area:a1;}
.a2{grid-area:a2;}
.a3{grid-area:a3;}
.a4{grid-area:a4;}
@media screen and (min-width:1024px){.gtc-235fr{grid-template-columns:235px minmax(200px,auto);grid-template-areas: "a1 a2""a3 a3""a4 a4";}
}
.ChapterNav{grid-template-columns:repeat(3,1fr)}
.aic,.nextPrev a{align-items:center}
.pcc{place-content:center}
.pic{place-items:center}
.jic{justify-items:center}
.bsc{background-size:cover}
.fdcr{flex-direction:column}
.jcsb,.label-name,.ofz{justify-content:space-between}
.jcc,.slider-nav{justify-content:center}
.jsc{justify-self:center}
.tac,.ChapterNav,.score,.ads .widget-content,#notification .widget-content{text-align:center}
.lsn,.Label,.flat,.related.style-2 li,#downloadlist ul,#myUL{list-style:none}
.Label ul,.flat,.pl-0,.related.style-2,.dsq-widget-list,#downloadlist ul,#myUL{padding-left:0}
.bg-main,.pagecurrent,.all,.releases,#PageList2{background:linear-gradient(to right, $(keycolor) , $(secclr))}
.header-background {background-color: $(keycolor)}
.jsfe{justify-self:flex-end}
.lh-60{line-height:60px}
.lh-42{line-height:42px}
.lh-37 {line-height:37px}
.lh-25px {line-height:25px}
.lh-26{line-height:26px}
.lh-20{line-height:20px}
.lh-1d7,.homechapter{line-height:1.7}
.lh-35{line-height:35px}
.gg-30{grid-gap:30px}
.gg-20,#Blog1{grid-gap:20px}
.gg-15{gap:15px}
.gg-10,.style-2{gap:10px}
.g5 {gap: 5px}
.fw-600,#sidebar #BlogArchive1 a,.subItem li .chpName{font-weight:600}
.fw-500{font-weight:500}
.fsi{font-style:italic}
#sidebar .c-fff ,.c-fff,#sidebar .overlay a,.date,.post-labels,.white\:hover:hover,.pagecurrent,.all,.all:hover{color:white}
.dim\:hover:hover{filter:brightness(80%)}
.c-666{color:#666}
.c-ddd{color:#ddd}
.c-999,.c-999-a a{color:var(--v999)}
.c-22{color:#222d34}
.c-555{color:#555}
.bg-171{background-color:var(--v171)}
.bg-999{background-color:var(--v999)}
.c-cc,#PageList2 a:hover{color:#ccc}
.bn{border:none}
.bg-trans{background:rgba(0,0,0,.18)}
.bg-222{background:#222}
.bt{background-color:transparent}
.r3,.col section .counter::before{border-radius:3px}
.tlr-5{border-top-left-radius:5px;border-top-right-radius:5px;}
.r4{border-radius:4px}
.r5{border-radius:5px}
.r50p{border-radius:50%}
.r-50{border-radius:50px}
#sidebar .widget,.r2,.FeaturedPost,#PopularPosts2,#disqus_thread,.ChapterNav,#downloadlist,.ofz,#main .HTML:not(.ads),.alr,.char:hover,.pv .m-GwWBFmbcL,#feed .widget,.tab li{border-radius:$(border.radius)}
.r2f {border-radius: 2px;border: .5px solid var(--primary-color);color: var(--primary-color);}
#sidebar .title {border-top-left-radius:$(border.radius);border-top-right-radius:$(border.radius);}
.c-fff-force {color: white !important;}
.tl-r3{border-top-left-radius:3px}
.bl-r3{border-bottom-left-radius:3px}
.br-r3{border-bottom-right-radius:3px}
.tr-r3{border-top-right-radius:3px}
.cp,.feather-filter,#prev,#next{cursor:pointer}
.feather-sun, .feather-moon{width:14px;height:14px;fill:white;stroke:white}
.feather-star{width:15px;height:13px;fill:$(keycolor);stroke:$(keycolor)}
.feather-bell{stroke:white;}
.unset{all:unset}
#sidebar .widget,.bc-fff,.FeaturedPost,#PopularPosts2,#allert .widget-content,#disqus_thread,.index-list,#downloadlist,#main .HTML:not(.ads),.pv .m-GwWBFmbcL,#feed .widget{background-color:white}
#sidebar .widget,.s1,.FeaturedPost,#PopularPosts2,#disqus_thread,#downloadlist,#main .HTML:not(.ads),#feed .widget{box-shadow:1px 3px 8px rgba(49,49,49,0.1)}
.s2{filter:drop-shadow(1px 1px 2px rgba(0,0,0,0.7))}
#sidebar .title{font-size:17px;padding-bottom:15px}
#sidebar .title,.c-theme,#PopularPosts2 .title,#downloadlist .db,#main .widget .title,#feed .title{color:$(keycolor)}
.col{grid-template-columns:repeat(3,1fr)}
.col section:nth-child(1){grid-column:1 / -1;}
.col img,.full,.post-thumb,.page-view img{width:100%}
.col section:nth-child(n+2) .post-title,.col section:nth-child(n+2) .byline,.col section:nth-child(n+2) .date{display:none}
.col section:nth-child(n+2) img,.ofc{height:135px;object-fit:cover}
.col section:nth-child(1) img{height:165px;object-fit:cover;object-position:top}
.col section:nth-child(1) .ov-title{background:linear-gradient(to bottom,#0000,#000)}
.col section:nth-child(n+2){margin:7px}
#sidebar, #main,.min{grid-auto-rows:min-content}
.relative{position:relative}
.absolute{position:absolute}
.col section .counter::before{counter-increment:section;content:counter(section);position:absolute;top:6px;left:4px;background:$(keycolor);color:white;padding:3px 7px;font-size:13px}
.ov-img, .ov-title{grid-row:1 / -1}
.ov-img{grid-column:1 / -1}
.ov-title{grid-column:1 / -1;align-self:self-end;padding:10px 15px;overflow:hidden}
.date,#sidebar .post-labels{font-size:13px}
#sidebar .post-labels,.wsn{white-space:nowrap}
.clamp{display:-webkit-box;-webkit-line-clamp:1;-webkit-box-orient:vertical;}
#sidebar .post-title,.fwn{font-weight:500}
.toe{text-overflow:ellipsis}
.oh,#PopularPosts2,#main .widget,#feed .widget,#sidebar .widget,#HTML3{overflow:hidden}
#sidebar #PopularPosts1{padding:0 0 3px 0}
#sidebar #PopularPosts1 .title{padding-bottom:0}
.ttu{text-transform:uppercase}
.fz-0d95r{font-size:.9rem}
.fs-30{font-size:30px}
.fs-25{font-size:25px}
.fs-20{font-size:20px}
.fs-9{font-size:9px}
.fs-14,.Label .label-name,.BlogArchive .widget-content,#allert .widget-content,.FeaturedPost .post-labels,.ChapterNav{font-size:14px}
.fs-15,.index-list,#downloadlist ul,#feed .title,#sidebar .title,.fw #main .title{font-size:15px}
.fs-13,.blog-pager{font-size:13px}
.fs-12,.share-icon{font-size:12px}
.fs-11{font-size:11px}
.fs-17{font-size:17px}
.p-3y6x{padding:3px 6px}
.pb-15{padding-bottom:15px}
#downloadlist ul{max-height:500px;overflow:auto}
.info{color:#00529B;background-color:#BDE5F8}
.success{color:#4F8A10;background-color:#DFF2BF}
.warning{color:#9F6000;background-color:#FEEFB3}
.error{color:#D8000C;background-color:#FFBABA}
.boxs{padding:10px;margin:10px 0}
.list-label-widget-content:hover,#download:hover{scrollbar-width:thin}
.list-label-widget-content,#download{max-height:300px;scrollbar-color:$(keycolor) #d4dae6;scrollbar-width:none;overflow:scroll;-webkit-overflow-scrolling:touch;}
.list-label-widget-content:hover,#download:hover{overflow-y:scroll}
.list-label-widget-content::-webkit-scrollbar,#download::-webkit-scrollbar{width:7px}
.list-label-widget-content::-webkit-scrollbar-track,#download::-webkit-scrollbar-track{background:#d4dae6}
.list-label-widget-content::-webkit-scrollbar-thumb,#download::-webkit-scrollbar-thumb{background:$(keycolor)}
.list-label-widget-content li,#downloadlist li{border-bottom:solid 1px #eceff5;padding:7px 10px}
.list-label-widget-content li:hover{background:#f1f1f14f}
.flat{grid-template-columns:1fr 1fr;grid-gap:6px}
.flat .archivedate{background:#f8f9fb;padding:3px;text-align:center;line-height:28px}
.post-count{font-size:12px;color:#999;margin-left:5px;font-weight:normal;}
.post-count::before{content:"("}
.post-count::after{content:")"}
.cloud-label-widget-content .label-size{padding:3px 6px;border:1px solid $(keycolor);display:inline-block;margin-bottom:5px}
#sidebar .cloud-label-widget-content .label-count{margin-left:5px;color:$(keycolor);font-weight:bold}
::selection{color:white;background:$(keycolor)}
.PopularPosts .post-title{display:-webkit-box;-webkit-line-clamp:3;-webkit-box-orient:vertical;overflow:hidden;text-overflow:ellipsis}
.item-thumbnail:hover img{filter:brightness(50%);transition:.2s}
#popular .PopularPosts .item-thumbnail img {width: 58px;height: 75.85px;object-fit: cover;border-radius: 2px;}
.bb-1pxsf,.ofz,#main .widget .title,#sidebar .title,#feed .title{border-bottom:1px solid #f1f1f1}
.bt-1pxs3{border-top:1px solid #333333a1}
.bb-2pxsec{border-bottom:solid 2px #eceff5}
.bt-2sf{border-top:2px solid #f1f1f1}
.s3f5{border-bottom:solid 3px #f5f7fa}
.y9x19p,#main .widget .title,#slide .widget .title,#sidebar .title,#feed .title{padding:8px 15px}
.yb10m,#main .widget .title,#slide .widget .title{margin-bottom:10px}
.m-3{margin:3px}
.m-y0x4-li li{margin:0 4px}
.y10x0{padding:10px 0}
.y3x5p{padding:3px 5px}
.y6x0p{padding:6px 0}
.y5x10p{padding:5px 10px}
.y0x9p{padding:0 9px}
.label{padding:4px 12px;color:$(keycolor);border:1px solid $(keycolor);background-color:$(keycolor)17;}
.label:hover{background-color:$(keycolor);color:white}
.yt8m{margin-top:8px;margin-bottom:8px}
.pv .mtn150{margin-top:-150px}
.pt-140p{padding-top:140%}
.pt-137p{padding-top:137%}
.y6x11p{padding:6px 11px}
.fd\:hover:hover{background-color:#fdfdfd}
.bc-f5{background-color:#f5f7fa}
.bc-2b{background-color:#2b2b2b}
.bc-22{background-color:#222}
.bc-33{background-color:#33333380}
.bc-e8{background-color:#e8ebf5}
.bg\:hover:hover{background:$(keycolor)}
.h-140{height:140px}
.h-220 img{height:199px}
.h-200{height:125px}
.h-135{height:135px}
.h-60{height:60px;width:40px;}
.h-17{height:17px}
.full-i img{width:100%;object-fit:cover;border-radius:2px;}
.b-0{bottom:0}
.l-0{left:0}
.t-3 {top: 3px}
.t-5{top:5px}
.r-5{right:5px}
.b\(50\){filter:brightness(50%)}
.dt{float:right}
[dir="rtl"] .dt{float:left}
.PageList [data]:before{margin-right:5px;vertical-align:sub}
[data="Series"]:before {content: url('https://api.iconify.design/ic:twotone-grid-view.svg?color=rgba(255,255,255,.6)&height=16');}
[data="Home"]:before {content: url('https://api.iconify.design/ant-design:home-twotone.svg?color=rgba(255,255,255,.6)&height=16');}
[data="Other"]::before {content: url('https://api.iconify.design/icon-park-outline:other.svg?color=rgba(255,255,255,.6)&height=16');}
[data="Komik"]::before {content: url('https://api.iconify.design/bx/bxs-book-reader.svg?color=rgba(255,255,255,.6)&height=16');}
[data="Manga List"]::before {content: url('https://api.iconify.design/bx/bx-list-minus.svg?color=rgba(255,255,255,.6)&height=16');}
[data="Bookmark"]::before {content: url('https://api.iconify.design/fluent/library-20-filled.svg?color=rgba(255,255,255,.6)&height=16');}
.chap-by-tag a:visited{color:gray}
.chap-by-tag div:not(:last-child){border-bottom:1px dashed $(keycolor)}
#Label2 .label-count{top:-5px;right:-8px;background:$(keycolor);width:16px;height:16px}
.share-icon{padding:2px 7px;margin:5px}
.facebookThis{background:#1877f2}
.twitterThis{background:#1da1f2}
.whatsappThis{background:#01ba6d}
.pinterestThis{background:#e81737}
.share-icon svg{fill:white;margin-right:4px;width:20px;height:20px}
.fill-f{fill:white}
.vam{vertical-align:middle}
.o5{opacity:.5}
.ofc-f img{width:150px;height:200px;object-fit:cover}
.f-1{flex:1}
.index-list{border-bottom:1px solid #eceff5}
.index-list a{display:block;padding:11px 15px}
.FeaturedPost .post-labels a{color:#606060;display:inline-block;background:#e8e8e9;padding:1px 4px}
.feather-user{width:15px;height:15px;stroke:$(keycolor)}
.feather-tag{width:15px;height:15px;vertical-align:text-top;margin-right:3px}
.dark-mode .header-background,.dark-mode #sidebar .widget,.dark-mode .bc-fff, .dark-mode .FeaturedPost, .dark-mode #PopularPosts2, .dark-mode #allert .widget-content, .dark-mode #disqus_thread,.dark-mode .next,.dark-mode .prev,.dark-mode .index-list,.dark-mode #downloadlist,.dark-mode #main .widget:not(.Blog),.dark-mode .m-GwWBFmbcL,.dark-mode #feed .widget{background-color:#222;}
.dark-mode .bb-1pxsf, .dark-mode #main .widget .title,.dark-mode .ofz,.dark-mode #sidebar .title,.dark-mode #feed .title{border-bottom:1px solid #333}
.dark-mode #sidebar a,.dark-mode a,.dark-mode .next,.dark-mode .prev,.dark-mode .bt-2sf,.dark-mode #downloadlist{color:#ccc}
.dark-mode .list-label-widget-content li,.dark-mode .gtc-1frxa,.dark-mode .index-list,.dark-mode #downloadlist li{border-bottom:solid 1px #333333d6}
.dark-mode .list-label-widget-content li:hover,.dark-mode .fd\:hover:hover{background:#33333361}
.dark-mode .list-label-widget-content,.dark-mode #download{scrollbar-color:$(keycolor) #333333d6}
.dark-mode .list-label-widget-content::-webkit-scrollbar-track,.dark-mode #download::-webkit-scrollbar-track{background:#333333d6}
.dark-mode .bc-f5{background-color:#3333338f}
.link\:hover:hover .ck{color:$(keycolor)}
.dark-mode .flat .archivedate{background:#2b2b2b}
.dark-mode .bt-2sf{border-top:2px solid #333333cf}
.dark-mode .bb-2pxsec{border-bottom:solid 2px #333333cf}
.dark-mode .c-ee{color:#eee}
.dark-mode .bc-e8{background-color:#2b2b2b}
.bg-photo-container{overflow:hidden;position:relative;}
#custom-hero,#custom-hero img,.limit img{position:absolute;top:0;width:100%;height:100%;object-fit:cover;}
.limit img {border-radius: 2px}
.post #custom-hero{display:none;}
.hero-background{height:264px;background-position:center;background-size:cover;width:100%;transform:scale(1.1);filter:blur(5px) saturate(2) brightness(70%);}
@media (max-width:768px){.gtc-175fr{grid-template-columns:125px 1fr}
}
@media (max-width:900px){.gtc-main{grid-template-columns:auto}
}
@media (max-width:375px){.gtc-175fr{grid-template-columns:auto}
.md\:tac{text-align:center}
.fdc-375{flex-direction:column}
}
@media (max-width:600px){#Text1{padding-right:13px;padding-left:13px}
}
@media (max-width:1024px){
.calc-wn20 {width: calc(100% - 20px);margin-right: auto;margin-left: auto;}
.gtc-235fr {grid-template-columns: auto;grid-template-areas: "a1""a2""a3""a4";}
.md-w120{width:120px}
.hero-background{height:170px;}
.md-auto{margin:0 auto}
.module-ctrl.top h1{font-size:1.2rem}
.md-ml-0{margin-left:revert}
.gtc-header{grid-template-columns:auto 1fr;padding:0 13px}
.fdc{flex-direction:column}
#PageList1{justify-self:flex-start}
#Header1{display:flex;align-items:center}
#PageList1,.md\:none{display:none}
.md\:jcc{justify-content:center}
.right{float:right}
.w-180,.md\:full,#PageList1{width:100%}
#PageList1 ul{padding-left:0}
#PageList1 li{border-bottom:1px solid #f1f1f1}
.dark-mode #PageList1 li{border-bottom:1px solid #333}
}
@media (max-width:900px){
.sm\:dn,#Query-input{display:none;}
.menu-item{width:35px;height:35px;overflow:hidden;}
.right{width:35px;height:35px;padding:10px;background:rgba(0,0,0,.4);margin-left:4px;border-radius:5px;display:grid;place-content:center;}
}
@media (min-width:1025px){.search,.menu{display:none}
}
.completed{color:green}
.dropped{color:orangered}
.blog-pager{margin-top:20px;border-top:1px solid #eceff5;padding-top:10px;padding-bottom:10px;text-align:center}
#blog-pager a,.showpageOf,.pagecurrent{padding:9px 16px;margin:5px;border-radius:2px;background-color:#eceff5;display:inline-block}
.dark-mode #blog-pager a,.dark-mode .showpageOf{background-color: #16151d;}
.pagecurrent {background: var(--primary-color);}
.dark-mode .showpageOf,.dark-mode .pagecurrent{border-color:#333333d6;color:#ccc}
.dark-mode #blog-pager a, .dark-mode .blog-pager{border-color:#333333d6}
.pagecurrent{border:none}
.box{box-sizing:border-box}
.icon{height:18px;width:102px;margin-bottom:7px}
.z-1{z-index:1}
.scale-2{scale:2}
.entry-title{-webkit-line-clamp:2;display:-webkit-box;-webkit-box-orient:vertical;overflow:hidden}
.gtc-1frxa:last-child,.index-list:last-child{border-bottom:none}
.label-view #Blog1{grid-gap:0}
#content{display:none}
.score{position:absolute;right:0;z-index:1;padding:3px 5px;font-size:12px;font-weight:500;bottom:0;background:rgba(0,0,0,.8);color:rgba(255,255,255,.9)}
.f1{flex:1}
[data*="Chapter"]{margin-right:5px;color:$(keycolor)}
.ex[data]{display:none}
.ex[data*="Chapter"]{display:block}
.xe[data]{display:inline-flex}
.xe[data*="Chapter"]{display:none}
.hot::before{content:"H";background:orangered;color:white;font-size:14px;padding:1px 4px;margin-right:4px;border-radius:4px;}
.new::before{content:"N";background:limegreen;color:white;font-size:14px;padding:1px 4px;margin-right:4px;border-radius:4px;}
.sac{scroll-snap-align:center}
.sac {scroll-margin-top: 5rem;}
.widget-content.list-label-widget-content::-webkit-scrollbar{display:none}
textarea:focus, input:focus{outline:none}
sup{font-size:15px;vertical-align:top}
.slide{overflow-x:auto;scroll-snap-type:x mandatory;scrollbar-width:none;scroll-behavior:smooth;}
.slide{align-content:center;display:grid;grid-template-columns:repeat(10,minmax(145px,1fr));grid-gap:1em;}
.slide::-webkit-scrollbar{display:none;}
:is(#feed,.slide,#recommendations)  img:hover{transform: scale(1.2);}
:is(#feed,.slide,#recommendations) img {transition: .3s;}
#s11{width:0;height:0;}
.com{top:18px;left:-29px;transform:rotate(-45deg);background:$(com);color:white;padding:2px 24px;box-shadow:0 2px 2px rgba(0, 0, 0, 0.5);}
.ong{top:17px;left:-25px;transform:rotate(-45deg);background:$(ong);color:white;padding:2px 24px;box-shadow:0 2px 2px rgba(0, 0, 0, 0.5);}
.soo{top:24px;left:-33px;transform:rotate(-45deg);background:$(soo);color:white;padding:2px 24px;box-shadow:0 2px 2px rgba(0, 0, 0, 0.5);}
.drp{top:18px;left:-29px;transform:rotate(-45deg);background:$(drp);color:white;padding:2px 24px;box-shadow:0 2px 2px rgba(0, 0, 0, 0.5);margin-left:4px;}
.blob{background:black;border-radius:20px;box-shadow:0 0 0 0 rgba(0, 0, 0, 1);margin:5px 10px;height:12px;width:19px;transform:scale(1);animation:pulse-black 2s infinite;display:inline-block;}
.blob.key{background:$(keycolor);box-shadow:0 0 0 0 $(keycolor)d1;animation:pulse-red 2s infinite;}
@keyframes pulse-red{0%{transform:scale(0.95);box-shadow:0 0 0 0 $(keycolor)d1;}
 70%{transform:scale(1);box-shadow:0 0 0 10px rgba(255, 82, 82, 0);}
 100%{transform:scale(0.95);box-shadow:0 0 0 0 rgba(255, 82, 82, 0);}
}
.pv figure .separator a,.p figure .separator a, .pen .separator a{pointer-events:none;}
.dark #listItem{background:#1b1b1b;}
.list-judul{padding:9px 19px;border-bottom:1px solid #ccd0d7;}
.dark-mode .list-judul{border-bottom:1px solid #514a4a;}
.list-judul h3{margin:0;font-size:19px;font-weight:500}
.searcch{padding:9px 8px}
input#searchchapter{font-weight:300;background:#e8ebf5;box-shadow:none !important;width:100%;height:34px;font-size:14px;line-height:1.42857143;color:white;border:none;border-radius:3px;transition:border-color ease-in-out .15s,box-shadow ease-in-out .15s;padding:10px;}
.char:hover{background-color:$(keycolor)1c}
.dark-mode input#searchchapter,.dark-mode .char:hover{background:#171616}
input#searchchapter::placeholder{color:#555}
.ep-item{padding:0;list-style:none;margin:0;display:flex;flex-wrap:wrap;}
.ep-right{margin-right:9px}
ul.ep-item::-webkit-scrollbar{width:2px;height:2px}
ul.ep-item::-webkit-scrollbar-thumb{border-radius:7px;background-color:#a20a0a}
.ep-item .char{padding:11px 15px 11px 8px;padding-top:11px;font-size:14px;position:relative;width:100%;display:flex;flex-wrap:nowrap;align-items:center;justify-content:space-between;flex:0 0 33%;max-width:33%;}
@media (max-width:768px){.ep-item .char{flex:100%;max-width:50%}
}
.ep-item .char:first-child{padding-top:11px}
.ep-item .char:last-child{border-bottom:none;}
.ep-right .eps{background:$(keycolor);padding:10px;color:#fff;display:block;text-align:center}
.ep-left,.ep-left .eps-jdl{overflow:hidden;width:100%}
.ep-left{flex:1}
.ep-left .eps-jdl{line-height:21px;text-overflow:ellipsis;white-space:nowrap;float:left}
span.eps a{color:#fff}
span.eps a:hover,span.eps-jdl a:hover{color:#a20a0a}
span.eps-jdl a{color:$(keycolor);}
.file-list span{font-size:7px}
.file-list span.eps-date{font-size:14px}
#threaded-comment-form .alr {background: #006b3c;}
.alr{margin-bottom:18px;box-shadow:0 2px 3px rgba(0,0,0,.1);color:#fff;background:#d7382d;font-size:13px;grid-template-columns:50px 1fr;}
.alr.royal{background:royalblue}
#Viewer-module:checked ~ .module-ctrl, .module-ctrl *{transition:.2s;}
.module-ctrl{max-height:0;opacity:0;visibility:hidden;overflow:hidden;}
#Viewer-module:checked ~ .module-ctrl.top, #Viewer-module:checked ~ .module-ctrl.bottom, .module-ctrl{position:fixed;width:100vw}
.module-ctrl{background-color:wheat}
.dark-mode .module-ctrl{background-color:#514d4d}
#Viewer-module:checked ~ .module-ctrl.top, .module-ctrl.top{top:0;}
#Viewer-module:checked ~ .module-ctrl.bottom{bottom:0;}
#Viewer-module:checked ~ .module-ctrl{max-height:200px;opacity:1;visibility:visible;}
.check-box img{max-width:100%;height:auto;margin:0 auto;width:100%}
.series-chapterlist{list-style:none;padding:0;font-size:15px;}
.flexch-infoz{padding:5px;}
.series-chapterlist li{background:#f7fafc;border-bottom:solid 1px #edf2f7;}
.flexch{display:grid;grid-template-columns:50px auto 50px;align-items:center;}
.series-chapterlist li time{display:block;}
.flexch-book, .flexch-dllink{position:relative;padding:10px;background:#edf2f7;font-size:25px;color:#777;text-align:center;}
.series-chapterlist li time{font-size:12px;}
.series-chapterlist li:hover svg{color:white;}
.series-chapterlist li:hover{color:#fff;}
.series-chapterlist li:hover a{color:#fff !important;}
.series-chapterlist li:hover .flexch-book, .series-chapterlist li:hover .flexch-dllink{background:#020202;}
.series-chapterlist li svg{color:$(keycolor)}
.dark-mode .series-chapterlist li{background:#3b3c4c;border-bottom:solid 1px #2f303e;}
.dark-mode .flexch-book, .dark-mode .flexch-dllink{background:#48495b;color:#eee;}
.dark-mode .series-chapterlist svg{color:#eee;}
.series-chapterlist li:hover{background:$(keycolor)e6;}
.ch-title{font-weight:normal;}
.ch-title span{font-weight:800;color:$(keycolor)}
.ch-title svg{width:20px;height:20px;vertical-align:middle;}
.flexch-infoz a:visited,.flexch > a:visited svg{color:red;}
.fit .header-background,.fit #disqus_thread,.fit footer{display:none;}
.fl-box{position:fixed;top:0;right:0;bottom:0;left:0;width:100%;height:100%;display:flex;align-items:center;justify-content:center;transition:all .2s ease;opacity:0;visibility:hidden;padding:5px;}
.dl-box{width:100%;max-width:500px;max-height:90%;display:flex;margin:0 auto -50%;background-color:white;border-radius:8px;transition:inherit;z-index:3;overflow:hidden;position:relative;box-shadow:0 10px 8px -8px rgb(0 0 0 / 12%);padding:10px;}
#allert .Text{position:fixed;top:0;right:0;bottom:0;left:0;width:100%;height:100%;display:flex;align-items:center;justify-content:center;transition:all .2s ease;opacity:0;visibility:hidden;padding:5px;}
#allert .widget-content{width:100%;max-width:500px;max-height:90%;margin:0 auto -50%;background-color:white;border-radius:8px;transition:inherit;z-index:3;position:relative;box-shadow:0 10px 8px -8px rgb(0 0 0 / 12%);}
.dark-mode .dl-box{background-color:#222}
#dl-module:checked ~ .fl-box{opacity:1;visibility:visible;background:rgba(0,0,0,.8);}
#dl-module:checked ~ .fl-box .dl-box{margin:0 auto;}
.mdl-close{z-index:1;padding:0;transform:rotate(45deg);}
.close{background:$(keycolor);border-radius:99rem;color:white;}
.fl-close{position:absolute;right:-.6rem;top:.1rem;min-width:3rem;z-index:1;padding:0;height:3rem;transform:rotate(45deg);}
.dl-box table{width:100%;}
.dl-box tbody{text-align:center;}
.dl-box td:first-child, .dl-box th:first-child{text-align:left;}
.dl-box td, .dl-box th{padding:.5rem;}
.dl-box .num{color:$(keycolor);font-weight:700;}
.dl-box .btn{font-size:.75rem;font-weight:700;padding:0 1.5rem;}
.btn{cursor:pointer;padding:.5rem 1.5rem;display:inline-block;vertical-align:top;text-align:center;line-height:2rem;width:auto;background-color:$(keycolor);color:var(--text);min-width:3rem;border:0;border-radius:5rem;}
#buttonDisqs {padding: .375rem 2.625rem;line-height: 1.5;background: $(keycolor);border-radius:$(border.radius);color: white;cursor: pointer;}
#scInput{width:100%;color:$(keycolor);font-family:inherit;padding:7px 10px;border:1px solid $(keycolor)70;border-radius:3px;background-color:$(keycolor)17;}
#myUL{display:flex;flex-wrap:wrap;gap:10px;line-height:1.5;max-height:300px;overflow-y:scroll;overflow-x:hidden;padding-right:5px;scrollbar-width:thin;}
#myUL li{display:flex;padding:5px 10px;border:1px solid $(keycolor)36;font-size:14px;border-radius:5px;flex:1 1 0;justify-content:space-between;min-width:20%;background:$(keycolor)1c;transition:.2s;flex-direction: column;}
#myUL span{display:block;}
@media (max-width: 550px){#myUL li {min-width: 50%}}
span.chapterdate{font-size:12px;color:#888;}
#myUL li:hover{background:$(keycolor);}
#myUL li:hover a{color:white;}
#myUL time {color: #888;font-size: 13px;}
#sidebar .LinkList ul{padding-left:15px;display:grid;grid-template-columns:repeat(3,auto);gap:10px;margin:0;font-size:14px;}
.image{width:100%;height:280px;background-position:center;}
.radio{display:none;}
.images,#homepage-slider{position:relative;}
.images-inner{overflow-x:auto;scroll-snap-type:x mandatory;scrollbar-width:none;scroll-behavior:smooth;}
.images-inner{align-content:center;display:grid;grid-template-columns:repeat(10, 100%);grid-gap:1em;}
.labels{position:absolute;right:15px;bottom:10px;}
.fake-radio{float:right;z-index:4;position:relative;}
#slide1:checked ~ div .fake-radio .radio-btn:nth-child(1),#slide2:checked ~ div .fake-radio .radio-btn:nth-child(2),#slide3:checked ~ div .fake-radio .radio-btn:nth-child(3){background:$(keycolor);}
.radio-btn{width:9px;height:9px;border-radius:5px;background:gray;display:inline-block !important;margin:0 1px;cursor:pointer;}
.bg::after{content:'';position:absolute;left:0;top:0;width:50%;height:100%;background:linear-gradient(to right,#000 0%,rgba(0,0,0,0) 100%);z-index:1;}
.slideinfo{max-width:1270px;margin:0 auto;position:relative;z-index:2;color:white;display:flex;height:100%;align-items:flex-end;padding:15px;}
.infolimit h3{font-size:23px;font-weight:normal;color:white;}
.infolimit{max-width:700px;padding-bottom:20px;}
.text{font-size:13px;}
.quality{display:inline-block;padding:2px 7px;background:#ffffff;color:#333;vertical-align:top;font-weight:700;font-size:11px;border-radius:2px;margin-right:10px;text-transform:uppercase;}
.gallery{padding:0;display:grid;grid-template-columns:repeat(10, 100vw);grid-template-rows:1fr;overflow:auto;height:280px;scroll-snap-type:both mandatory;margin:0;scrollbar-width:none;scroll-behavior:smooth;}
.swiper-pagination{position:absolute;right:20px;bottom:10px;z-index:20;display:flex;}
.swiper-pagination a{background:white;width:10px;height:10px;border-radius:99rem;padding:6px;margin:7px;}
@media (max-width:1024px){.gallery{height:180px;}
.infolimit p,.swiper-pagination a{display:none;}
}
.gallery::-webkit-scrollbar{display:none;}
.active{scroll-snap-type:unset;}
.gallery li{scroll-snap-align:center;display:inline-block;background-position:center;background-size:cover;position:relative;}
#Label3{max-width:1100px;margin:0 auto;}
#Label3 .cloud-label-widget-content{position:relative;padding:0 10px 0 10px;margin-top:-25px;z-index:4;overflow:hidden;box-shadow:0 2px 3px rgba(0,0,0,.1);}
#Label3 .cloud-label-widget-content .label-name{line-height:50px;color:white;text-transform:uppercase;padding:0 20px;display:inline-block;}
@media (max-width:1024px){#Label3 .cloud-label-widget-content{text-align:center;}
}
.label-more::after{content:attr(data-text);}
.label-more::after{flex-shrink:0;font-size:14px;margin-left:4px;color:white;}
.labelInput ~ .labelAll{transition:.3s ease-in-out;max-height:0;overflow:hidden;}
.labelInput:checked ~ .labelAll{max-height:100vh;margin-bottom:10px;}
.genres-list{float:left;width:100%;}
.genres-list a{width:150px;color:#fff;font-size:15px;cursor:pointer;max-width:100%;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;display:inline-block;}
.mySlides{display:none}
img{vertical-align:middle;}

.hotx .iconify{width:20px;height:20px;color:white;}
.colored .iconify{width:18px;height:18px;color:#222d34;}
.hotx{position:absolute;bottom:5px;right:5px;z-index:1;width:25px;text-align:center;background:#f44336;border-radius:99rem;height:25px;}
.colored{position:absolute;z-index:1;bottom:5px;left:5px;background:#ebcf04;color:rgba(0,0,0,.7);font-weight:700;font-size:10px;padding:2px 5px;border-radius:3px;text-transform:uppercase;display:flex;align-items:center;}
.m-GwWBFmbcL svg{width:16px;height:16px;color:$(keycolor);}
.dropdown{position:relative;}
.check-box {user-select: none;pointer-events: none;}
.dropMenu ~ ul{border-radius:6px;box-shadow:0 4px 4px rgba(0,0,0,.38);left:-5px;opacity:0;pointer-events:none;position:absolute;top:52px;user-select:none;padding:5px 0;min-width:240px;}
.p-y7x15-a a:hover{background:rgba(0,0,0,.32);color:white;transition:color .5s;}
.dropMenu a{padding:7px 15px;}
.dropMenu:checked ~ ul{animation:v-4fbac4e1 .25s;opacity:1;pointer-events:auto;user-select:auto;z-index:100;}
.dropdown ul::before{width:0;height:0;content:"";z-index:2;transform:scale(1.01);border-bottom:.6rem solid currentColor;border-left:.4rem solid transparent;border-right:.4rem solid transparent;bottom:100%;color:var(--v171);left:23%;position:absolute;}
@keyframes v-4fbac4e1{0%{opacity:0;transform:translateY(-15px) }
 60%{opacity:1 }
 to{transform:none }
}
.row{display:flex;justify-content:space-between;align-items:center;}
.entry{position:relative;transition:.15s;}
.entry .cover{display:none;max-width:0;min-width:0;padding:0;width:0;}
.entry > div{flex:2;padding:8px 10px;text-align:center;}
.entry .titles{flex:5;padding-left:15px;text-align:left;display:flex;align-items:center;}
.entry .titles{order:-1;}
.entry .titles a{transition:0s;margin-right:auto;}
.entry:hover .cover{display:block;}
.entry .cover .image{background-position:50%;background-repeat:no-repeat;background-size:cover;border-radius:3px;height:40px;width:40px;}
.entry:hover .cover .image{border-radius:3px;display:block;padding:0;position:absolute;top:-60px;width:140px;z-index:111;}
.entry:hover{background:$(keycolor);color:white;}
.entry:hover a{color:white}
.alert-warning{color:#856404;background-color:#fff3cd;border-color:#ffeeba;position:relative;padding:.75rem 1.25rem;margin-bottom:1rem;border:1px solid transparent;border-radius:.25rem;width:100%}
.pop-area::-webkit-scrollbar{display:none}
.pop-area{display:flex!important;width:100%;height:100%;position:fixed;top:0;left:0;background:rgb(0 0 0 / 51%);visibility:hidden;opacity:0;transition:all 0.25s ease-in-out;z-index:999999;overflow-y:scroll}
.pop-area.open{opacity:1;visibility:visible}
.pop-html{background:#fff;padding-bottom:10px;display:block;margin:auto auto;width:calc(100% - 20px);max-width:500px;visibility:hidden;opacity:0;overflow:hidden;transition:all 0.5s ease-in-out;transform:scale(.5);border-radius:7px;box-shadow:0 9px 46px 8px rgba(0,0,0,.14),0 11px 15px -7px rgba(0,0,0,.12),0 24px 38px 3px rgba(0,0,0,.2)}
.pop-area.open .pop-html{opacity:1;transform:scale(1);visibility:visible}
.head-pop{width:-webkit-fill-available;padding:12px 30px;overflow:hidden;background:$(keycolor)}
.close-btn{float:right;cursor:pointer;fill:#7e7e7e}
.body-content{padding:10px}
.text-center{display:grid;text-align:center;grid-gap:15px}
.text-center svg{margin:0 auto}
.btn.btn-outline-info{width:fit-content;margin:0 auto;text-decoration:none}
.table{width:100%;border:1px solid $(keycolor);border-radius:7px;margin:5px 0;padding:5px}
.table img{border-radius:4px;width:auto}
.table a{text-decoration:none}
.img-left{width:1px}
.span-spc{margin-top:3px;white-space:unset;color:#888;margin-bottom:5px;overflow:hidden;text-overflow:ellipsis;display:-webkit-box;-webkit-box-orient:vertical;-webkit-line-clamp:2;}
.item-left{vertical-align:-webkit-baseline-middle;padding-right:10px}
.btn-remove{cursor:pointer}
.show-bookmark{color:#fff;background-color:#007bff;position:relative;top:-20px;right:10px;font-size:50%;padding:.15em .3em;display:inline-block;padding:.25em .4em;font-size:75%;font-weight:700;line-height:1;text-align:center;white-space:nowrap;vertical-align:baseline;border-radius:50%;transition:color .15s ease-in-out,background-color .15s ease-in-out,border-color .15s ease-in-out,box-shadow .15s ease-in-out}
.hartomy-bookmark-btn,.btn-outline-info{position:relative;display:inline-block;box-sizing:border-box;border:none;border-radius:4px;padding:0 16px;width:100%;height:36px;vertical-align:middle;text-align:center;text-overflow:ellipsis;text-transform:uppercase;color:rgb(var(--pure-material-onprimary-rgb,255,255,255));box-shadow:0 3px 1px -2px rgba(0,0,0,0.2),0 2px 2px 0 rgba(0,0,0,0.14),0 1px 5px 0 rgba(0,0,0,0.12);font-family:var(--pure-material-font,"Roboto","Segoe UI",BlinkMacSystemFont,system-ui,-apple-system);font-size:14px;font-weight:500;line-height:36px;overflow:hidden;outline:none;cursor:pointer;transition:box-shadow 0.2s;margin-bottom:15px;}
.hartomy-bookmark-btn::-moz-focus-inner{border:none}
.hartomy-bookmark-btn svg{vertical-align:middle}
.buka-tutup{color:white;}
.dark-mode .body-content,.dark-mode .pop-html{background:#222;}
.dark-mode .table{border:1px solid #333;}
.myGrid .bookItem,.bookItem>a{position:relative;overflow:hidden}
.bookItem>.data>h2,.subItem li .chpName{overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.myGrid{display:grid;grid-template-columns:repeat(3,1fr)}
.myGrid .bookItem>a{float:left;height:141px;margin-right:10px;border-radius:3px}
.snippet-thumbnail {aspect-ratio: 3/4;}
.bookItem .snippet-thumbnail img{width:90px;height:auto;object-fit:cover;border-radius:$(border.radius);}
.myGridv2 .bookItem .snippet-thumbnail img {width:100%}
.bookItem>.data{overflow:hidden;line-height:21px;}
.bookItem>.data>h2{font-size:.98em;font-weight:500}
.myGrid .bookItem>.data>h2{margin:0;}
.myGridv2 .bookItem>.data>h2{margin:8px 0;}
.bookItem a{color:#333;text-decoration:none}
.bookItem>.data>.subItem{margin:10px 0 0;padding-left:15px}
.myGrid .bookItem {padding: 15px 10px;}
.bookItem:last-child {border-bottom: none}
.subItem li{margin-bottom:5px;font-size:13px}
.myGrid .subItem li .chpName{float:left;max-width:80px}
.myGrid .subItem li .chpDate{float:right;color:#999;font-size:12px}
.snippet-thumbnail{overflow:hidden;position:relative;}
.myGridv2{display:grid;grid-template-columns:repeat(auto-fill,minmax(141px,1fr));gap:20px;padding:15px;}
.myGridv2 .bb-1pxsf{border-bottom:none;}
.myGridv2 .new-tag{display:none;}
.myGridv2 .bookItem > .data > .subItem{padding-left:0;list-style:none;margin:0;}
.myGridv2 .char{display:flex;align-items:center;justify-content:space-between;}
.myGridv2 .chpName{padding:0 7px;background:$(keycolor)2e;border-radius:10px;}
@media screen and (max-width:1080px){.myGrid{grid-template-columns:repeat(3,1fr)}
}
@media screen and (max-width:500px){.myGrid{grid-template-columns:repeat(1,1fr)}
}
.po{bottom:4px;right:4px;background:gray;padding:0 6px;font-size:13px;border-radius:4px;color:white;}
.manga {background:#ff0038;}
.manhua {background:#007fff;}
.manhwa {background:#006b3c;}
.myGridv2 .bookItem > a{position:unset;}

.dark-mode .bookItem a{color:#ccc}
.nav-a a,.nav-a label{color:rgba(255,255,255,.6);font-weight:500;}
.subItem li .chpName a:visited,#myUL a:visited{color:$(keycolor)}
.nav-a a:hover,.nav-a label:hover{color:#fff;}
.nav-a a::after,.nav-a label::after{content:'';display:block;width:0;height:2px;z-index:1;position:relative;background:white;transition:0.3s;}
.nav-a a:hover::after,.nav-a label:hover::after{width:100%;transition:0.3s;}
.dark-mode #sidebar ul.genre::before,.dark-mode #sidebar ul.genre::after{background:#333}
#notification{background-color:$(keycolor);color:white;}
#notification .widget-content{padding:7px;}
.tab{overflow:hidden;background-color:#f1f1f1;}
.dark-mode .tab{background-color:#333}
.tab li{background-color:inherit;float:left;border:none;outline:none;cursor:pointer;padding:4px;transition:0.3s;font-size:14px;width:20%}
.dark-mode .tab li{color:#ccc}
.tab li:hover{background-color:#ddd;}
.dark-mode .tab li:hover{background-color:$(keycolor)4a;}
.tab li.active{background-color:$(keycolor);color:white;}
@media only screen and (max-width:590px){.tab li:nth-child(n+4){display:none;}
 .tab li{width:33.3%}
}
#recommendations .widget{display:none;}
#recommendations .widget{padding:10px 0;}
.jp{background-image:url(https://blogger.googleusercontent.com/img/a/AVvXsEgy78vVijPJfAhiDZibEiink5MdFFe99hZw8-rVzqfgJXqeTclaiQCcjxEN-37ZZSqllxyfOkQATOqQW6-RDHw15lj5v7jJCfmfCtkbKqeiRWpl_7hqU6EbwIDNiG9xQkMr3WegbTmCjmoV3KeVsuz5_wSLCg_XPSHvfhdFh3_gPO6w6qAJuWblIL4rWQ=s50);}
.cn{background-image:url(https://blogger.googleusercontent.com/img/a/AVvXsEh7o3WESCpE9G2NSiDpLhD6_N9WYQBJ74JJHavvaQVGBwgIV6D4zL8l4sguDSqkFqhzsOfBq0y1NmE3tEF9A6Y_4BwqBD6DTI9BIZ-UL58sQyEMyDPRGoW9Y-iSmr4t3BxpOgMkxJDEBfMRGdHAucprfhrPC8Pc4ZtC-xY3zuabK7nY39w6seW4GOv7Hw=s50);}
.kr{background-image:url(https://blogger.googleusercontent.com/img/a/AVvXsEi18s6Wr5BOAC7-G2x7GLPX7aEOIoqLCbiU3YAslN0a7J8Jz2OMe0OhGHMgM9g3WeM9rQHP3Qz-u4ooyiOwyRTGznCktu_EJfTMqj_y2GVYwThGNKTLAKs_o_1RjLL3yEUNlQiazeCXruPpY0nS2xudxDeV_VJIYosrC9pwwzDTehjVtJ5F9eb8zy9WpQ=s50);}
#chapterSelect{background:#333;border:1px solid #333;font-family:inherit;display:block;color:#9b9b9b;padding:3px 10px;border-radius:20px;font-size:13px;max-width: 150px;}
.nextPrev a{padding:3px 15px;border-radius:20px;color:#fff;font-size:13px;background:$(keycolor);}
.nextPrev svg{width:18px;height:18px;}
#ecNext a{padding-right:8px;}
#ecPrev a{padding-left:8px;}
.progress-custom{display:flex;align-items:center;background:;}
.progress{display:flex;height:1rem;overflow:hidden;font-size:0.75rem;background-color:;border-radius:0.25rem;height:1rem;font-size:0.6em;flex:1;position:relative;}
.progress-bar{display:flex;flex-direction:column;justify-content:center;overflow:hidden;color:#fff;text-align:center;white-space:nowrap;transition:width 0.6s ease;overflow:hidden;background:linear-gradient(to right, $(keycolor), $(secclr));padding-right:calc(100% - var(--width));width:100%;height:100%;-webkit-clip-path:inset(0 calc(100% - var(--width)) 0 0);clip-path:inset(0 calc(100% - var(--width)) 0 0);}
.progress-custom .progress-value{font-size:0.8em;padding:0 0.5em;}
div#ec_Select { visibility: hidden;user-select: none;pointer-events: none;width: 0;}

/* Random Post Multi Tab Dagruel */ 
.series-gen ul.nav-tabs{display:flex;list-style:none;margin:0;padding:6px;overflow:hidden;}
.series-gen ul.nav-tabs li{flex:1;cursor:pointer;text-align: center;}
.customAF.scroll{display:none;position:relative;padding:5px 10px;}
.customAF.scroll.active{display:block;}
.customAF.scroll .scrollButton{display:inline-block;position:absolute;top:calc(50% - 63px);z-index:3;background:#303030;transition:.3s;padding:30px 10px;outline:0;border:none;cursor:pointer;opacity:0;}
.customAF.scroll:hover .scrollButton{opacity:.9;}
.customAF.scroll .scrollButton:hover{background:#3b3b3b;opacity:1;}
.scrollButton.left{left:10px;}
.scrollButton.right{right:10px;}
.scrollButton svg{width:24px;height:24px;vertical-align:middle;}
.scrollButton svg path{fill:#fff;}
.customAF .inner{display:-webkit-box;display:-webkit-flex;display:-moz-box;display:-ms-flexbox;display:flex;flex-wrap:wrap;padding:5px 5px 0;width:calc(100% - 10px);}
.customAF .inner.scrolling{display:grid;gap:20px;grid-template-columns:repeat(auto-fill,minmax(142px,1fr));overflow-x:hidden;scroll-behavior:smooth;padding:0;width:100%;}
.customAF .inner .customAgata{float:left;width:calc(20% - 10px);padding:0 5px;margin-bottom:10px;}
.customAF .inner.scrolling .customAgata{float:none;width:auto!important;padding:0;margin:0;}
.customAgata .images{position:relative;}
.customAF .inner .customAgata .images figure{position:relative;margin:0;padding-top:142%;border-radius:3px;overflow:hidden;}
.customAgata .images figure:after,.customAgata .images figure:before{content:'';}
.customAgata .images figure img,.customAgata .images figure:after,.customAgata .images figure:before{position:absolute;left:0;right:0;bottom:0;top:0;}
.customAgata .images figure:before{margin:auto;width:3rem;height:3rem;line-height:3rem;text-align:center;font-size:1.5rem;z-index:2;transform:scale(0);background-repeat:no-repeat;background-position:center;background-size:50px;background-image:url('data:image/svg+xml,%3Csvg xmlns="http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg" width="1em" height="1em" preserveAspectRatio="xMidYMid meet" viewBox="0 0 1024 1024"%3E%3Cpath fill="white" d="M928 161H699.2c-49.1 0-97.1 14.1-138.4 40.7L512 233l-48.8-31.3A255.2 255.2 0 0 0 324.8 161H96c-17.7 0-32 14.3-32 32v568c0 17.7 14.3 32 32 32h228.8c49.1 0 97.1 14.1 138.4 40.7l44.4 28.6c1.3.8 2.8 1.3 4.3 1.3s3-.4 4.3-1.3l44.4-28.6C602 807.1 650.1 793 699.2 793H928c17.7 0 32-14.3 32-32V193c0-17.7-14.3-32-32-32zM324.8 721H136V233h188.8c35.4 0 69.8 10.1 99.5 29.2l48.8 31.3l6.9 4.5v462c-47.6-25.6-100.8-39-155.2-39zm563.2 0H699.2c-54.4 0-107.6 13.4-155.2 39V298l6.9-4.5l48.8-31.3c29.7-19.1 64.1-29.2 99.5-29.2H888v488zM396.9 361H211.1c-3.9 0-7.1 3.4-7.1 7.5v45c0 4.1 3.2 7.5 7.1 7.5h185.7c3.9 0 7.1-3.4 7.1-7.5v-45c.1-4.1-3.1-7.5-7-7.5zm223.1 7.5v45c0 4.1 3.2 7.5 7.1 7.5h185.7c3.9 0 7.1-3.4 7.1-7.5v-45c0-4.1-3.2-7.5-7.1-7.5H627.1c-3.9 0-7.1 3.4-7.1 7.5zM396.9 501H211.1c-3.9 0-7.1 3.4-7.1 7.5v45c0 4.1 3.2 7.5 7.1 7.5h185.7c3.9 0 7.1-3.4 7.1-7.5v-45c.1-4.1-3.1-7.5-7-7.5zm416 0H627.1c-3.9 0-7.1 3.4-7.1 7.5v45c0 4.1 3.2 7.5 7.1 7.5h185.7c3.9 0 7.1-3.4 7.1-7.5v-45c.1-4.1-3.1-7.5-7-7.5z"%2F%3E%3C%2Fsvg%3E');transition:transform .2s ease-out;}
.customAgata:hover .images figure:before{opacity:1;transform:scale(1);}
.customAgata .images figure img{object-fit:cover;}
.customAgata .images figure img,.customAgata .images figure:after{width:100%;height:100%;}
.customAgata .images figure:after{border-radius:3px;background-color:#263238;opacity:0;transition:opacity .2s ease-out;}
.customAgata:hover .images figure:after{opacity:.5;}
.customAgata .entry-title{font-size:.95em;margin:8px 0;margin-bottom:8px;margin-bottom:5px;font-weight:500;line-height:19px;text-align:left;overflow:hidden;text-overflow:ellipsis;display:-webkit-box;-webkit-box-orient:vertical;-webkit-line-clamp:2;}
@media screen and (min-width:1120px){.customAF.scroll .scrollButton {display: none;}}
@media screen and (max-width:1120px){.customAF .inner .customAgata{width:calc(25% - 10px);}}
@media screen and (max-width:768px){.customAF .inner .customAgata{width:calc(33.333333% - 10px);}}
@media screen and (max-width:544px){.customAF .inner .customAgata{width:calc(50% - 10px);}}
.customAF .inner.scrolling::-webkit-scrollbar{display:none;}
.scrollButton.left{border-radius:0 0.25rem 0.25rem 0;}
.scrollButton.right{border-radius:0.25rem 0 0 0.25rem;}
.series-gen .title svg{vertical-align:middle;margin-left:10px;transition:.5s;}
.head svg {transition: .5s}
.head:hover svg{transform:rotate(180deg);transition:.5s;}
@media screen and (min-width:1279px){.gta-ms{grid-template-columns:1fr minmax(200px,330px);gap:1.3rem;}}



/* Search Filter */
.BlogSearch input[type=checkbox]:not(.simple,.hidden){position:relative;-webkit-appearance:none;width:12px;height:18px;border:1px solid #DDD;border-radius:5px;-webkit-transition:.4s;transition:.15s;vertical-align:-25%;display:inline-block;cursor:pointer;outline:0;margin: 0;}
.dark-mode .BlogSearch input[type=checkbox]:not(.simple,.hidden){border-color:#666}
input[type=checkbox]:not(.simple,.hidden):after{content: url('https://api.iconify.design/bi/check.svg?color=%23ddd');position:absolute;top:0;left:0;bottom:3px;transition:.15s;}
.BlogSearch input[type=checkbox]:not(.simple):checked{background:$(keycolor);}
.BlogSearch input[type=checkbox]:not(.simple):checked:after{transition:.15s;}
.BlogSearch input[type=checkbox]:not(.simple).nocolor:checked{background-color:var(--primary);}
.filters button[type="submit"]{color:#fff;transition:all .15s;width:100%;border:1px solid var(--primary-color);background:var(--primary-color);border-radius:.25rem;}
.filters button{font-size:13px;font-weight:400;padding: 3px 6px;}
.filters button[type="submit"]:hover{filter:brightness(90%);}
.filters .searchf{padding:0 15px;margin-left:0;margin-right:0;margin-bottom:8px;}
.filters input:focus,.filters input:hover{color:#d5d5d5;border-color:#404040;}
.filters input{padding:0 8px;border:1px solid #363636;transition:all .15s;width:100%;background:0 0;color:#666;height:30px;border-radius:.25rem;}
.filters{counter-reset:checked;}
.filters input:checked{counter-increment:checked;}
.filters .dropdown-menu li input:checked ~ label {color:$(keycolor);}
.filters .dropdown-menu li label{color:#666;line-height:23px;padding-left:2px;background:0 0!important;border-radius:2px;cursor: pointer;}
.dropdown-menu {scrollbar-width: thin;}
.count:after{content:counter(checked);}
.filters svg{height:15px;}
.filter{position:relative;}
.dropdown-toggle{width:100%;border:1px solid #efefef;outline:0;line-height:25px;border-radius:.25rem;background:#efefef;font-size:.85em;color:#666;display:block;}
.dark-mode .dropdown-toggle{border:1px solid #262626;background:#262626;color:#ccc;}
.dropdown-toggle .value{color:var(--primary-color);}
.dropdown-menu{position:absolute;top:100%;right:0;z-index:1000;float:left;width:100%;margin:.125rem 0 0;font-size:.94rem;color:#aaa;text-align:left;list-style:none;background-color:#fff;background-clip:padding-box;border:1px solid rgba(0,0,0,.15);border-radius:.25rem;opacity:0;user-select:none;pointer-events:none;}
.filters .dropdown-menu{background:#fff;box-shadow:0 6px 12px rgba(0,0,0,.175);padding:10px;margin-top:1px;font-size:.9em;overflow: hidden;}
.c4:hover {overflow-y: scroll;}
.dark-mode .filters .dropdown-menu{background:#212121;box-shadow:0 6px 12px rgba(0,0,0,.175);}
.filters .dropdown-menu.c4{width:500px;}
.filters .opt{display:grid;grid-template-columns:1fr 1fr;padding:15px;gap:8px;}
.filters .dropdown-toggle{transition:all .15s;padding:0 10px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;display:block;text-align:center;cursor:pointer;color:#2f2f2f;}
@media screen and (min-width:1280px){.filters .dropdown-menu.lg{max-height:240px;}}
@media screen and (max-width:576px){.filters .dropdown-menu.lg{width:300px;}}
@media only screen and (max-width: 900px){.dropdown-menu{right: 0;left: 0;max-width: unset}}
.hidden{display:none;}
#Genre:checked ~ ul,#Status:checked ~ ul,#Type:checked ~ ul,#Lang:checked ~ ul,#Country:checked ~ ul,#Quality:checked ~ ul{opacity:1;user-select:auto;pointer-events:auto;}
.opt > div:nth-child(2n) .dropdown-menu{left:auto;right:0;}
.filters .dropdown-toggle:hover{background:#d0d0d0;border-color:#d0d0d0;}
.dark-mode .filters .dropdown-toggle:hover{background:#2d2d2d;border-color:#2d2d2d;}
.dark-mode .filters .dropdown-toggle {color:#666}
.chk:checked ~ [for]{background:var(--primary-color);color:white;}
.chk:checked ~ .dropdown-toggle .value{color:white;}
.dropdown-menu{display:grid;gap:5px;}
.c4{grid-template-columns:repeat(auto-fill,minmax(100px,1fr));}
#sidebar .widget {overflow: unset;}
#close,.mystyle #submit {
  display: none;
}
.mystyle #close {
  display: flex;
}
.mystyle {
  position: absolute;
  left: 5px;
  right: 5px;
  border-radius: 5px;
  width: auto;
  background: #17151b;
  padding: 4px;
  margin-right: 0;
	display:flex !important; 
}

    /* Star Rating Css by Wolv Themes */

.starRating .p{background:#fefefe; padding-left:5px;width:160px; border:1px solid #eceff1;border-radius:10px;
position: relative; top:20px;margin-top:-45px;text-transform: uppercase;}     .darkMode .starRating .p{background:#232323;}    
 /* Product Rating */
.rating-produk i.icon-star-angka{font-weight:400;font-size:12px;margin-left:5px;vertical-align:1px}
.rating-produk{padding:0;width:55%;float:left;box-sizing:border-box;margin-top:10px}
b.widget-rating{display:block;margin-bottom:10px}
i.icon-star,.icon-star{font-weight:400;font-style:normal;display:inline-block}
i.icon-star:before,.icon-star:before{content:&#39;&#39;;width:17px;height:17px;display:inline-block;margin:-2px;transition:all .3s ease;background:url(&quot;data:image/svg+xml,%3Csvg viewBox=&#39;0 0 24 24&#39; xmlns=&#39;http://www.w3.org/2000/svg&#39;%3E%3Cpath d=&#39;M12,17.27L18.18,21L16.54,13.97L22,9.24L14.81,8.62L12,2L9.19,8.62L2,9.24L7.45,13.97L5.82,21L12,17.27Z&#39; fill=&#39;%23ffc53e&#39;/%3E%3C/svg%3E&quot;) no-repeat}
i.icon-star.silver:before,i.icon-star.silver:before{content:&#39;&#39;;width:17px;height:17px;display:inline-block;margin:-2px;transition:all .3s ease;background:url(&quot;data:image/svg+xml,%3Csvg viewBox=&#39;0 0 24 24&#39; xmlns=&#39;http://www.w3.org/2000/svg&#39;%3E%3Cpath d=&#39;M12,17.27L18.18,21L16.54,13.97L22,9.24L14.81,8.62L12,2L9.19,8.62L2,9.24L7.45,13.97L5.82,21L12,17.27Z&#39; fill=&#39;%23a9acad&#39;/%3E%3C/svg%3E&quot;) no-repeat}

.check-box img{opacity:1;transition:opacity 1s}
.check-box img[data-src]{opacity:0}

.menu-item{display:flex;place-content:center;color:white;background-color:rgba(0,0,0,.4);padding:4px 10px;border-radius:5px;}
.shwx{position:absolute;top:53px;left:0;width:100%;background:#222;z-index:3;height:100%;display:block!important;}
.shwx ul{margin:20px;}
#PageList1.shwx li{border-bottom:none;}
  
   /* Post Comment */
#comments {grid-area: a4;}
#showComments, #disqus_thread{margin-top:30px;text-align:center;}
#showComments:target, #showComments + #comments{display:none} #showComments:target + #comments{display:block}
.show-comment a, .comment-add .comment-reply{display:block;padding:18px 20px;border:1px solid #505050;border-radius:5px;font-size:13px;color:#505050;text-align:center}
.comment-add .comment-reply.hidden{display:none}
.show-comment a:hover, .comment-add .comment-reply:hover{border-color:#989b9f;color:#989b9f}
.comments{margin-top:30px}
.comments .comment-disable{text-align:center}
.comments ol, .comments ul{list-style:none;margin:0;padding:0}
.comments li{position:relative;padding:15px 20px;border-radius:$(border.radius);background-color:rgba(255,255,255,.7);box-shadow:0 4px 12px 0 rgba(9,32,76,.05)}
.comments li{margin-bottom:15px}
.comments li a{color:inherit}
.comments li .avatar-image-container{display:flex;align-items:center;position:absolute;width:40px;height:40px;border-radius:50%;overflow:hidden;background:#ebeced url("data:image/svg+xml,") center / 18px no-repeat;transition:all .2s ease-out;-webkit-transition:all .2s ease-out}
.comments li .avatar-image-container img{margin:auto;width:40px}
.comments li .comment-header{display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;height:40px;margin:0 0 20px 50px;padding:3px 0}
.comments li .comment-header .datetime{width:100%;font-size:11px;color:#989b9f}
.comments li .comment-header .datetime a{color:inherit}
.comments li .comment-header .user{flex:0 0 auto;display:flex;align-items:flex-start;font-size:13px;font-weight:700;font-family:'Nunito Sans', sans-serif;color:#161617}
.comments li .comment-header .user span{overflow:hidden;text-overflow:ellipsis;white-space:nowrap;max-width:130px}
.comments li .comment-header .user svg{width:16px;height:16px;fill:#519bd6;margin:0 0 0 5px}
.comments li .comment-header .user .blog-author{display: block;background-color: #e4e6eb;margin-left: 5px;border-radius: 4px;font-size: 11px;padding-left: 4px;padding-right: 4px;font-weight: 600;color: #65676b;}
.comments li .comment-actions, .comments li .comment-replies .comment-reply{margin:10px 0 0 auto;font-size:13px}
.comments li .comment-replies + .comment-actions{display:none}
.comments li .comment-replies{margin:10px 0 0 auto}
.comments li .comment-replies .thread-toggle,
.comments li .comment-replies .comment-reply a, .comments li .comment-actions a{display:inline-flex;align-items:center;font-size:13px;}
.comments li .comment-replies .thread-toggle svg, .comments li .comment-replies .comment-reply svg, .comments li .comment-actions svg{width:14px;height:14px;margin-right:5px;stroke:#505050}
.comments li .comment-replies .thread-show:checked + .comment-thread .thread-toggle svg{-webkit-transform:rotate(180deg);transform:rotate(180deg)}
.comments li .comment-replies .thread-show:checked + .comment-thread .thread-chrome,
.comments li .comment-replies .thread-show:checked + .comment-thread + .comment-reply{display:none}
.comments li .comment-replies .thread-chrome{margin-top:20px}
.comments li .comment-replies .comment-reply{width:calc(100% - 55px);display:flex;align-items:center;}
.comments li .comment-replybox-single{margin-top:20px}
.comments li li{display:flex;align-items:flex-start;flex-wrap:wrap;padding:0;background-color:transparent;box-shadow:none}
.comments li li:not(:last-child){margin-bottom:10px}
.comments li li .avatar-image-container{width:32px;height:32px}
.comments li li .comment-block{width:calc(100% - 40px);margin-left:auto;padding:0 15px 15px;background-color:#f7f9f8;border-radius:15px}
.comments li li .comment-header{height:initial;margin:0 0 10px;padding:0}
.comments li li .comment-header .datetime{width:initial}
.dark-mode .comments li {background: #222;}
.dark-mode .comments li .comment-header .user {color: white;}
  

	/* Comment Sorting*/
.cmAl:checked ~ div .s::before{content:attr(data-new);}
.s::before{content:attr(data-text);margin:0 6px;opacity:.7;font-size:90%;}
.s::after{content:'\296E';line-height:18px;font-size:17px;}
.cmAl:checked ~ div .s::before{content:attr(data-new);}
.comments-content > ol{display:flex;flex-direction:column;}
.cmAl:checked + * + div > ol{flex-direction:column-reverse;}
.s{cursor:pointer;}

/* Chapter List Dengan Tombol Download Blogger Dagruel */

@import url(https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css);
.bxcl a{color:#222d34;text-decoration:none}.dark-mode .bxcl a{color:#ccc;}.bixbox *{box-sizing:border-box}.pv .releases{position:relative;display:flex;justify-content:space-between;align-items:baseline;border-bottom:1px solid #312f40;padding:8px 15px}.releases:after{position:absolute;left:0;bottom:0;right:auto;top:auto;height:1px;width:100%;background-color:transparent;display:block;z-index:1;transform:scaleY(.5);opacity:.8;background-image:linear-gradient(90deg,rgba(0,0,0,.01) 0,rgba(0,0,0,.1) 10%,rgba(0,0,0,.2) 20%,rgba(0,0,0,.3) 30%,rgba(0,0,0,.3) 70%,rgba(0,0,0,.2) 80%,rgba(0,0,0,.1) 90%,rgba(0,0,0,.01) 100%)}.releases h2{font-size:15px;color:#fff;line-height:20px;font-weight:500;margin:0;position:relative}.lastend{display: flex;gap: 5px;overflow:hidden;position:relative;}.lastend .inepcx{width:50%;float:left;text-align:center}.lastend .inepcx[data-id="2"]{float:right}.lastend .inepcx a{display:block;color:#fff;margin-top:10px;padding:15px;background:#0c70de;border-radius:5px;line-height:normal}.lastend .inepcx a span{display:block;font-size:15px}.lastend .inepcx a span.epcur{font-size:20px;margin-top:6px;font-weight:700}.lastend .inepcx a:hover{background:#333}.bxcl{overflow:hidden}.bxcl ul{padding:0;list-style:none;overflow:auto;max-height:297px}.bxcl ul li{float:left;width:25%}.bxcl ul li .chbox{overflow:hidden;padding:5px 10px;border:1px solid $(keycolor)36;font-size:14px;margin:0 5px;margin-bottom:10px;position:relative;border-radius:5px}.bxcl ul li .chbox:hover{background:$(keycolor)1c}.bxcl ul::-webkit-scrollbar-thumb{background:#0c70de}.bxcl ul::-webkit-scrollbar-track{background:0 0}.bxcl ul::-webkit-scrollbar{width:5px}.bxcl ul li .eph-num{float:left}.bxcl ul li .dt{float:right;font-size:20px;margin-top:8px;margin-right:5px}.bxcl ul li .eph-num span{display:block}.bxcl ul li .eph-num span.chapternum{font-weight:400}.bxcl ul li .eph-num span.chapterdate{font-size:12px;color:#888}.bxcl ul li .eph-num a:visited{color:#0c70de}.bxcl ul li .dt a{color:#0c70de}.bxcl ul li .dt a:hover{color:#fff}@media only screen and (max-width:950px){.bxcl ul li{width:33.3333333%}}@media only screen and (max-width:800px){.bixbox{border-radius:0;margin-bottom:5px}}@media only screen and (max-width:570px){.bxcl ul li{width:50%}}@media only screen and (max-width:320px){.bxcl ul li{width:auto;float:none}}.lightmode .quickfilter .filters .filter ul li input:not(:checked)+label:before{background-color:#ddd}.bxcl ul::-webkit-scrollbar-thumb,.lastend .inepcx a{background:$(keycolor)}.bxcl ul li .dt a,.bxcl ul li .eph-num a:visited,a:hover{color:$(keycolor)}


/* Slider */
#slider{position:relative;}
#left-button,#right-button{padding:15px 0;}
#left-button{position:absolute;top:50%;left:0;transform:translate(0,-50%);background:$(keycolor)b5;border-radius:0 8px 8px 0;cursor:pointer;z-index: 2;}
#right-button{position:absolute;top:50%;right:0;transform:translate(0,-50%);background:$(keycolor)b5;border-radius:8px 0 0 8px;cursor:pointer;z-index: 2;}
#right-button svg,#left-button svg{stroke:white;width:36px;height:36px;position:relative;top:3px;}
#right-button,#left-button{display:none;}
#slider:hover #right-button,#slider:hover #left-button{display:block;}
.item{min-width:100%;height:280px;scroll-snap-align:start;overflow:hidden;background-size:cover;background-position:center;}
#slides{display:flex;overflow:hidden;scroll-behavior:smooth;scroll-snap-type:x mandatory;}
.mainslider{position:relative;overflow:hidden}
.mainslider::before{position:absolute;top:0;left:0;z-index:2;display:block;width:100%;height:100%;background:rgb(0 0 0 / 18%);content:"";}
.mainslider .limit{position:relative;background:#222;overflow:hidden;height:280px;}
.mainslider .limit::before{position:absolute;bottom:0;display:block;width:100%;height:25%;content:"";background-color:rgba(255,255,255,0);background-image:-webkit-gradient(linear,left top,left bottom,from(rgba(255,255,255,0)),to(#1e2129));background-image:-webkit-linear-gradient(top,rgb(255 255 255 / 0%),#1e2129);background-image:-moz-linear-gradient(top,rgba(255,255,255,0),#1e2129);background-image:-ms-linear-gradient(top,rgba(255,255,255,0),#1e2129);background-image:-o-linear-gradient(top,rgba(255,255,255,0),#1e2129);background-image:linear-gradient(top,rgba(255,255,255,0),#1e2129);filter:progid:DXImageTransform.Microsoft.gradient(startColorStr='rgba(255,255,255,0)',endColorStr='#1e2129');z-index:3;}
.mainslider .limit .sliderinfo{position:absolute;bottom:10%;z-index:2;width:100%;font-family:'Roboto',sans-serif;}
.mainslider .limit .sliderinfo .sliderinfolimit{max-width:1200px;margin:0 auto;padding:0 15px;}
.mainslider .limit .bigbanner{background-position:50% 35%;background-repeat:no-repeat;background-size:cover;min-height:280px;}
.mainslider .limit .sliderinfo .sliderinfolimit span.name{color:#FFF;font-weight:300;font-size:23px;margin-bottom:10px;display:block;max-width:700px;line-height:normal;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;}
.mainslider .limit .sliderinfo .sliderinfolimit .meta{margin-bottom:8px;box-shadow:none;}
.mainslider .limit .sliderinfo .sliderinfolimit .desc{color:#ddd;max-width:520px;overflow:hidden;line-height:19px;font-size:13px;font-weight:300;}
.bookmarked,.menu-item:hover {filter: hue-rotate(100deg);}
.black-bg{padding:10px;background:rgba(0,0,0,0.7);border-radius:8px;max-width:700px;color:$(keycolor);}


#nPL{display:flex;justify-content:space-between;margin-bottom:20px;}
#nPL,#nPL2{padding:5px;direction: ltr;}
#nPL_select{background:#333;border:1px solid #333;font-family:inherit;display:block;color:#9b9b9b;padding:5px 10px;padding-right:25px;border-radius:20px;font-size:13px;-webkit-appearance:none;max-width:160px;}
.inner_nPL,.inner_nPL li{list-style-type:none;margin:0;padding:0;}
.inner_nPL{display:flex;align-items:center;margin-top:10px;}
.inner_nPL li{flex:1;text-align:center;}
.inner_nPL li a{display:block;color:#fff;padding:5px;text-decoration:none;background-color:#00008b;border-radius:5px;}
.inner_nPL a{margin-left:5px;background-color:$(keycolor);}
.inner_nPL a{margin-right:5px;background-color:$(keycolor);}
.inner_nPL a{display:block;padding:2px 15px;border-radius:20px;color:#FFF;font-size:13px;line-height:25px;}
.inner_nPL li a:before,.inner_nPL li.next a:after{content:'';display:inline-block;min-width:20px;min-height:20px;background:url("data:image/svg+xml,%3Csvg viewBox='0 0 24 24'xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M3,6H21V8H3V6M3,11H21V13H3V11M3,16H21V18H3V16Z'fill='%23fff'/%3E%3C/svg%3E");background-position:center;background-repeat:no-repeat;vertical-align:middle}
.inner_nPL li.prev a:before{background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 24 24'xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M15.41,16.58L10.83,12L15.41,7.41L14,6L8,12L14,18L15.41,16.58Z'fill='%23fff'/%3E%3C/svg%3E")}
.inner_nPL li.next a:before{content:none}
.inner_nPL li.next a:after{background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 24 24'xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M8.59,16.58L13.17,12L8.59,7.41L10,6L16,12L10,18L8.59,16.58Z'fill='%23fff'/%3E%3C/svg%3E")}
.inner_nPL li span{vertical-align:middle}
.inner_nPL .dlx {background: #d50f00;}
.chpName a .new-tag{color:green;margin-left:5px;font-size:10px;background-color:green;color:white;border-radius:3px;padding:0 3px;}
.chpName a:visited .new-tag{color:white;background-color:white;}
.dark-mode .chpName a:visited .new-tag{color:#222222;background-color:#222222;}
.char:hover .new-tag{color:$(keycolor)1c;background-color:$(keycolor)1c;}

/* Scroll To Top */
#scTop{display:none;position:fixed;bottom:20px;right:25px;z-index:99;font-size:18px;border:none;outline:none;background-color:$(keycolor);color:white;cursor:pointer;padding:5px;border-radius:$(border.radius);width: 33px;height: 33px;}
#scTop:hover{background-color:#555;}

/* Reading History */
.widget-history ul{list-style:none;padding:0;margin:0;}
.widget-history li{padding:0;border-bottom:1px solid  rgb(236,236,236);}
.widget-history a{padding:7px 15px;display:block;line-height:20px;transition:.2s linear;font-size:13px;}
.widget-history li:hover a{color:white;}
.widget-history li:hover{background-color:$(keycolor);transition:.2s linear;}
.dark-mode .widget-history li{border-bottom-color:#333;}
.widget-history li:last-child{border-bottom:none;}

/* Social Footer */
.socialbutton a .fab,.socialbutton a .fas{line-height:28px;}
.socialbutton a{display:inline-block;margin:0 2px;font-size:15px;color:rgba(255,255,255,.7);background:#2e2e2e;border-radius:5px;width:30px;border:1px solid #4b4b4b;}
.socialbutton a.scfb:hover{background:#1877f2!important;border-color:#1877f2!important;color:#FFF!important;}
.socialbutton a.scig:hover{background:linear-gradient(45deg,#405de6,#5851db,#833ab4,#c13584,#e1306c,#fd1d1d)!important;color:#FFF!important;border:0;}
.socialbutton a.scdc:hover{background-color:#7289da;border:0;}

/* Social Footer */
#character ul{display:grid;gap:10px;list-style:none;padding-left:0;}
#character img{width:45px;height:45px;object-fit:cover;border-radius:50%;}
#character li{display:grid;grid-template-columns:50px auto;gap:10px;align-items:center;}
#character span{color:#999;font-size:.8rem;}


@media only screen and (max-width:600px){#nPL{flex-direction:column;align-items:center;}#nPL > div{width:100%;}#nPL_select{width:100%;max-width:100%;}.inner_nPL > a{width:100%;}}
@media only screen and (max-width:350px){.inner_nPL{display:grid;gap:10px;grid-template-columns:repeat(2,1fr);}#dl{grid-column:1/3;}}
  @media only screen and (max-width: 600px)
.customAF.scroll .scrollButton {
  display: none;
}

.m-10{margin:10px;}
#sidebar .active{background-color:$(keycolor);color:white;}
#popular .PopularPosts {display: none}
#popular .PopularPosts.current {display: block} .distbtr{opacity:0}


 ]]></b:skin>

    <b:template-skin>
      <![CDATA[
body#layout section {width: 100%}
body#layout main {display: flex}

body#layout header div.section h4 {display: none;}
body#layout header div.section {display: flex;flex-wrap: wrap;}
body#layout header div.section .widget {flex: 1;}
      ]]>
    </b:template-skin>
    <b:defaultmarkups>
      <b:defaultmarkup type='Common'>
        <b:includable id='relatedPost' var='post'>
          <div class='bc-fff r2 s1 a3 oh'>
            <h2 class='c-theme m-0 bb-1pxsf y9x19p fs-15 flex aic jcsb'><span class='flex aic'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><g fill='none'><path d='M10 2H2v8h3v12h2V10h3v2h2v2h2v8h8v-8h-8v-2h-2v-2h-2V2zM4 8V4h4v4H4zm12 12v-4h4v4h-4z' fill='currentColor'/></g></svg>Rekomendasi</span><div class='flex aic wh-18-svg gg-10'>
                                <div id='prev'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><path d='M4.431 12.822l13 9A1 1 0 0 0 19 21V3a1 1 0 0 0-1.569-.823l-13 9a1.003 1.003 0 0 0 0 1.645z' fill='currentColor'/></svg></div>
                                <div id='next'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><path d='M5.536 21.886a1.004 1.004 0 0 0 1.033-.064l13-9a1 1 0 0 0 0-1.644l-13-9A1 1 0 0 0 5 3v18a1 1 0 0 0 .536.886z' fill='currentColor'/></svg>
                                </div>

                              </div></h2>
            <div class='bc-fff s1 r2 p-13 oh full' id='related-posts'/>
            <script>
              var labelArray = [<b:if cond='data:post.labels'><b:loop values='data:post.labels' var='label'>&quot;<data:label.name/>&quot;<b:if cond='data:label.isLast != &quot;true&quot;'>,</b:if></b:loop></b:if>];
              var relatedPostConfig={
              homePage: &quot;<data:blog.homepageUrl/>&quot;,
              widgetTitle: &quot;&quot;,
              numPosts: 10,
              summaryLength: 20,
              titleLength:&quot;auto&quot;,
              thumbnailSize: 250,
              noImage: &quot;data:image/png;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs=&quot;,
              containerId: &quot;related-posts&quot;,
              newTabLink: false,
              moreText: &quot;Read more&quot;,
              widgetStyle: 2,
              callBack:function(){}
              }
            </script>
            <script>/*<![CDATA[*/ 
var randomRelatedIndex, showRelatedPost;
(function(n, m, k) {
  var d = {
    widgetTitle: "<h3 class='heading'>Related Posts</h3>",
    widgetStyle: 1,
    homePage: "http://www.jagodesain.com",
    numPosts: 7,
    summaryLength: 320,
    titleLength: "auto",
    thumbnailSize: 200,
    noImage: "data:image/png;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs=",
    containerId: "related-posts",
    newTabLink: false,
    moreText: "Read more",
    callBack: function() {}
  };
  for (var f in relatedPostConfig) {
    d[f] = (relatedPostConfig[f] == "undefined") ? d[f] : relatedPostConfig[f]
  }
  var j = function(a) {
      var b = m.createElement("script");
      b.async = "async";
      b.rel = "preload";
      b.src = a;
      k.appendChild(b)
    },
    o = function(b, a) {
      return Math.floor(Math.random() * (a - b + 1)) + b
    },
    l = function(a) {
      var p = a.length,
        c, b;
      if (p === 0) {
        return false
      }
      while (--p) {
        c = Math.floor(Math.random() * (p + 1));
        b = a[p];
        a[p] = a[c];
        a[c] = b
      }
      return a
    },
    e = (typeof labelArray == "object" && labelArray.length > 0) ? "/-/" + l(labelArray)[0] : "",
    h = function(b) {
      var c = b.feed.openSearch$totalResults.$t - d.numPosts,
        a = o(1, (c > 0 ? c : 1));
      j(d.homePage.replace(/\/$/, "") + "/feeds/posts/summary/-/Series" + e + "?alt=json-in-script&orderby=updated&start-index=" + a + "&max-results=" + d.numPosts + "&callback=showRelatedPost")
    },
    g = function(z) {
      var s = document.getElementById(d.containerId),
        x = l(z.feed.entry),
        A = d.widgetStyle,
        c = d.widgetTitle + '<ul class="pl-0 m-0 grid gtc-f141a gg-20 slide rel lsn ul style-' + A + '">',
        b = d.newTabLink ? ' target="_blank"' : "",
        y = '<!-- <div class="clear"/> -->',
        v, t, w, r, u;
      if (!s) {
        return
      }
      for (var q = 0; q < d.numPosts; q++) {
        if (q == x.length) {
          break
        }
        t = x[q].title.$t;
        w = (d.titleLength !== "auto" && d.titleLength < t.length) ? t.substring(0, d.titleLength) + "&hellip;" : t;
        r = ("media$thumbnail" in x[q] && d.thumbnailSize !== false) ? x[q].media$thumbnail.url.replace("s72","w210-h270") : d.noImage;
        u = ("summary" in x[q] && d.summaryLength > 0) ? x[q].summary.$t.replace(/<br ?\/?>/g, " ").replace(/<.*?>/g, "").replace(/[<>]/g, "").substring(0, d.summaryLength) + "&hellip;" : "";
        for (var p = 0, a = x[q].link.length; p < a; p++) {
          v = (x[q].link[p].rel == "alternate") ? x[q].link[p].href : "#"
        }
        if (A == 2) {
          c += '<li><div class="grid gtc-1001fr gg-10"><div class="item-thumbnail imgItem full-i h-220 relative b-img oh"><a href="' + v + '"><img class="post-thumb lazy" alt="' + w + '" src="' + r + '"></a></div><div class="item-title clamp toe oh block fs-15 lh-20 yt8m ck m-0"><a href="' + v + '"><span>' + w + '</span></a></div></div></li>'
        } else {
          c += '<li><div class="item-related"><div class="item-thumbnail"><div><img class="post-thumb lazy" alt="' + w + '" src="' + r + '"></div></div><div class="item-title"><a href="' + v + '"><span>' + w + '</span></a></div></div></li>'
        }
      }
      s.innerHTML = c += "</ul>";
      d.callBack()
    };
  randomRelatedIndex = h;
  showRelatedPost = g;
  j(d.homePage.replace(/\/$/, "") + "/feeds/posts/summary/-/Series" + e + "?alt=json-in-script&orderby=updated&max-results=0&callback=randomRelatedIndex")
})(window, document, document.getElementsByTagName("head")[0]);

/*]]>*/</script>
          </div>
        </b:includable>
        <b:includable id='postPagination-numeric'>
          <script>/*<![CDATA[*/
var noPage,currentPage,currentPageNo,postLabel,
perPage=20,
numPages=3,
firstText="First",
lastText="Last",
prevText="Previous",
nextText="Next",

urlactivepage=location.href,home_page="/";function looppagecurrentg(e){var a="";pageNumber=parseInt(numPages/2),pageNumber==numPages-pageNumber&&(numPages=2*pageNumber+1),pageStart=currentPageNo-pageNumber,pageStart<1&&(pageStart=1),lastPageNo=parseInt(e/perPage)+1,lastPageNo-1==e/perPage&&(lastPageNo-=1),pageEnd=pageStart+numPages-1,pageEnd>lastPageNo&&(pageEnd=lastPageNo),a+="<span class='showpageOf'>Page "+currentPageNo+" of "+lastPageNo+"</span>";var t=parseInt(currentPageNo)-1;currentPageNo>1&&(a+="page"==currentPage?'<span class="showpage firstpage"><a href="'+home_page+'">'+firstText+"</a></span>":'<span class="displaypageNum firstpage"><a href="/search/label/'+postLabel+"?&max-results="+perPage+'">'+firstText+"</a></span>"),currentPageNo>2&&(a+=3==currentPageNo?"page"==currentPage?'<span class="showpage"><a href="'+home_page+'">'+prevText+"</a></span>":'<span class="displaypageNum"><a href="/search/label/'+postLabel+"?&max-results="+perPage+'">'+prevText+"</a></span>":"page"==currentPage?'<span class="displaypageNum"><a href="#" onclick="redirectpage('+t+');return false">'+prevText+"</a></span>":'<span class="displaypageNum"><a href="#" onclick="redirectlabel('+t+');return false">'+prevText+"</a></span>"),pageStart>1&&(a+="page"==currentPage?'<span class="displaypageNum"><a href="'+home_page+'">1</a></span>':'<span class="displaypageNum"><a href="/search/label/'+postLabel+"?&max-results="+perPage+'">1</a></span>'),pageStart>2&&(a+=" ... ");for(var s=pageStart;s<=pageEnd;s++)a+=currentPageNo==s?'<span class="pagecurrent">'+s+"</span>":1==s?"page"==currentPage?'<span class="displaypageNum"><a href="'+home_page+'">1</a></span>':'<span class="displaypageNum"><a href="/search/label/'+postLabel+"?&max-results="+perPage+'">1</a></span>':"page"==currentPage?'<span class="displaypageNum"><a href="#" onclick="redirectpage('+s+');return false">'+s+"</a></span>":'<span class="displaypageNum"><a href="#" onclick="redirectlabel('+s+');return false">'+s+"</a></span>";pageEnd<lastPageNo-1&&(a+="..."),pageEnd<lastPageNo&&(a+="page"==currentPage?'<span class="displaypageNum"><a href="#" onclick="redirectpage('+lastPageNo+');return false">'+lastPageNo+"</a></span>":'<span class="displaypageNum"><a href="#" onclick="redirectlabel('+lastPageNo+');return false">'+lastPageNo+"</a></span>");var r=parseInt(currentPageNo)+1;currentPageNo<lastPageNo-1&&(a+="page"==currentPage?'<span class="displaypageNum"><a href="#" onclick="redirectpage('+r+');return false">'+nextText+"</a></span>":'<span class="displaypageNum"><a href="#" onclick="redirectlabel('+r+');return false">'+nextText+"</a></span>"),currentPageNo<lastPageNo&&(a+="page"==currentPage?'<span class="displaypageNum lastpage"><a href="#" onclick="redirectpage('+lastPageNo+');return false">'+lastText+"</a></span>":'<span class="displaypageNum lastpage"><a href="#" onclick="redirectlabel('+lastPageNo+');return false">'+lastText+"</a></span>");for(var p=document.getElementsByName("pageArea"),n=document.getElementById("blog-pager"),l=0;l<p.length;l++)p[l].innerHTML=a;p&&p.length>0&&(a=""),n&&(n.innerHTML=a)}function totalcountdata(e){var a=e.feed;looppagecurrentg(parseInt(a.openSearch$totalResults.$t,10))}function pagecurrentg(){var e=urlactivepage;-1!=e.indexOf("/search/label/")&&(postLabel=-1!=e.indexOf("?updated-max")?e.substring(e.indexOf("/search/label/")+14,e.indexOf("?updated-max")):e.substring(e.indexOf("/search/label/")+14,e.indexOf("?&max"))),-1==e.indexOf("?q=")&&-1==e.indexOf(".html")&&(-1==e.indexOf("/search/label/")?(currentPage="page",currentPageNo=-1!=urlactivepage.indexOf("#PageNo=")?urlactivepage.substring(urlactivepage.indexOf("#PageNo=")+8,urlactivepage.length):1,document.write('<script src="'+home_page+'feeds/posts/summary?max-results=1&alt=json-in-script&callback=totalcountdata"><\/script>')):(currentPage="label",-1==e.indexOf("&max-results=")&&(perPage=20),currentPageNo=-1!=urlactivepage.indexOf("#PageNo=")?urlactivepage.substring(urlactivepage.indexOf("#PageNo=")+8,urlactivepage.length):1,document.write('<script src="'+home_page+"feeds/posts/summary/-/"+postLabel+'?alt=json-in-script&callback=totalcountdata&max-results=1" ><\/script>')))}function redirectpage(e){jsonstart=(e-1)*perPage,noPage=e;var a=document.getElementsByTagName("head")[0],t=document.createElement("script");t.type="text/javascript",t.setAttribute("src",home_page+"feeds/posts/summary?start-index="+jsonstart+"&max-results=1&alt=json-in-script&callback=finddatepost"),a.appendChild(t)}function redirectlabel(e){jsonstart=(e-1)*perPage,noPage=e;var a=document.getElementsByTagName("head")[0],t=document.createElement("script");t.type="text/javascript",t.setAttribute("src",home_page+"feeds/posts/summary/-/"+postLabel+"?start-index="+jsonstart+"&max-results=1&alt=json-in-script&callback=finddatepost"),a.appendChild(t)}function finddatepost(e){post=e.feed.entry[0];var a=post.published.$t.substring(0,19)+post.published.$t.substring(23,29),t=encodeURIComponent(a);if("page"==currentPage)var s="/search?updated-max="+t+"&max-results="+perPage+"#PageNo="+noPage;else s="/search/label/"+postLabel+"?updated-max="+t+"&max-results="+perPage+"#PageNo="+noPage;location.href=s}void 0===firstText&&(firstText="First"),void 0===lastText&&(lastText="Last"),pagecurrentg();
 /*]]>*/</script>
        </b:includable>
        <b:includable id='Category'>

          <b:if cond='data:post.labels any (l =&gt; l.name == &quot;Manga&quot;)'>
            <svg class='absolute t-5 r-5 c-fff s2' viewBox='0 0 640 480' xmlns='http://www.w3.org/2000/svg'><defs><clipPath id='a'><path d='M-88.001 32h640v480h-640z' fill-opacity='.67'/></clipPath></defs><g clip-path='url(#a)' fill-rule='evenodd' stroke-width='1pt' transform='translate(88.001 -32)'><path d='M-128 32h720v480h-720z' fill='#fff'/><circle cx='523.08' cy='344.05' fill='#d30000' r='194.93' transform='translate(-168.44 8.618) scale(.76554)'/></g></svg>
            <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Manhua&quot;)'/>

            <svg class='absolute t-5 r-5 c-fff s2' viewBox='0 0 30 20' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'>
              <defs>
                <path d='M0,-1 0.587785,0.809017 -0.951057,-0.309017H0.951057L-0.587785,0.809017z' fill='#FFFF00' id='s'/>
              </defs>
              <rect fill='#EE1C25' height='20' width='30'/>
              <use transform='translate(5,5) scale(3)' xlink:href='#s'/>
              <use transform='translate(10,2) rotate(23.036243)' xlink:href='#s'/>
              <use transform='translate(12,4) rotate(45.869898)' xlink:href='#s'/>
              <use transform='translate(12,7) rotate(69.945396)' xlink:href='#s'/>
              <use transform='translate(10,9) rotate(20.659808)' xlink:href='#s'/>
            </svg>
            <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Manhwa&quot;)'/>
            <svg class='absolute t-5 r-5 c-fff s2' viewBox='0 0 640 480' xmlns='http://www.w3.org/2000/svg'><defs><clipPath id='a'><path d='M-95.808-.44h682.67v512h-682.67z' fill-opacity='.67'/></clipPath></defs><g clip-path='url(#a)' fill-rule='evenodd' transform='translate(89.82 .412) scale(.9375)'><path d='M610.61 511.56h-730.17v-512h730.17z' fill='#fff'/><path d='M251.871 256.021c0 62.137-50.372 112.508-112.507 112.508-62.137 0-112.507-50.372-112.507-112.508 0-62.137 50.371-112.507 112.507-112.507 62.137 0 112.507 50.372 112.507 112.507z' fill='#fff'/><path d='M393.011 262.55c0 81.079-65.034 146.803-145.261 146.803S102.488 343.63 102.488 262.55s65.034-146.804 145.262-146.804S393.01 181.471 393.01 262.55z' fill='#c70000'/><path d='M-49.417 126.44l83.66-96.77 19.821 17.135-83.66 96.771zM-22.018 150.127l83.66-96.77 19.82 17.135-83.66 96.77z'/><path d='M-49.417 126.44l83.66-96.77 19.821 17.135-83.66 96.771z'/><path d='M-49.417 126.44l83.66-96.77 19.821 17.135-83.66 96.771zM5.967 174.32l83.66-96.77 19.82 17.136-83.66 96.77z'/><path d='M-49.417 126.44l83.66-96.77 19.821 17.135-83.66 96.771z'/><path d='M-49.417 126.44l83.66-96.77 19.821 17.135-83.66 96.771zM459.413 29.638l83.002 97.335-19.937 17-83.002-97.334zM403.707 77.141l83.002 97.335-19.936 17-83.002-97.334z'/><path d='M417.55 133.19l78.602-67.814 14.641 16.953-83.996 75.519-9.247-24.659z' fill='#fff'/><path d='M514.228 372.013l-80.416 95.829-19.716-16.4 80.417-95.828zM431.853 53.14l83.002 97.334-19.936 17.001-83.002-97.334zM541.475 394.676l-80.417 95.829-19.715-16.399 80.417-95.829zM486.39 348.857l-80.417 95.83-19.715-16.4 80.416-95.829z'/><path d='M104.6 236.68c4.592 36.974 11.297 78.175 68.199 82.455 21.328 1.278 62.817-5.074 77.061-63.19 18.688-55.829 74.975-71.88 113.28-41.613 21.718 14.166 27.727 36.666 29.283 53.557-1.739 54.243-32.874 101.2-72.823 122.14-45.93 27.3-109.56 27.87-165.3-13.49-25.12-23.57-60.219-67.02-49.7-139.86z' fill='#3d5897'/><path d='M435.91 370.59l78.734 67.661-14.591 16.997-87.156-71.851 23.013-12.807z' fill='#fff'/><path d='M-1.887 357.197l83.002 97.335-19.937 17-83.002-97.334z'/><path d='M-16.188 437.25l78.602-67.814 14.641 16.953-83.996 75.519-9.247-24.659z' fill='#fff'/><path d='M25.672 333.696l83.003 97.334-19.937 17-83.002-97.334zM-30.033 381.199l83.002 97.334-19.936 17L-49.97 398.2z'/></g></svg>
          </b:if>

        </b:includable>
        <b:includable id='cfs'>
          <b:if cond='data:post.labels any (l =&gt; l.name == &quot;Hot&quot;)'>
            <span class='hotx flex aic jcc' title='Hot'><span class='iconify' data-icon='ph:flame-duotone' data-inline='false'/></span>
          </b:if>
          <b:if cond='data:post.labels any (l =&gt; l.name == &quot;Color&quot;)'>
            <span class='colored'><span class='iconify mr-3' data-icon='ic:twotone-color-lens' data-inline='false'/> Color</span>
            <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Webtoon&quot;)'/>
            <span class='colored'><span class='iconify mr-3' data-icon='simple-icons:webtoon' data-inline='false'/> Webtoon</span>
          </b:if>
          <b:if cond='data:post.labels any (l =&gt; l.name == &quot;Completed&quot;)'>
            <span class='absolute com ttu fs-11'>Completed</span>
            <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Dropped&quot;)'/>
            <span class='absolute drp ttu fs-11'>Dropped</span>
            <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Ongoing&quot;)'/>
            <span class='absolute ong ttu fs-11'>Ongoing</span>
            <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Coming Soon&quot;)'/>
            <span class='absolute soo ttu fs-11'>Coming Soon</span>
          </b:if>
        </b:includable>
        <b:includable id='ScoreMultiItem'>
          <div class='m-GwWBFmbcL flex aic'>
            <b:class cond='data:view.isPost' name='s1'/>
          <b:include name='rbt'/>
          </div>
        </b:includable>
        <b:includable id='postEnclosures'>
          <b:loop values='data:post.enclosures' var='enclosure'>
            <b:if cond='data:enclosure.url in {&quot;https://dl.blog&quot;}'>   
              <a class='svg12sv flex aic' expr:href='data:enclosure.mimeType' rel='nofollow' target='_blank'>
                <svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 512 512' width='1em' xmlns='http://www.w3.org/2000/svg'><path d='M432 320h-32a16 16 0 0 0-16 16v112H64V128h144a16 16 0 0 0 16-16V80a16 16 0 0 0-16-16H48a48 48 0 0 0-48 48v352a48 48 0 0 0 48 48h352a48 48 0 0 0 48-48V336a16 16 0 0 0-16-16ZM488 0H360c-21.37 0-32.05 25.91-17 41l35.73 35.73L135 320.37a24 24 0 0 0 0 34L157.67 377a24 24 0 0 0 34 0l243.61-243.68L471 169c15 15 41 4.5 41-17V24a24 24 0 0 0-24-24Z' fill='currentColor'/></svg>
              </a>
            </b:if>
          </b:loop> 
        </b:includable>
        <b:includable id='Status'>
          <b:loop index='i' values='data:post.labels' var='label'>
            <b:if cond='data:label.name not in data:Status and data:label.name not in data:Score and data:label.name not in data:Other and data:label.name not in data:Other and data:label.name not in data:Genre and data:label.name not in data:Genre2 and data:label.name not in data:Alphabet and data:label.name not in data:Format and data:label.name not in data:Demographic and data:label.name not in data:Content'>
              <span class='ex wsn oh f1 toe' expr:data='data:label.name'>
                <data:label.name/>
                </span>
            </b:if>
          </b:loop>
        </b:includable>
        <b:includable id='darkMode'>
          <div class='flex aic mr-13 mla'>
            <label class='modeSwitch'>
              <input class='check flex' onclick='darkMode()' type='checkbox'/>
              <span class='toggleSwitch'/>
            </label>
          </div>
        </b:includable>
        <b:includable id='inlineAd2'>
          <div class='ads'>
<div class='widget-content'>
<img src='https://1.bp.blogspot.com/-FmfAILeAUs4/YQJE9dL6VhI/AAAAAAAAHXA/qm9QN_rJxwsG84UY9LYcD4Y58XTvQcwNQCLcBGAsYHQ/s720/ads.png'/>
</div>
</div>
        </b:includable>
        <b:includable id='inlineAd3'>
          <div class='ads'>
<div class='widget-content'>
<img src='https://1.bp.blogspot.com/-hLi6yeFLYTs/YQJT7C6A78I/AAAAAAAAHXY/49cOpBjTiV06NbAvtSMi2Ywezz2kE-T6gCLcBGAsYHQ/s400/ads-p.png'/>
</div>
</div>
        </b:includable>
        <b:includable id='rbt'>
          <b:with value='[&quot;0&quot;,&quot;1&quot;,&quot;2&quot;,&quot;3&quot;,&quot;4&quot;,&quot;5&quot;,&quot;6&quot;,&quot;7&quot;,&quot;8&quot;,&quot;9&quot;]' var='checkNumber'>
  <b:if cond='data:post.labels'>
    <b:loop values='data:post.labels' var='item'>
      <b:with value='&quot;String: &quot; + data:item.name' var='string'>
        <b:loop values='data:checkNumber' var='first'>
          <b:if cond='data:string contains data:first + &quot;.&quot;'>
            <b:loop values='data:checkNumber' var='last'>
              <b:if cond='data:string contains &quot;.&quot; + data:last'>
                <div class='rating'>
                  <script type='application/ld+json'>
  {
    &quot;@context&quot;: &quot;https://schema.org&quot;,
    &quot;@type&quot;: &quot;CreativeWorkSeries&quot;,
    &quot;url&quot;: &quot;<data:blog.url/>&quot;,
    &quot;name&quot;: &quot;<data:blog.pageTitle/>&quot;,
    &quot;alternateName&quot;: &quot;<data:blog.pageTitle/>&quot;,
    &quot;description&quot;: &quot;<data:post.snippets.short/>&quot;,
    &quot;inLanguage&quot;: &quot;<data:blog.locale/>&quot;,
    &quot;aggregateRating&quot;: {
    	&quot;@type&quot;: &quot;AggregateRating&quot;,
    	&quot;ratingValue&quot;: &quot;<data:item.name/>&quot;,
    	&quot;bestRating&quot;: &quot;10&quot;,
    	&quot;worstRating&quot;: &quot;1&quot;,
   	&quot;ratingCount&quot;: &quot;<data:post.body.size/>&quot;,
    	&quot;reviewCount&quot;: &quot;<data:post.body.size/>&quot;
  },
    &quot;author&quot;: {&quot;@type&quot;: &quot;Person&quot;, &quot;name&quot;: &quot;<data:post.author.name/>&quot;},
    &quot;publisher&quot;: {&quot;@type&quot;: &quot;Organization&quot;, &quot;name&quot;: &quot;<data:blog.title/>&quot;}
    }
  }
</script>
                  <div class='rating-prc'>
                    <div class='rtp'>
                      <b:with value='10' var='ten'>
                        <b:if cond='data:string contains data:ten + &quot;.&quot;'>
                          <div class='rtb'><span style='width:100%'/></div>
                          <b:else/>
                          <div class='rtb'><span expr:style='&quot;width:&quot; + data:first + &quot;&quot; + data:last + &quot;%&quot;'/></div>
                        </b:if>
                      </b:with>
                    </div>
                    <div class='num' expr:content='data:item.name'>
                      <data:item.name/>
                    </div>
                  </div>
                </div>
              </b:if>
            </b:loop>
          </b:if>
        </b:loop>
      </b:with>
    </b:loop>
  </b:if>
</b:with>
        </b:includable>
      </b:defaultmarkup>
    </b:defaultmarkups>
    <b:if cond='data:view.isPost'>
      <script>/*<![CDATA[*/ 
  document.getElementById('there').appendChild(
    document.getElementById('download')
  ); 
/*]]>*/</script>
      <script>/*<![CDATA[*/ 
  document.getElementById('myhero').appendChild(
    document.getElementById('custom-hero')
  ); 
/*]]>*/</script>
      <script>/*<![CDATA[*/ 
  document.getElementById('extra-target').appendChild(
    document.getElementById('extra-info')
  ); 
/*]]>*/</script>
      <script>/*<![CDATA[*/ 
  document.getElementById('syn-target').appendChild(
    document.getElementById('synopsis')
  ); 
/*]]>*/</script>
    </b:if>
    <script type='text/javascript'>
      var numposts = 3;
      var showpostthumbnails = false;
      var showpostdate = true;
    </script>
    <b:if cond='data:view.isMultipleItems'>
      <script type='text/javascript'>
        //<![CDATA[
function rcentbytag(e){document.write('<div class="chap-by-tag full">');for(var t=0;t<numposts;t++){var n=e.feed.entry[t];var r=n.title.$t;var i;if(t==e.feed.entry.length)break;for(var o=0;o<n.link.length;o++){if(n.link[o].rel=="replies"&&n.link[o].type=="text/html"){var u=n.link[o].title;var f=n.link[o].href}if(n.link[o].rel=="alternate"){i=n.link[o].href;break}}var l;try{l=n.media$thumbnail.url}catch(h){s=n.content.$t;a=s.indexOf("<img");b=s.indexOf('src="',a);c=s.indexOf('"',b+5);d=s.substr(b+5,c-b-5);if(a!=-1&&b!=-1&&c!=-1&&d!=""){l=d}else l="http://2.bp.blogspot.com/-giova1ZCh-A/Uzq6L8QTJNI/AAAAAAAAAJc/USXictTq_xs/s70-c/KM+Icon.png"}var p=n.published.$t;var v=p.substring(0,4);var m=p.substring(5,7);var g=p.substring(8,10);var y=new Array;y[1]="Januari";y[2]="Februari";y[3]="Maret";y[4]="April";y[5]="Mei";y[6]="Juni";y[7]="Juli";y[8]="Agustus";y[9]="September";y[10]="Oktober";y[11]="November";y[12]="Desember";document.write('<div class="flex aic jcsb y6x0p">');if(showpostthumbnails==true)document.write('<a href="'+i+'"  title="'+r+'"><img class="rct-thumb" alt="'+r+'" src="'+l+'"/></a>');document.write('<strong><a href="'+i+'" title="'+r+'" rel="nofollow">'+r+'</a></strong>');var x="";var T=0;if(showpostdate==true){x='<time class="showdates">'+x+g+" "+y[parseInt(m,10)]+" </time>";T=1}document.write(x);document.write("</div>");if(t!=numposts-1)document.write("")}document.write("</div>")}
//]]> </script>

    </b:if>
    <b:if cond='data:view.isPost'>
      <script>//<![CDATA[
function searchList() {
    var input, filter, ul, li, a, i, txtValue;
    input = document.getElementById("scInput");
    filter = input.value.toUpperCase();
    ul = document.getElementById("myUL");
    li = ul.getElementsByTagName("li");
    for (i = 0; i < li.length; i++) {
        a = li[i].getElementsByTagName("a")[0];
        txtValue = a.textContent || a.innerText;
        if (txtValue.toUpperCase().indexOf(filter) > -1) {
            li[i].style.display = "";
        } else {
            li[i].style.display = "none";
        }
    }
}
//]]> </script>
    </b:if>
    <b:if cond='data:view.isPost'>
<script type='text/javascript'>//<![CDATA[
  var numposts = 9999;
  var standardstyling = true;

  function chapterlist(json) {
    for (var i = 0; i < numposts; i++) {
      var entry = json.feed.entry[i];
      var posttitle = entry.title.$t;
	  var datatitle = entry.title.$t;
		var thumbnail = json.feed.entry[i].media$thumbnail.url'
      var date = json.feed.entry[i].published.$t;
      var posturl;
      if (i == json.feed.entry.length) break;
      for (var k = 0; k < entry.link.length; k++) {
        if (entry.link[k].rel == 'alternate') {
          posturl = entry.link[k].href;
          break;
        }
      }
      posttitle = posttitle.link(posturl);
      if (standardstyling) document.write('<li data="' + datatitle + '">');
      document.write(posttitle);
      document.write('<time class="timeago" datetime="' + date + '">');
      document.write(date);
      document.write('</time>');
    }
    if (standardstyling) document.write('</li>');
  } //]]></script>
<script type='text/javascript'>//<![CDATA[
const limitHistory = 10;
const histories = (function(){
list = [];
function Item(id,title,link){
	this.id = id;
	this.title = title;
    this.link = link;
}
function setHistory(){
	localStorage.setItem('History', JSON.stringify(list));
}
function loadHistory() {
    list = JSON.parse(localStorage.getItem('History'));
}
if (localStorage.getItem("History") != null) {
    loadHistory();
}
obj = {};
obj.addHistory = function(id,title,link) {
    var item = new Item(id,title,link);
    if(list != null){
    	same = list.find(item =>{return item.id == id;});
    		if(list.length<limitHistory){
     			if(!same){
    			list.push(item);
    			setHistory();
      			}else{
      			  for(let item in list){
      				if(list[item].id === id) {
        				list.splice(list.length, 0, list.splice(item, 1)[0]);
      				}
            		setHistory();
				  }
	  			}
			}else{
				if(!same){
				list.splice(0, 1);
    			list.push(item);
    			setHistory();
      			}else{
      			  for(let item in list){
      				if(list[item].id === id) {
        				list.splice(list.length, 0, list.splice(item, 1)[0]);
      				}
            		setHistory();
				  }
	  			}
	}
}else{
list.push(item);
setHistory();
}
}
return obj;
})(); //]]></script>
      <script>
        //<![CDATA[
eval(function(p,a,c,k,e,d){e=function(c){return(c<a?"":e(parseInt(c/a)))+((c=c%a)>35?String.fromCharCode(c+29):c.toString(36))};if(!''.replace(/^/,String)){while(c--)d[e(c)]=k[c]||e(c);k=[function(e){return d[e]}];e=function(){return'\\w+'};c=1;};while(c--)if(k[c])p=p.replace(new RegExp('\\b'+e(c)+'\\b','g'),k[c]);return p;}('1S I=["\\A\\q\\X\\e\\c\\m\\O\\e\\c\\R\\m\\19\\e\\1E\\q\\1D\\E\\Z\\q\\1g\\o\\p\\N\\A\\q\\d\\e\\16\\f\\c\\T\\o\\b\\c\\i\\b\\p\\E\\d\\f\\c\\r\\e\\b\\C\\c\\H\\C\\c\\u\\C\\c\\d\\C\\M\\C\\b\\n\\c\\s\\n\\b\\1t\\c\\Q\\e\\c\\L\\G\\c\\J\\e\\1p\\G\\X\\M\\c\\z\\e\\b\\n\\X\\n\\b\\G\\O\\M\\c\\V\\e\\b\\n\\O\\m\\16\\f\\c\\D\\f\\c\\U\\o\\d\\p\\P\\Z\\q\\1p\\o\\d\\p\\N\\A\\q\\g\\e\\16\\f\\c\\19\\o\\c\\O\\p\\E\\U\\o\\g\\p\\N\\g\\f\\1K\\e\\b\\b\\E\\A\\q\\h\\e\\d\\f\\c\\x\\E\\U\\o\\h\\f\\14\\f\\T\\w\\K\\p\\N\\1c\\o\\A\\q\\j\\e\\K\\E\\j\\y\\h\\f\\14\\f\\T\\E\\j\\n\\n\\p\\1c\\o\\A\\q\\i\\e\\h\\f\\14\\v\\j\\t\\m\\l\\e\\i\\f\\c\\1v\\f\\1C\\g\\m\\r\\e\\i\\f\\c\\Y\\f\\1C\\g\\m\\u\\e\\K\\E\\u\\y\\i\\f\\1d\\f\\T\\E\\u\\n\\n\\p\\U\\o\\b\\c\\k\\b\\e\\e\\i\\f\\1d\\v\\u\\t\\f\\c\\h\\p\\N\\A\\q\\x\\e\\i\\f\\1d\\v\\u\\t\\f\\13\\E\\x\\G\\G\\x\\f\\T\\w\\K\\G\\G\\l\\G\\G\\l\\f\\T\\w\\K\\G\\G\\r\\G\\G\\r\\f\\T\\w\\K\\G\\G\\19\\f\\c\\g\\o\\N\\1i\\1a\\x\\m\\R\\1a\\l\\m\\c\\1r\\1a\\r\\P\\p\\E\\c\\l\\P\\U\\o\\h\\f\\14\\f\\T\\w\\e\\O\\p\\X\\n\\e\\O\\m\\1g\\o\\p\\E\\17\\N\\1c\\o\\A\\q\\k\\m\\B\\e\\b\\b\\m\\k\\e\\b\\c\\1v\\b\\e\\e\\e\\c\\j\\1t\\19\\f\\c\\1y\\o\\Z\\o\\d\\m\\g\\p\\N\\c\\B\\q\\d\\f\\R\\w\\g\\f\\R\\1t\\c\\1a\\M\\c\\P\\p\\1a\\19\\m\\s\\e\\K\\E\\s\\y\\k\\f\\T\\E\\s\\n\\n\\p\\N\\A\\q\\z\\e\\k\\v\\s\\t\\f\\c\\1r\\m\\J\\e\\z\\f\\10\\o\\K\\m\\1f\\p\\m\\L\\e\\z\\f\\10\\o\\18\\m\\1q\\p\\m\\Q\\e\\z\\f\\10\\o\\1y\\m\\c\\K\\p\\m\\D\\e\\1E\\q\\1D\\E\\D\\v\\c\\t\\e\\b\\c\\A\\b\\m\\D\\v\\1H\\t\\e\\b\\c\\1o\\b\\m\\D\\v\\1r\\t\\e\\b\\c\\1q\\b\\m\\D\\v\\1f\\t\\e\\b\\c\\1z\\b\\m\\D\\v\\18\\t\\e\\b\\c\\12\\b\\m\\D\\v\\1v\\t\\e\\b\\c\\1g\\b\\m\\D\\v\\1q\\t\\e\\b\\c\\1m\\b\\m\\D\\v\\1y\\t\\e\\b\\c\\Z\\b\\m\\D\\v\\1o\\t\\e\\b\\c\\X\\b\\m\\D\\v\\c\\K\\t\\e\\b\\c\\15\\b\\m\\D\\v\\c\\c\\t\\e\\b\\c\\17\\b\\m\\D\\v\\c\\1H\\t\\e\\b\\c\\1e\\b\\E\\c\\16\\N\\U\\o\\k\\v\\s\\t\\f\\R\\f\\1x\\o\\b\\1u\\b\\p\\p\\N\\A\\q\\H\\e\\k\\v\\s\\t\\f\\R\\f\\1s\\o\\b\\1u\\b\\p\\v\\c\\t\\E\\H\\e\\H\\f\\c\\18\\o\\C\\v\\1J\\K\\M\\1o\\1j\\f\\M\\t\\n\\C\\J\\m\\b\\b\\p\\P\\17\\q\\U\\o\\k\\v\\s\\t\\f\\R\\f\\1x\\o\\b\\1m\\b\\p\\p\\N\\A\\q\\H\\e\\k\\v\\s\\t\\f\\R\\f\\1s\\o\\b\\1m\\b\\p\\v\\c\\t\\E\\H\\e\\H\\f\\c\\18\\o\\C\\v\\1J\\K\\M\\1o\\1j\\f\\M\\t\\n\\C\\J\\m\\b\\b\\p\\P\\17\\q\\A\\q\\H\\e\\b\\1z\\C\\15\\b\\P\\c\\1d\\o\\d\\p\\N\\c\\10\\f\\c\\1u\\o\\b\\c\\1x\\b\\p\\P\\B\\n\\e\\S\\y\\1I\\q\\Y\\e\\b\\c\\11\\b\\w\\y\\11\\q\\Y\\e\\b\\12\\M\\c\\14\\b\\w\\y\\V\\q\\Y\\e\\b\\1e\\b\\w\\y\\j\\q\\13\\e\\b\\S\\n\\k\\v\\s\\t\\f\\1i\\n\\S\\b\\w\\y\\c\\1f\\w\\S\\n\\H\\n\\S\\y\\C\\c\\1f\\w\\y\\C\\j\\w\\y\\C\\V\\w\\y\\C\\11\\w\\y\\11\\q\\Y\\e\\b\\12\\M\\c\\1i\\b\\w\\y\\V\\q\\Y\\e\\b\\1e\\M\\c\\1c\\b\\w\\y\\j\\q\\13\\e\\b\\S\\n\\k\\v\\s\\t\\f\\1i\\n\\S\\b\\w\\S\\n\\k\\v\\s\\t\\f\\R\\n\\S\\y\\C\\j\\w\\y\\C\\V\\w\\y\\V\\q\\Y\\e\\b\\1e\\M\\c\\13\\b\\w\\S\\n\\Q\\n\\b\\q\\b\\n\\D\\v\\c\\1s\\o\\L\\m\\c\\K\\p\\t\\n\\b\\q\\b\\n\\J\\n\\b\\y\\C\\V\\w\\y\\C\\11\\w\\y\\C\\1I\\w\\b\\P\\g\\f\\1K\\e\\S\\y\\1F\\q\\Y\\e\\b\\12\\M\\c\\1p\\b\\w\\S\\n\\B\\n\\b\\y\\C\\1F\\w\\b\\P\\P\\P\\P","\\a","\\l\\k\\i\\u\\g","\\a\\a\\a\\a\\a\\a\\a\\a\\a\\a\\a\\D\\j\\h\\a\\a\\a\\a\\a\\a\\a\\a\\i\\d\\r\\J\\g\\L\\a\\T\\x\\s\\x\\i\\a\\a\\a\\a\\a\\a\\B\\i\\j\\l\\l\\a\\a\\a\\a\\a\\a\\l\\k\\j\\r\\a\\u\\Q\\a\\H\\j\\U\\a\\d\\k\\10\\u\\l\\g\\15\\h\\h\\a\\a\\d\\r\\g\\h\\O\\a\\l\\g\\j\\h\\g\\a\\s\\u\\D\\a\\Q\\x\\r\\B\\g\\u\\z\\r\\a\\d\\i\\l\\d\\a\\x\\h\\i\\a\\Q\\z\\h\\a\\s\\z\\B\\x\\H\\d\\r\\g\\a\\L\\h\\d\\Q\\a\\d\\k\\l\\a\\l\\x\\A\\l\\g\\h\\u\\r\\J\\a\\d\\k\\a\\a\\i\\u\\r\\R\\a\\d\\k\\10\\u\\l\\g\\a\\u\\r\\B\\i\\x\\s\\d\\l\\a\\l\\k\\i\\u\\g\\a\\Z\\k\\u\\l\\z\\s\\d\\a\\h\\x\\r\\Z\\k\\10\\u\\l\\g\\a\\X\\L\\j\\k\\g\\d\\h\\a\\15\\h\\h\\j\\O\\a\\r\\d\\V\\a\\i\\u\\a\\x\\i\\a\\u\\r\\r\\d\\h\\1c\\1g\\12\\10\\a\\a\\a\\a\\g\\j\\r\\J\\J\\j\\i\\a\\B\\L\\j\\k\\g\\d\\h\\a\\h\\d\\k\\i\\j\\B\\d\\a\\g\\u\\g\\i\\d\\a\\12\\j\\h\\a\\l\\z\\h\\g\\a\\17\\d\\A\\a\\l\\z\\h\\g\\A\\O\\a\\13\\j\\r\\a\\h\\d\\g\\x\\h\\r\\a\\i\\j\\A\\d\\i\\a\\s\\d\\Q\\j\\x\\i\\g\\a\\j\\i\\g\\a\\B\\j\\i\\i\\A\\j\\B\\R\\a\\T\\l\\z\\r\\a\\k\\z\\l\\g\\l\\a\\B\\h\\d\\j\\g\\d\\Z\\i\\d\\H\\d\\r\\g\\a\\c\\18\\K\\a\\l\\B\\h\\u\\k\\g\\a\\Q\\d\\d\\s\\l\\a\\l\\h\\B\\a\\u\\r\\s\\d\\U\\a\\j\\i\\g\\d\\h\\r\\j\\g\\d\\a\\k\\x\\A\\i\\u\\l\\L\\d\\s\\a\\h\\d\\i\\a\\A\\h\\d\\j\\R\\a\\k\\x\\l\\L\\a\\Q\\d\\d\\s\\a\\A\\z\\s\\O\\a\\h\\d\\l\\x\\i\\g\\l\\a\\j\\k\\k\\d\\r\\s\\X\\L\\u\\i\\s\\a\\z\\x\\g\\k\\x\\g\\11\\u\\D\\a\\J\\d\\g\\Z\\i\\d\\H\\d\\r\\g\\14\\O\\16\\s\\a\\1d\\B\\g\\a\\h\\u\\J\\L\\g\\a\\1m\\d\\k\\a\\B\\L\\j\\h\\a\\15\\x\\J\\a\\1z\\z\\D\\a\\i\\d\\Q\\g\\a\\T\\s\\i\\a\\g\\h\\O\\a\\s\\j\\g\\d\\a\\11\\d\\B\\a\\B\\z\\r\\l\\z\\i\\d\\a\\12\\j\\O\\a\\15\\k\\h\\a\\B\\j\\g\\B\\L\\a\\u\\g\\d\\H\\a\\d\\h\\h\\z\\h\\a\\k\\j\\h\\l\\d\\16\\r\\g\\a\\13\\x\\i\\a\\13\\x\\r\\a\\i\\z\\J","","\\Q\\h\\z\\H\\X\\L\\j\\h\\X\\z\\s\\d","\\h\\d\\k\\i\\j\\B\\d","\\1j\\V\\n","\\1j\\A","\\J"];1T(1h(1l,1n,F,1b,W,1w){W=1h(F){1k(F<1n?I[4]:W(1U(F/1n)))+((F=F%1n)>1R?1B[I[5]](F+1V):F.1N(1M))};1G(!I[4][I[6]](/^/,1B)){1A(F--){1w[W(F)]=1b[F]||W(F)};1b=[1h(W){1k 1w[W]}];W=1h(){1k I[7]};F=1};1A(F--){1G(1b[F]){1l=1l[I[6]](1L 1Q(I[8]+W(F)+I[8],I[9]),1b[F])}};1k 1l}(I[0],1O,1P,I[3][I[2]](I[1]),0,{}))',62,120,'||||||||||x7C|x22|x31|x65|x3D|x2E|x74|x72|x6C|x61|x70|x73|x2C|x2B|x28|x29|x20|x6E|x64|x5D|x69|x5B|x3E|x75|x3C|x6F|x62|x63|x2F|x76|x3B|_0x2237x3|x26|x6D|_0x1fc8|x67|x30|x68|x2D|x7B|x79|x7D|x66|x6B|x27|x6A|x78|x77|_0x2237x5|x43|x71|x45|x4C|x44|x4D|x4A|x42|x41|x49|x46|x35|x7A|x3A|_0x2237x4|x48|x4F|x4B|x34|x54|function|x47|x5C|return|_0x2237x1|x53|_0x2237x2|x39|x50|x37|x33|x52|x3F|x55|x36|_0x2237x6|x51|x38|x4E|while|String|x24|x56|x57|x59|if|x32|x58|x5E|x5A|new|36|toString|62|119|RegExp|35|var|eval|parseInt|29'.split('|'),0,{}));
//]]>
      </script>  
      <script type='text/javascript'>/*<![CDATA[*/
  const nPL={arr:new Array,compile:function(){const t=this.arr;let e='<div class="inner_nPL"><a id="dl" href="#" class="dlx r"><i class="fas fa-cloud-download-alt mr-7"></i>Download</a>',n='<div><select id="nPL_select" onchange="this.options[this.selectedIndex].value&&window.open(this.options[this.selectedIndex].value,\'_self\')" name="nPL_list"><option value="" selected>Select Chapter</option>';for(let s=0;s<t.length;s++){s!=t.length-0&&(n+=`<option value="${t[s].link}">${t[s].title}</option>`);const l=window.location.pathname;t[s].link.includes(l)&&(t[s+1]&&t[s+1]!=t.length-0&&(console.log(t[s+1]),s+1!=t.length-0&&(e+=`<a href="${t[s+1].link}" title="${t[s+1].title}"><i class="fas fa-angle-left mr-7"></i><span>Prev</span></a>`)),t[t.length-0]&&(e+=`<a href="${t[t.length-0].link}" title="${t[t.length-0].title}"><span>Home</span></a>`),t[s-1]&&(console.log(t[s-1]),e+=`<a href="${t[s-1].link}" title="${t[s-1].title}"><span class="mr-7">Next</span><i class="fas fa-angle-right"></i></a>`))}n+=`</select></div>${e}</div>`,jQuery("#nPL").html(n)},create:function(t){const e=this;t.ajax({type:"get",url:`/feeds/posts/summary/-/${e.settings.cat}?alt=json-in-script&start-index=${e.settings.start}&max-results=${e.settings.max}`,dataType:"jsonp",success:function(t){"entry"in t.feed?(t.feed.entry.forEach(t=>{e.arr.push({title:t.title.$t,link:t.link.find(t=>"alternate"==t.rel).href})}),t.feed.length>=e.settings.max?(e.settings.start+=e.settings.max,e.run(e.settings.cat)):e.compile()):e.arr.length>0&&e.compile()},error:function(t){console.log(t)}})},run:function(t){"function"==typeof jQuery&&document.getElementById("nPL")?(this.settings.cat=t,this.create(jQuery)):console.log("Error not function")},settings:{start:1,max:150}};
/*]]>*/</script>
      <script type='text/javascript'>/*<![CDATA[*/
  const nPL2={arr:new Array,compile:function(){const t=this.arr;let e='<div class="inner_nPL">',n='<div><select id="nPL_select" onchange="this.options[this.selectedIndex].value&&window.open(this.options[this.selectedIndex].value,\'_self\')" name="nPL_list"><option value="" selected>Select Chapter</option>';for(let s=0;s<t.length;s++){s!=t.length-0&&(n+=`<option value="${t[s].link}">${t[s].title}</option>`);const l=window.location.pathname;t[s].link.includes(l)&&(t[s+1]&&t[s+1]!=t.length-0&&(console.log(t[s+1]),s+1!=t.length-0&&(e+=`<a href="${t[s+1].link}" title="${t[s+1].title}"><i class="fas fa-angle-left mr-7"></i><span>Prev</span></a>`)),t[t.length-0]&&(e+=`<a href="${t[t.length-0].link}" title="${t[t.length-0].title}"><span>Home</span></a>`),t[s-1]&&(console.log(t[s-1]),e+=`<a href="${t[s-1].link}" title="${t[s-1].title}"><span class="mr-7">Next</span><i class="fas fa-angle-right"></i></a>`))}n+=`</select></div>${e}</div>`,jQuery("#nPL2").html(n)},create:function(t){const e=this;t.ajax({type:"get",url:`/feeds/posts/summary/-/${e.settings.cat}?alt=json-in-script&start-index=${e.settings.start}&max-results=${e.settings.max}`,dataType:"jsonp",success:function(t){"entry"in t.feed?(t.feed.entry.forEach(t=>{e.arr.push({title:t.title.$t,link:t.link.find(t=>"alternate"==t.rel).href})}),t.feed.length>=e.settings.max?(e.settings.start+=e.settings.max,e.run(e.settings.cat)):e.compile()):e.arr.length>0&&e.compile()},error:function(t){console.log(t)}})},run:function(t){"function"==typeof jQuery&&document.getElementById("nPL2")?(this.settings.cat=t,this.create(jQuery)):console.log("Error not function")},settings:{start:1,max:150}};
/*]]>*/</script>
    </b:if>
    <b:if cond='data:view.isHomepage'>
      <script>
//<![CDATA[
//Start function
function timeAgo(o){var t=(new Date).getTime()-o.getTime(),e=Math.floor(t/1e3),r=Math.floor(e/60),a=Math.floor(r/60),g=Math.floor(a/24),h=Math.floor(g/30),n=Math.floor(h/12);return 0===t?"Just now":e<60?e+" seconds Ago":r<60?r+" min Ago":a<24?a+" hours Ago":g<30?g+" days Ago":h<12?h+" months":n+" years Ago"}
//End function

//]]>
</script>
      <script async='async'>
  //<![CDATA[
  var timeString=function(t){if(/([12]\d{3}-(0[1-9]|1[0-2])-(0[1-9]|[12]\d|3[01]))/.test(t)){var e=t,i=e.substring(0,4),n=e.substring(5,7),r=e.substring(8,10),o=new Array;return o[1]="Jan",o[2]="Feb",o[3]="Mar",o[4]="Apr",o[5]="May",o[6]="Jun",o[7]="Jul",o[8]="Aug",o[9]="Sep",o[10]="Oct",o[11]="Nov",o[12]="Dec",r+" "+o[parseInt(n,10)]+" "+i}return!1},imageString=function(t){var e=t.indexOf("<img"),i=t.indexOf('src="',e),n=t.indexOf('"',i+5),r=t.substr(i+5,n-i-5);return-1!=e&&-1!=i&&-1!=n&&""!=r?r:"https://1.bp.blogspot.com/-BYDJ1dpFEhE/X9QnAUfeORI/AAAAAAAAHxw/OjfaqiPHjhAmCgJts39XIg7o4KR-8YtdACNcBGAsYHQ/w300-h225-p-k-no-nu/dagruel-no-image.png"},mangaPost={mainItemArr:new Array,subItemArr:new Array,compile:function(t){var e=t.feed.entry;if(!e)return!1;var i=document.getElementById("myManga");if(!i)return!1;if(i.dataset.created="Dagruel",e.forEach(function({category:t,content:e,link:i,title:n,published:r,media$thumbnail:o}){var a=n.$t,s=t.map(function(t){return t.term}),u=i.find(function(t){if("alternate"===t.rel)return t}).href,c="function"==typeof timeAgo?timeAgo(new Date(r.$t)):timeString(r.$t),l=e.$t&&e.$t.length>0?e.$t:"Nothing",m=o?o.url.replace("s72","w175-h235"):imageString(l);s=s.filter(function(t){if("Project"!==t)return t}),mangaPost.mainItem.filter(function(t){s.join(", ").includes(t)&&mangaPost.mainItemArr.push({title:a,link:u,image:m,category:s})}),mangaPost.subItem.filter(function(t){s.join(", ").includes(t)&&mangaPost.subItemArr.push({titleSub:a,linkSub:u,publishedSub:c,categorySub:s})})}),mangaPost.mainItemArr.length>0){var n="";mangaPost.mainItemArr.forEach(function({title:t,link:e,image:i,category:r}){var o="";
var lang = "";
var label = r.find(i => "Hot, New".includes(i));
if ("Hot" == label) {
  lang = "<span class='hot absolute r-5 t-3'></span>";
} else if ("New" == label) {
  lang = "<span class='new absolute r-5 t-3'></span>";
} else lang = "";
var typ = "";
var label2 = r.find(i => "Manga, Manhua, Manhwa".includes(i));
if ("Manga" == label2) {
  typ = "<span class='absolute po manga'>Manga</span>";
} else if ("Manhua" == label2) {
  typ = "<span class='absolute po manhua'>Manhua</span>";
} else if ("Manhwa" == label2) {
  typ = "<span class='absolute po manhwa'>Manhwa</span>";
} else typ = "";
console.log(`${label} & ${lang}`);
mangaPost.subItemArr.length>0&&mangaPost.subItemArr.forEach(function({titleSub:t,linkSub:e,publishedSub:i,categorySub:n}){var a=t;mangaPost.settingTitle.forEach(function({name:e,news:i}){a.includes(e)&&(a=i+" "+t.split(e)[1].replace(/[^0-9\.-]+/g,""))}),n.filter(function(n){r.join(", ").includes(n)&&(o+='<li class="char"><div class="chpName"><a href="'+e+'" title="'+t+'">'+a+'<span class="new-tag">new</span></a></div><time class="chpDate">'+i+"</time></li>")})}),n+='<div class="bookItem bb-1pxsf"><a href="'+e+'" title="'+t+'"><div class="snippet-thumbnail"><img loading="lazy" src="' + i + '"/>'+lang+typ+'</div></a><div class="data"><h2><a href="'+e+'" title="'+t+'">'+t+'</a></h2><ul class="subItem">'+o+"</ul></div></div>"}),i.innerHTML=n}},run:function(t,e){var i=document.createElement("script");i.src="/feeds/posts/default/-/"+t+"?orderby=published&alt=json-in-script&max-results="+e+"&callback=mangaPost.compile",document.body.appendChild(i)}};

  //Setting Script
  mangaPost.mainItem = ['Manga','Manhwa','Manhua'];
  mangaPost.subItem = ['Chapter'];
  mangaPost.settingTitle = [{
    name: 'Chapter',
    news: 'Ch'
  }, {
    name: 'Episode',
    news: 'Ep'
  }];
  //]]>
</script>
      <script async='async'>
  //<![CDATA[
  var timeString = function(t) {
    if (/([12]\d{3}-(0[1-9]|1[0-2])-(0[1-9]|[12]\d|3[01]))/.test(t)) {
      var e = t,
        i = e.substring(0, 4),
        n = e.substring(5, 7),
        r = e.substring(8, 10),
        o = new Array;
      return o[1] = "Jan", o[2] = "Feb", o[3] = "Mar", o[4] = "Apr", o[5] = "May", o[6] = "Jun", o[7] = "Jul", o[8] = "Aug", o[9] = "Sep", o[10] = "Oct", o[11] = "Nov", o[12] = "Dec", r + " " + o[parseInt(n, 10)] + " " + i
    }
    return !1
  },
  imageString = function(t) {
    var e = t.indexOf("<img"),
      i = t.indexOf('src="', e),
      n = t.indexOf('"', i + 5),
      r = t.substr(i + 5, n - i - 5);
    return -1 != e && -1 != i && -1 != n && "" != r ? r : "https://1.bp.blogspot.com/-BYDJ1dpFEhE/X9QnAUfeORI/AAAAAAAAHxw/OjfaqiPHjhAmCgJts39XIg7o4KR-8YtdACNcBGAsYHQ/w300-h225-p-k-no-nu/dagruel-no-image.png"
  },
  update = {
    mainItemArr: new Array,
    subItemArr: new Array,
    compile: function(t) {
      var e = t.feed.entry;
      if (!e) return !1;
      var i = document.getElementById("Update");
      if (!i) return !1;
      if (i.dataset.created = "Dagruel", e.forEach(function({
          category: t,
          content: e,
          link: i,
          title: n,
          published: r,
          media$thumbnail: o
        }) {
          var a = n.$t,
            s = t.map(function(t) {
              return t.term
            }),
            u = i.find(function(t) {
              if ("alternate" === t.rel) return t
            }).href,
            c = "function" == typeof timeAgo ? timeAgo(new Date(r.$t)) : timeString(r.$t),
            l = e.$t && e.$t.length > 0 ? e.$t : "Nothing",
            m = o ? o.url.replace("s72", "w175-h235") : imageString(l);
          s = s.filter(function(t) {
            if ("Project" !== t) return t
          }), update.mainItem.filter(function(t) {
            s.join(", ").includes(t) && update.mainItemArr.push({
              title: a,
              link: u,
              image: m,
              category: s
            })
          }), update.subItem.filter(function(t) {
            s.join(", ").includes(t) && update.subItemArr.push({
              titleSub: a,
              linkSub: u,
              publishedSub: c,
              categorySub: s
            })
          })
        }), update.mainItemArr.length > 0) {
        var n = "";
        update.mainItemArr.forEach(function({
          title: t,
          link: e,
          image: i,
          category: r
        }) {
          var o = "";
var lang = "";
var label = r.find(i => "Hot, New".includes(i));
if ("Hot" == label) {
  lang = "<span class='hot absolute r-5 t-3'></span>";
} else if ("New" == label) {
  lang = "<span class='new absolute r-5 t-3'></span>";
} else lang = "";
var typ = "";
var label2 = r.find(i => "Manga, Manhua, Manhwa".includes(i));
if ("Manga" == label2) {
  typ = "<span class='absolute po manga'>Manga</span>";
} else if ("Manhua" == label2) {
  typ = "<span class='absolute po manhua'>Manhua</span>";
} else if ("Manhwa" == label2) {
  typ = "<span class='absolute po manhwa'>Manhwa</span>";
} else typ = "";
console.log(`${label} & ${lang}`);
          update.subItemArr.length > 0 && update.subItemArr.forEach(function({
            titleSub: t,
            linkSub: e,
            publishedSub: i,
            categorySub: n
          }) {
            var a = t;
            update.settingTitle.forEach(function({
              name: e,
              news: i
            }) {
              a.includes(e) && (a = i + " " + t.split(e)[1].replace(/[^0-9\.-]+/g, ""))
            }), n.filter(function(n) {
              r.join(", ").includes(n) && (o += '<li class="char"><div class="chpName"><a href="' + e + '" title="' + t + '">' + a + '<span class="new-tag">new</span></a></div><time class="chpDate">' + i + "</time></li>")
            })
          }), n += '<div class="bookItem bb-1pxsf"><a href="' + e + '" title="' + t + '"><div class="snippet-thumbnail"><img loading="lazy" src="' + i + '"/>'+lang+typ+'</div></a><div class="data"><h2><a href="' + e + '" title="' + t + '">' + t + '</a></h2><ul class="subItem">' + o + "</ul></div></div>"
        }), i.innerHTML = n
      }
    },
    run: function(t, e) {
      var i = document.createElement("script");
      i.src = "/feeds/posts/default/-/" + t + "?orderby=published&alt=json-in-script&max-results=" + e + "&callback=update.compile", document.body.appendChild(i)
    }
  };
  //Setting Script
  update.mainItem = ['Update'];
  update.subItem = ['Chapter'];
  update.settingTitle = [{
    name: 'Chapter',
    news: 'Ch'
  }, {
    name: 'Episode',
    news: 'Ep'
  }];
  //]]>
</script>
      <script type='text/javascript'>/*<![CDATA[*/
const mTP={shuffleArray:t=>{var e,i,n=t.length;if(0===n)return!1;for(;--n;)e=Math.floor(Math.random()*(n+1)),i=t[n],t[n]=t[e],t[e]=i;return t},run:(t,e,i=10,n=5)=>{if(0==t("#mTP_Slider").length)return console.log("Tag mTP_Slider tidak ada");mTP.maxCat=n,mTP.max=i,window.matchMedia("(max-width: 600px)").matches&&(mTP.maxCat=3),window.matchMedia("(max-width: 480px)").matches&&(mTP.maxCat=2);const a=0==e?"":`/-/${e}`;t.ajax({url:`/feeds/posts/default${a}?alt=json-in-script&max-results=150`,type:"get",dataType:"jsonp",success:function(e){mTP.compile(t,e)},error:function(t){console.log(t)}})},compile:(t,e)=>{if("entry"in e.feed){const n=mTP.shuffleArray(e.feed.entry);mTP.filter=mTP.shuffleArray(e.feed.category.map(t=>t.term).filter(t=>{if(mTP.Select.includes(t))return t})).slice(0,mTP.maxCat),mTP.obj={},t.each(mTP.filter,function(e,i){n.filter(e=>{const n=e.category.map(t=>t.term);if(n.includes(i)){const a=mTP.obj[i];a?a.length<mTP.max&&a.push({title:e.title.$t,cat:n,link:e.link.find(t=>"alternate"==t.rel).href,image:"media$thumbnail"in e?e.media$thumbnail.url.match(/\/s[0-9]{2}-(w[0-9]+-)?c/)?e.media$thumbnail.url.replace(/\/s[0-9]{2}-(w[0-9]+-)?c/,`/${mTP.iSize}-p-k-no-nu`):e.media$thumbnail.url.replace(/\=s[0-9]{2}-(w[0-9]+-)?c/,`=${mTP.iSize}-p-k-no-nu`):"content"in e?t(e.content.$t).find("img").attr("src"):mTP.noImage}):mTP.obj[i]=[{title:e.title.$t,cat:n,link:e.link.find(t=>"alternate"==t.rel).href,image:"media$thumbnail"in e?e.media$thumbnail.url.match(/\/s[0-9]{2}-(w[0-9]+-)?c/)?e.media$thumbnail.url.replace(/\/s[0-9]{2}-(w[0-9]+-)?c/,`/${mTP.iSize}-p-k-no-nu`):e.media$thumbnail.url.replace(/\=s[0-9]{2}-(w[0-9]+-)?c/,`=${mTP.iSize}-p-k-no-nu`):"content"in e?t(e.content.$t).find("img").attr("src"):mTP.noImage}]}})});const a=t('<div class="series-gen"><div class="head"><div class="r-title"></div><ul class="nav-tabs tabs tab r2"></ul></div><div class="listupd"></div></div>'),l=Object.keys(mTP.obj).sort().reduce((t,e)=>(t[e]=mTP.obj[e],t),{});for(var i in l){const e=i.replace(/\W/g,"");a.find(".nav-tabs").append(`<li><span data-id="series-${e}">${i}</span></li>`),a.find(".listupd").append(`<div id="series-${e}" class="customAF scroll"><div class="inner scrolling"></div>${mTP.btnPrev}${mTP.btnNext}</div>`),t.each(mTP.obj[i],function(){a.find(`#series-${e} .inner`).append(`<article class="customAgata">\n          <a href="${this.link}" title="${this.title}">\n            <div class="images">\n              <figure>\n                <img src="${this.image}" alt="${this.title}">\n              </figure>\n            </div>\n            <h2 class="entry-title">${this.title}</h2>\n          </a>\n        </article>`)})}t("#mTP_Slider").html(a),t(".nav-tabs li").click(function(){const e=t(this).find("span").attr("data-id");t(".customAF.scroll, .nav-tabs li").each(function(){t(this).attr("id")==e||t(this).find("span").attr("data-id")==e?t(this).addClass("active"):t(this).removeClass("active")})}),t(".nav-tabs li").first().click()}},sN:t=>{let e=t.parentElement.querySelector(".inner.scrolling"),i=e.clientWidth;e.scrollLeft+=i},sB:t=>{let e=t.parentElement.querySelector(".inner.scrolling"),i=e.clientWidth;e.scrollLeft-=i},btnNext:'<button onclick="mTP.sN(this)" class="scrollButton right"><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="1em" height="1em" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24"><g fill="none"><path d="M15.713 12l-6.01-6.01l-1.415 1.414l4.6 4.6l-4.6 4.593l1.414 1.414L15.713 12z" fill="currentColor"/></g></svg></button>',btnPrev:'<button onclick="mTP.sB(this)" class="scrollButton left"><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="1em" height="1em" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24"><g fill="none"><path d="M8.288 12l6.01 6.01l1.414-1.414l-4.6-4.6l4.6-4.6l-1.414-1.406L8.288 12z" fill="currentColor"/></g></svg></button>',iSize:"w207-h300",noImage:"https://1.bp.blogspot.com/-BYDJ1dpFEhE/X9QnAUfeORI/AAAAAAAAHxw/OjfaqiPHjhAmCgJts39XIg7o4KR-8YtdACNcBGAsYHQ/w300-h225-p-k-no-nu/dagruel-no-image.png"};
mTP.Select = ["Action", "Adventure", "Comedy", "Drama", "Ecchi", "Fantasy", "Game", "Harem", "Historical", "Isekai", "Horror", "Josei", "Magic", "Mecha", "Military", "Music", "Mystery", "Parody", "Police", "Psychological", "Romance", "Samurai", "School", "School Life", "Sci-Fi", "Seinen", "Shoujo", "Shoujo Ai", "Shounen", "Slice of Life", "Space", "Sports", "Super Power", "Supernatural", "Thriller", "Vampire", "Yuri"];
/*]]>*/</script>
    </b:if>
    <script type='text/javascript'>/*<![CDATA[*/
  const clwd={arr:new Array,compile:function(){const t=this,e=this.arr.length;t.settings.title.some(e=>t.arr[0].title.includes(e.in))||t.arr.push(t.arr.shift());let n="<ul>",s='<div class="lastend">';jQuery.each(t.arr,function(i,a){let l=a.title;if(jQuery.each(t.settings.title,function(t,e){l.includes(e.in)&&(l=e.out+" "+l.split(e.in)[1].replace(/[^0-9\.-]+/g,""))}),i==e-2&&(s+=`<div class="inepcx" data-id="1"><a href="${a.link}"><span>Chapter Awal</span><span class="epcur epcurfirst">${l}</span></a></div>`),0==i&&(s+=`<div class="inepcx" data-id="2"><a href="${a.link}"> <span>Chapter Baru</span> <span class="epcur epcurlast">${l}</span></a></div>`),i!=e-1){let t=0==a.dLink?"":`<div class="dt"> <a href="${a.dLink}" rel="nofollow" class="dload" target="_blank"><i class="fas fa-cloud-download-alt"></i></a></div>`;n+=`<li><div class="chbox"><div class="eph-num"><a href="${a.link}"><span class="chapternum">${l}</span> <span class="chapterdate">${a.published}</span></a></div>${t}</div></li>`}}),s+="</div>",n+="</ul>",document.getElementById("clwd").innerHTML=`${s+n}`},get:function(t){const e=this;t.ajax({url:`/feeds/posts/default/-/${this.settings.cat}?alt=json-in-script&start-index=${this.settings.start}&max-results=${this.settings.max}`,type:"get",dataType:"jsonp",success:function(n){"entry"in n.feed?(n.feed.entry.forEach(n=>{e.arr.push({title:n.title.$t,link:n.link.find(t=>"alternate"==t.rel).href,dLink:"content"in n&&(0!=t(n.content.$t).find("#downBTN").length&&t(n.content.$t).find("#downBTN").attr("href")),published:"function"==typeof timeAgo?timeAgo(new Date(n.updated.$t)):e.timeStirng(n.updated.$t)})}),n.feed.entry.length>=e.settings.max?(e.settings.start+=e.settings.max,e.run(e.settings.cat)):e.compile()):0!=e.arr.length&&e.compile()},error:function(t){console.log(t)}})},run:function(t){this.settings.cat=t,"function"==typeof jQuery&&document.getElementById("clwd")?this.get(jQuery):console.log("Output Nothing")},settings:{max:150,start:1,title:[{in:"Episode",out:"Ep."},{in:"Chapter",out:"Ch."},{in:"Volume",out:"Vol."}],judul:"Chapter List"},timeStirng:function(t){if(/([12]\d{3}-(0[1-9]|1[0-2])-(0[1-9]|[12]\d|3[01]))/.test(t)){var e=t,n=e.substring(0,4),s=e.substring(5,7),i=e.substring(8,10),a=new Array;return a[1]="Jan",a[2]="Feb",a[3]="Mar",a[4]="Apr",a[5]="May",a[6]="Jun",a[7]="Jul",a[8]="Aug",a[9]="Sep",a[10]="Oct",a[11]="Nov",a[12]="Dec",i+" "+a[parseInt(s,10)]+" "+n}return!1}};
/*]]>*/</script>
    <script src='https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js'/>
    <script src='//code.iconify.design/1/1.0.6/iconify.min.js'/>
    <style>
  @import url(https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css);
.rating{width: 100%;}
  .rating-prc {
  display: flex;
  justify-content: space-between;
}
.rating-prc .rtp{overflow:hidden;display:inline-block}
.rating-prc .rtp .rtb{position:relative;overflow:hidden;color:#ff0000;height:15px;line-height:1;width:85px;font-size:15px;margin:0 auto}
.fw .rating-prc .rtp .rtb {font-size:13px}
.rating-prc .rtp .rtb:before{content:&quot;\f005\f005\f005\f005\f005&quot;;font-family:&quot;Font Awesome 5 Free&quot;;position:absolute;top:0;left:0;height:15px}
.rating-prc .rtp .rtb span{overflow:hidden;top:0;left:0;position:absolute;padding-top:15px}
.rating-prc .rtp .rtb span:before{content:&quot;\f005\f005\f005\f005\f005&quot;;font-family:&quot;Font Awesome 5 Free&quot;;font-weight:900;top:0;position:absolute;left:0}
.rating-prc .num{line-height:normal;font-size:13px;color:#999}
    </style>
    <script type='text/javascript'>//<![CDATA[
const history_ = function(widget,id){
let getHistory = JSON.parse(localStorage.getItem('History')),structure = '';
if(getHistory != null && getHistory != ''){
for(let item in getHistory.reverse()){
structure += `<li class="bm_item"><a href="${getHistory[item].link}">${getHistory[item].title}</a></li>`;
}
$(id).html(structure);
}else{
$(widget).remove();
}
}
//]]></script>
    &lt;!--</head>--&gt;&lt;/head&gt;
  <body id='modeSwitch'>
    <b:class cond='data:view.isPost' name='pv'/>
    <b:class cond='data:view.isMultipleItems' name='fw'/>
    <b:class cond='data:view.isLabelSearch' name='label-view'/>
    <b:class cond='data:view.isSearch and !data:view.isLabelSearch' name='svo'/>
    <b:class cond='data:view.isPage' name='p'/>
    <script>/*<![CDATA[*/ (localStorage.getItem('mode')) === 'darkmode' ? document.querySelector('#modeSwitch').classList.add('dark-mode') : document.querySelector('#modeSwitch').classList.remove('dark-mode') /*]]>*/</script>

    <b:with value='[&quot;A&quot;,&quot;B&quot;,&quot;C&quot;,&quot;D&quot;,&quot;E&quot;,&quot;F&quot;,&quot;G&quot;,&quot;H&quot;,&quot;I&quot;,&quot;J&quot;,&quot;K&quot;,&quot;L&quot;,&quot;M&quot;,&quot;N&quot;,&quot;O&quot;,&quot;P&quot;,&quot;Q&quot;,&quot;R&quot;,&quot;S&quot;,&quot;T&quot;,&quot;U&quot;,&quot;V&quot;,&quot;W&quot;,&quot;X&quot;,&quot;Y&quot;,&quot;Z&quot;,&quot;0-9&quot;]' var='Alphabet'>
      <b:with value='[&quot;Action&quot;,&quot;Adventure&quot;,&quot;Comedy&quot;,&quot;Crime&quot;,&quot;Drama&quot;,&quot;Fantasy&quot;,&quot;Historical&quot;,&quot;Horror&quot;,&quot;Isekai&quot;,&quot;Magical Girls&quot;,&quot;Mecha&quot;,&quot;Medical&quot;,&quot;Mystery&quot;,&quot;Philosophical&quot;,&quot;Psychological&quot;,&quot;Romance&quot;,&quot;Sci-Fi&quot;,&quot;Shoujo Ai&quot;,&quot;Shounen Ai&quot;,&quot;Slice of Life&quot;,&quot;Sports&quot;,&quot;Superhero&quot;,&quot;Thriller&quot;,&quot;Tragedy&quot;,&quot;Wuxia&quot;,&quot;Yaoi&quot;,&quot;Yuri&quot;,&quot;Tsundere&quot;,&quot;Yandere&quot;]' var='Genre'>
        <b:with value='[&quot;Adaptation&quot;,&quot;Cooking&quot;,&quot;Harem&quot;,&quot;Loli&quot;,&quot;Mafia&quot;,&quot;Magic&quot;,&quot;Military&quot;,&quot;Music&quot;,&quot;Reincarnation&quot;,&quot;Reverse Harem&quot;,&quot;Samurai&quot;,&quot;School Life&quot;,&quot;Supernatural&quot;,&quot;Survival&quot;,&quot;Time Travel&quot;,&quot;Vampire&quot;,&quot;Video Games&quot;,&quot;Demon&quot;,&quot;Monsters&quot;,&quot;Martial Arts&quot;,&quot;Virtual Reality&quot;,&quot;Demons&quot;,&quot;Monster Girls&quot;,&quot;Monsters&quot;,&quot;Police&quot;]' var='Genre2'>
          <b:with value='[&quot;Shounen&quot;,&quot;Shoujo&quot;,&quot;Seinen&quot;,&quot;Josei&quot;,&quot;Mature&quot;]' var='Demographic'>
            <b:with value='[&quot;Ecchi&quot;,&quot;Gore&quot;,&quot;Sexual Violence&quot;,&quot;Smut&quot;,&quot;Series&quot;,&quot;Project&quot;]' var='Content'>
              <b:with value='[&quot;Chapter&quot;,&quot;Novel&quot;,&quot;Ongoing&quot;,&quot;Hot&quot;,&quot;New&quot;,&quot;Color&quot;]' var='Other'>
                <b:with value='[&quot;Light Novel (JP)&quot;,&quot;Web Novel (CN)&quot;,&quot;Web Novel (JP)&quot;,&quot;Web Novel (KR)&quot;,&quot;Manga&quot;,&quot;Manhua&quot;,&quot;Manhwa&quot;,&quot;Doujinshi&quot;,&quot;Long Strip&quot;,&quot;Full Color&quot;,&quot;One Shot&quot;,&quot;Web Comic&quot;,&quot;Official Colored&quot;,&quot;Jepang&quot;,&quot;Korea&quot;,&quot;Cina&quot;,&quot;Indonesia&quot;,&quot;Webtoon&quot;,&quot;Webtoons&quot;]' var='Format'>
                  <b:with value='[&quot;Ongoing&quot;,&quot;Completed&quot;,&quot;Cancelled&quot;,&quot;Hiatus&quot;,&quot;Dropped&quot;,&quot;Coming Soon&quot;]' var='Status'>
                    <b:with value='[&quot;Score 0.5&quot;,&quot;Score 1.0&quot;,&quot;Score 1.5&quot;,&quot;Score 2.0&quot;,&quot;Score 2.5&quot;,&quot;Score 3.0&quot;,&quot;Score 3.5&quot;,&quot;Score 4.0&quot;,&quot;Score 4.5&quot;,&quot;Score 5.0&quot;,&quot;Score 5.5&quot;,&quot;Score 6.0&quot;,&quot;Score 6.5&quot;,&quot;Score 7.0&quot;,&quot;Score 7.5&quot;,&quot;Score 8.0&quot;,&quot;Score 8.5&quot;,&quot;Score 9.0&quot;,&quot;Score 9.5&quot;,&quot;Score 10.0&quot;]' var='Score'>

                      <header class='bg-main'>
                        <b:section class='max-w mra mla grid gtc-header aic gg-30' growth='vertical' id='header' maxwidgets='3' showaddelement='true'>
                          <b:widget id='Header1' locked='true' title='KomikKilat (Header)' type='Header' version='2' visible='true'>
                            <b:widget-settings>
                              <b:widget-setting name='displayUrl'>https://blogger.googleusercontent.com/img/a/AVvXsEgKl2CGWk9uKKlZVRsxrXZngJ7yR8DjlDr_3K93-sn-uDeggryybOi2G_XNfgDve36vyw8qMzPEL-wcpDS4aCoSlh62VDJA5_qevrrXDz1cCx02vvM98NygSFOA1tt7JkVkUNSe26X-y1j3Wce-_e--kCh6QG63ckJWnnBEu33sHJI5-BZdIzgzQDjEsl0=s1280</b:widget-setting>
                              <b:widget-setting name='displayHeight'>640</b:widget-setting>
                              <b:widget-setting name='sectionWidth'>963</b:widget-setting>
                              <b:widget-setting name='useImage'>true</b:widget-setting>
                              <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
                              <b:widget-setting name='imagePlacement'>REPLACE</b:widget-setting>
                              <b:widget-setting name='displayWidth'>1280</b:widget-setting>
                            </b:widget-settings>
                            <b:includable id='main' var='this'>
                              <div class='menu'>
                                <button class='bn bt c-fff p-13' onclick='myMenu()'><svg style='width:24px;height:24px' viewBox='0 0 24 24'>
                                  <path d='M3,6H21V8H3V6M3,11H21V13H3V11M3,16H21V18H3V16Z' fill='currentColor'/>
                                  </svg></button>
                              </div>
                              <div class='flex aic md:jcc'>
								<b:include cond='data:imagePlacement in {&quot;REPLACE&quot;, &quot;BEFORE_DESCRIPTION&quot;}' name='image'/>
                                <b:include cond='data:imagePlacement not in {&quot;REPLACE&quot;, &quot;BEFORE_DESCRIPTION&quot;}' name='title'/>
								<b:include cond='data:imagePlacement == &quot;BEHIND&quot;' name='behindImageStyle'/>
                              </div>
                              
                            </b:includable>
                            <b:includable id='behindImageStyle'>
                              <b:if cond='data:sourceUrl'>
                                <b:include cond='data:this.image' data='{                    image: data:this.image,                    selector: &quot;.header-widget&quot;                  }' name='responsiveImageStyle'/>
                                <style type='text/css'>
                                  .header-widget {
                                  background-position: <data:blog.locale.languageAlignment/>;
                                  background-repeat: no-repeat;
                                  background-size: cover;
                                  }
                                </style>
                              </b:if>
                            </b:includable>
                            <b:includable id='description'>
                              <p>
                                <data:this.description/>
                              </p>
                            </b:includable>
                            <b:includable id='image'>
                              <a class='header-image-wrapper' expr:href='data:blog.homepageUrl'>
                                <b:include data='{                                                 image: data:image,                                                 altText: data:blog.title.escaped,                                                 originalWidth: data:width,                                                 originalHeight: data:height                                               }' name='responsiveImage'/>
                              </a>
                            </b:includable>
                            <b:includable id='title'>
                              <div class='logo flex aic'>
                                
                                <a class='c-fff fsi fs-20 fw-600 white:hover' href='/'>
                                  <data:blog.title/>
                                  <sup>v5</sup>
                                </a>
                              </div>
                            </b:includable>
                          </b:widget>
                          <b:widget id='PageList1' locked='true' title='Pages' type='PageList' version='2' visible='true'>
                            <b:widget-settings>
                              <b:widget-setting name='pageListJson'>{}</b:widget-setting>
                              <b:widget-setting name='homeTitle'>Beranda</b:widget-setting>
                            </b:widget-settings>
                            <b:includable id='main'>

                              <b:include name='content'/>
                            </b:includable>
                            <b:includable id='content'>

                              <nav class='widget-content nav-a'>
                                <b:include name='pageList'/>
                              </nav>
                            </b:includable>
                            <b:includable id='overflowButton'>
                              <b:include name='verticalMoreIcon'/>
                            </b:includable>
                            <b:includable id='overflowablePageList'>
                              <div class='overflowable-container'>
                                <div class='overflowable-contents'>
                                  <div class='container'>
                                    <b:with value='true' var='overflow'>
                                      <b:with value='&quot;tabs&quot;' var='pageListClass'>
                                        <b:include name='pageList'/>
                                      </b:with>
                                    </b:with>
                                  </div>
                                </div>
                                <div class='overflow-button hidden'>
                                  <b:include name='overflowButton'/>
                                </div>
                              </div>
                            </b:includable>
                            <b:includable id='pageLink'>
                              <li class='mx-5'>
                                <b:class cond='data:overflow' name='overflowable-item'/>
                                <b:class cond='data:link.isCurrentPage' name='selected'/>

                                <a class='block px-5 lh-37 c-fff fs-14' expr:data='data:link.title' expr:href='data:link.href'><data:link.title/></a>
                              </li>
                              
                            </b:includable>
                            <b:includable id='pageList'>
                              <ul class='flex m-0 lsn fdc pl-0'>
                                <b:class cond='data:pageListClass' expr:name='data:pageListClass'/>
                                <b:loop values='data:links' var='link'>
                                  <b:include name='pageLink'/>
                                </b:loop>                       
                                <li class='dropdown mx-5'>
                                <label class='block px-5 lh-37 c-fff fs-14' data='Other' for='dropmenu'>Other<svg aria-hidden='true' class='h-14' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 16 16' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><g fill='currentColor'><path d='M7.247 11.14L2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z'/></g></svg></label>
                                <input class='dropMenu hidden' id='dropmenu' name='dropDown' type='checkbox'/>
                                <ul class='pl-0 lsn bg-171 c-999-a p-y7x15-a block-a'>
                                  <li><a expr:href='data:blog.homepageUrl + &quot;search/label/Manga?&amp;max-results=20&quot;'>Manga</a></li>
                                  <li><a expr:href='data:blog.homepageUrl + &quot;search/label/Manhwa?&amp;max-results=20&quot;'>Manhwa</a></li>
                                  <li><a expr:href='data:blog.homepageUrl + &quot;search/label/Manhua?&amp;max-results=20&quot;'>Manhua</a></li>
                                  <li><a expr:href='data:blog.homepageUrl + &quot;search/label/Western?&amp;max-results=20&quot;'>Western</a></li>
                                </ul>
                              </li>
                              </ul>
                            </b:includable>
                          </b:widget>
                          <b:widget id='BlogSearch1' locked='true' title='Cari Blog Ini' type='BlogSearch' version='2' visible='true'>
                            <b:includable id='main'>

                              <b:include name='content'/>

                            </b:includable>
                            <b:includable id='content'>
                              <div class='flex aic' role='search'>
                                <b:include name='darkMode'/>
                                <b:include name='searchForm'/>
                                <a class='menu-item svg14 flex aic' href='https://komikkilat.blogspot.com/p/bookmark.html'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg'><path d='M5.5 3A1.5 1.5 0 0 1 7 4.5v15A1.5 1.5 0 0 1 5.5 21h-2A1.5 1.5 0 0 1 2 19.5v-15A1.5 1.5 0 0 1 3.5 3h2Zm6 0A1.5 1.5 0 0 1 13 4.5v15a1.5 1.5 0 0 1-1.5 1.5h-2A1.5 1.5 0 0 1 8 19.5v-15A1.5 1.5 0 0 1 9.5 3h2Zm7.281 3.124l3.214 12.519a1.5 1.5 0 0 1-1.08 1.826l-1.876.48a1.5 1.5 0 0 1-1.826-1.08L13.999 7.354a1.5 1.5 0 0 1 1.08-1.826l1.876-.483a1.502 1.502 0 0 1 1.826 1.08Z' fill='currentColor'/></svg><span class='sm:dn'>Bookmark</span></a>
                                <div class='search'>
                                <button class='right bn bt c-fff p-13' onclick='fungsiSearch()'><svg style='width:24px;height:24px' viewBox='0 0 24 24'>
                                  <path d='M9.5,3A6.5,6.5 0 0,1 16,9.5C16,11.11 15.41,12.59 14.44,13.73L14.71,14H15.5L20.5,19L19,20.5L14,15.5V14.71L13.73,14.44C12.59,15.41 11.11,16 9.5,16A6.5,6.5 0 0,1 3,9.5A6.5,6.5 0 0,1 9.5,3M9.5,5C7,5 5,7 5,9.5C5,12 7,14 9.5,14C12,14 14,12 14,9.5C14,7 12,5 9.5,5Z' fill='currentColor'/>
                                  </svg></button>
                              </div>
                              </div>

                            </b:includable>
                            <b:includable id='searchForm'>
                              <form class='flex mr-13 md:full r-5 oh' expr:action='data:blog.searchUrl' id='Query-input'>
                                <b:attr cond='not data:view.isPreview' name='target' value='_top'/>
                                <b:include name='urlParamsAsFormInput'/>
                                <div class='md:full'>
                                  <input autocomplete='off' class='p-y6x12 bn c-fff bg-trans tl-r3 bl-r3 w-180 box' expr:aria-label='data:messages.search' expr:placeholder='data:messages.search' expr:value='data:view.isSearch ? data:view.search.query.escaped : &quot;&quot;' name='q'/>
                                </div>
                                <b:include name='searchSubmit'/>
                              </form>
                            </b:includable>
                            <b:includable id='searchSubmit'>
                              <label class='bg-trans c-fff bn tr-r3 br-r3 cp flex aic pr-10' id='submit'>
                                <input class='hidden' expr:value='data:messages.search.escaped' type='submit'/>
                                <svg aria-hidden='true' class='svg12' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 12 12' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><g fill='none'><path d='M5 1a4 4 0 1 0 2.248 7.31l2.472 2.47a.75.75 0 1 0 1.06-1.06L8.31 7.248A4 4 0 0 0 5 1zM2.5 5a2.5 2.5 0 1 1 5 0a2.5 2.5 0 0 1-5 0z' fill='currentColor'/></g></svg>
                                
                              </label>
                              <label class='bg-trans c-fff bn tr-r3 br-r3 cp flex aic pr-10' id='close'>
                               
                                
                                <svg aria-hidden='true' height='1em' onclick='fungsiSearch()' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg'><path d='M12 22A9.99 9.99 0 0 1 2 12v-.2a10.005 10.005 0 0 1 17.074-6.874A10 10 0 0 1 12 22Zm0-8.59L14.59 16L16 14.59L13.41 12L16 9.41L14.59 8L12 10.59L9.41 8L8 9.41L10.59 12L8 14.59L9.41 16L12 13.411v-.001Z' fill='currentColor'/></svg>
                              </label>
                            </b:includable>
                          </b:widget>
                        </b:section>
                      </header>
                      <b:section growth='vertical' id='notification' maxwidgets='1' showaddelement='true'>
                        <b:widget id='Text4' locked='false' title='Global Notification' type='Text' version='2' visible='false'>
                          <b:widget-settings>
                            <b:widget-setting name='content'>Download &lt;span class=&quot;p-5 bg-171 r2&quot;&gt;&lt;a class=&quot;c-fff&quot; href=&quot;
https://protemplates.org/zeistmanga-premium-blogger-template/
&quot;&gt;ZeistManga&lt;/a&gt; v4&lt;/span&gt;</b:widget-setting>
                          </b:widget-settings>
                          <b:includable id='main'>
  <b:include name='widget-title'/>

                            <div class='aic flex gg-10 widget-content pcc'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 1024 1024' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><path d='M229.6 678.1c-3.7 11.6-5.6 23.9-5.6 36.4c0-12.5 2-24.8 5.7-36.4h-.1zm76.3-260.2H184v188.2h121.9l12.9 5.2L840 820.7V203.3L318.8 412.7z' fill='currentColor' fill-opacity='.15'/><path d='M880 112c-3.8 0-7.7.7-11.6 2.3L292 345.9H128c-8.8 0-16 7.4-16 16.6v299c0 9.2 7.2 16.6 16 16.6h101.7c-3.7 11.6-5.7 23.9-5.7 36.4c0 65.9 53.8 119.5 120 119.5c55.4 0 102.1-37.6 115.9-88.4l408.6 164.2c3.9 1.5 7.8 2.3 11.6 2.3c16.9 0 32-14.2 32-33.2V145.2C912 126.2 897 112 880 112zM344 762.3c-26.5 0-48-21.4-48-47.8c0-11.2 3.9-21.9 11-30.4l84.9 34.1c-2 24.6-22.7 44.1-47.9 44.1zm496 58.4L318.8 611.3l-12.9-5.2H184V417.9h121.9l12.9-5.2L840 203.3v617.4z' fill='currentColor'/></svg>
<p class='m-0'><data:content/></p></div>
</b:includable>
                        </b:widget>
                      </b:section>
                      <b:section class='mb-15' cond='data:view.isHomepage' id='hero' maxwidgets='2' showaddelement='true'>
                        <b:widget id='HTML3' locked='true' title='Slider' type='HTML' version='2' visible='true'>
                          <b:widget-settings>
                            <b:widget-setting name='content'>&lt;div dir=&quot;ltr&quot; id=&quot;slider&quot;&gt;
&lt;div class=&quot;slides&quot; id=&quot;slides&quot;&gt;

&lt;div class=&quot;item&quot;&gt;
&lt;a href=&quot;https://komikkilat.blogspot.com/2023/11/solo-farming-in-tower-bahasa-indonesia_26.html&quot;&gt;
&lt;div class=&quot;mainslider&quot;&gt;
&lt;div class=&quot;limit&quot;&gt;
&lt;div class=&quot;sliderinfo&quot;&gt;
&lt;div class=&quot;sliderinfolimit&quot;&gt;
&lt;div class=&quot;black-bg&quot;&gt;
&lt;span class=&quot;name&quot;&gt; Solo Farming In The Tower Bahasa Indonesia&lt;/span&gt;
&lt;div class=&quot;meta&quot;&gt;&lt;span class=&quot;quality&quot;&gt;8.7&lt;/span&gt;
&lt;span class=&quot;text&quot;&gt;Type: &lt;b&gt;Manhwa&lt;/b&gt;&lt;/span&gt; &lt;span class=&quot;text&quot;&gt;Genres: Monster, Action, Adventure, Drama&lt;/span&gt;
&lt;/div&gt;
&lt;div class=&quot;desc&quot;&gt;
&lt;p&gt;Suatu hari, sebuah menara misterius tiba-tiba muncul di kota.&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;div class=&quot;bigbanner&quot; style=&quot;background-image: url(&#39;https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi-ys8feVpHDbxKs1kR26j32-ziQccsSxY8GAT6ANMJCsZp-juvJ-A8XpW69qVD4yITGut9uome7x0FmZPhkOsH8KHY0eCfQWCvNnwMdhjHHQtdon5oseFQPqP7HVyXDp4I1fyUOEWcUUrpFcduQuFMdqH6jtWbd60taWAdRxRc61pjdbXcwelw5je5MVY/s623/solo-farming-in-the-tower.jpg&#39;);&quot;&gt;&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/a&gt;
&lt;/div&gt;






&lt;div class=&quot;item&quot;&gt;
&lt;a href=&quot;https://komikkilat.blogspot.com/2023/12/mercenary-enrollment-bahasa-indonesia.html&quot;&gt;
&lt;div class=&quot;mainslider&quot;&gt;
&lt;div class=&quot;limit&quot;&gt;
&lt;div class=&quot;sliderinfo&quot;&gt;
&lt;div class=&quot;sliderinfolimit&quot;&gt;
&lt;div class=&quot;black-bg&quot;&gt;
&lt;span class=&quot;name&quot;&gt; Mercenary Enrollment Bahasa Indonesia&lt;/span&gt;
&lt;div class=&quot;meta&quot;&gt;&lt;span class=&quot;quality&quot;&gt;7.90&lt;/span&gt;
&lt;span class=&quot;text&quot;&gt;Type: &lt;b&gt;Manhwa&lt;/b&gt;&lt;/span&gt; &lt;span class=&quot;text&quot;&gt;Genres: Action, Adventure, Drama&lt;/span&gt;
&lt;/div&gt;
&lt;div class=&quot;desc&quot;&gt;
&lt;p&gt;Yu Ijin adalah satu-satunya yang selamat dari kecelakaan pesawat saat dia masih kecil. Setelah menjadi tentara bayaran untuk bertahan hidup selama 10 tahun, ia kembali ke keluarganya di kampung halamannya.&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;div class=&quot;bigbanner&quot; style=&quot;background-image: url(&#39;https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjSHHxdIvp7lTU54e-TcGFCkJneCJAw3tgc5EEVZiyTnhzsrTJYob5ws_LlLeSZEud8861QHmRf099uKLNaniL0GXfgTJFp_s8bPx71x7AjZ8I3d2mxng2deg6gy8vrGFJ6oS0IUdIAur2Hk1XD_tdF2nKVEw-rz54YdbclBE6IMWf2wi9OEyqzRcfV17w/s620/Komik-Mercenary-Enrollment%20%281%29.jpg&#39;);&quot;&gt;&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/a&gt;
&lt;/div&gt;










&lt;/div&gt;
&lt;div id=&quot;left-button&quot;&gt;&lt;svg class=&quot;icon icon-tabler icon-tabler-arrow-narrow-left&quot; height=&quot;44&quot; viewbox=&quot;0 0 24 24&quot; width=&quot;44&quot; xmlns=&quot;http://www.w3.org/2000/svg&quot;&gt;
&lt;path d=&quot;M0 0h24v24H0z&quot; fill=&quot;none&quot; stroke=&quot;none&quot;&gt;&lt;/path&gt;
&lt;line x1=&quot;5&quot; x2=&quot;19&quot; y1=&quot;12&quot; y2=&quot;12&quot;&gt;&lt;/line&gt;
&lt;line x1=&quot;5&quot; x2=&quot;9&quot; y1=&quot;12&quot; y2=&quot;16&quot;&gt;&lt;/line&gt;
&lt;line x1=&quot;5&quot; x2=&quot;9&quot; y1=&quot;12&quot; y2=&quot;8&quot;&gt;&lt;/line&gt;
&lt;/svg&gt;&lt;/div&gt;
&lt;div id=&quot;right-button&quot;&gt;&lt;svg class=&quot;icon icon-tabler icon-tabler-arrow-narrow-right&quot; height=&quot;44&quot; viewbox=&quot;0 0 24 24&quot; width=&quot;44&quot; xmlns=&quot;http://www.w3.org/2000/svg&quot;&gt;
&lt;path d=&quot;M0 0h24v24H0z&quot; fill=&quot;none&quot; stroke=&quot;none&quot;&gt;&lt;/path&gt;
&lt;line x1=&quot;5&quot; x2=&quot;19&quot; y1=&quot;12&quot; y2=&quot;12&quot;&gt;&lt;/line&gt;
&lt;line x1=&quot;15&quot; x2=&quot;19&quot; y1=&quot;16&quot; y2=&quot;12&quot;&gt;&lt;/line&gt;
&lt;line x1=&quot;15&quot; x2=&quot;19&quot; y1=&quot;8&quot; y2=&quot;12&quot;&gt;&lt;/line&gt;
&lt;/svg&gt;&lt;/div&gt;
&lt;/div&gt;</b:widget-setting>
                          </b:widget-settings>
                          <b:includable id='main'>
                            <div class='widget-content relative'>
                              <data:content/>
                            </div>
                          </b:includable>
                        </b:widget>
                        <b:widget id='Label3' locked='true' title='Popular Genre' type='Label' version='2' visible='false'>
                          <b:widget-settings>
                            <b:widget-setting name='sorting'>FREQUENCY</b:widget-setting>
                            <b:widget-setting name='display'>CLOUD</b:widget-setting>
                            <b:widget-setting name='selectedLabelsList'>Action,Adaptation,Adventure,Comedy,Completed,Crime,Demon,Drama,Ecchi,Fantasy,Full Color,Gore,Harem,Historical,Horror,Isekai,Josei,Light Novel (JP),Mafia,Magic,Manga,Manhua,Manhwa,Martial Arts,Mature,Mecha,Military,Monsters,Mystery,Official Colored,Reincarnation,Romance,School Life,Sci-Fi,Seinen,Shounen,Slice of Life,Sports,Supernatural,Survival,Thriller,Tragedy,Video Games,Virtual Reality</b:widget-setting>
                            <b:widget-setting name='showType'>ALL</b:widget-setting>
                            <b:widget-setting name='showFreqNumbers'>true</b:widget-setting>
                          </b:widget-settings>
                          <b:includable id='main' var='this'>

                            <b:include name='content'/>
                          </b:includable>
                          <b:includable id='cloud'>
                            <span class='bc-fff y6x11p r4 c-theme' role='button'><data:title/></span>
                            <b:loop values='data:labels limit 7' var='label'>
                              <span class='p-size'>
                                <b:class expr:name='&quot;label-size-&quot; + data:label.cssSize'/>
                                <a class='label-name' expr:href='data:label.url'>
                                  <data:label.name/>
                                  <b:if cond='data:this.showFreqNumbers'>
                                    <span class='label-count o5'><data:label.count/></span>
                                  </b:if>
                                </a>
                              </span>
                            </b:loop>

                            <label aria-label='Show label' class='label-more cp' data-hide='Show less' data-show='Show more' expr:data-text='&quot;+&quot; + (data:labels.length - 4)' for='p-label' role='button'><svg class='vam fill-f' height='24' viewBox='0 0 24 24' width='24'><path d='M16,12A2,2 0 0,1 18,10A2,2 0 0,1 20,12A2,2 0 0,1 18,14A2,2 0 0,1 16,12M10,12A2,2 0 0,1 12,10A2,2 0 0,1 14,12A2,2 0 0,1 12,14A2,2 0 0,1 10,12M4,12A2,2 0 0,1 6,10A2,2 0 0,1 8,12A2,2 0 0,1 6,14A2,2 0 0,1 4,12Z'/></svg></label>
                            <input class='labelInput hidden' id='p-label' type='checkbox'/>
                            <div class='labelAll genres-list'>
                              <b:loop index='alltags' values='data:labels' var='label'>
                                <b:if cond='data:alltags &gt;= 7'>
                                  <a expr:href='data:label.url'>
                                    <span class='label-title'><data:label.name/></span>
                                    <b:if cond='data:this.showFreqNumbers'>
                                      <span class='label-count o5'><data:label.count/></span>
                                    </b:if>    
                                  </a>
                                </b:if>
                              </b:loop>
                            </div>
                          </b:includable>
                          <b:includable id='content'>
                            <div class='widget-content bg-main r2'>
                              <b:class expr:name='data:this.display + &quot;-label-widget-content&quot;'/>
                              <b:include cond='data:this.display == &quot;list&quot;' name='list'/>
                              <b:include cond='data:this.display == &quot;cloud&quot;' name='cloud'/>
                            </div>
                          </b:includable>
                          <b:includable id='list'>
                            <ul>
                              <b:loop values='data:labels' var='label'>
                                <li>
                                  <a class='label-name' expr:href='data:label.url'>
                                    <data:label.name/>
                                    <b:if cond='data:this.showFreqNumbers'>
                                      <span class='label-count'><data:label.count/></span>
                                    </b:if>
                                  </a>
                                </li>
                              </b:loop>
                            </ul>
                          </b:includable>
                        </b:widget>
                      </b:section>
                      <b:section class='max-w mla mra mb-15' cond='data:view.isHomepage' id='slide' maxwidgets='1' showaddelement='true'>
                        <b:widget cond='data:view.isHomepage' id='HTML6' locked='true' title='Ads' type='HTML' version='2' visible='true'>
                          <b:widget-settings>
                            <b:widget-setting name='content'><![CDATA[<script type='text/javascript' src='//wokm8isd4zit.com/94/52/fa/9452fa2b8819c638839af4fc0d8f7355.js'></script>]]></b:widget-setting>
                          </b:widget-settings>
                          <b:includable id='main'>
                              <b:class name='ads'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                        </b:widget>
                        <b:widget id='PopularPosts2' locked='true' title='POPULER' type='PopularPosts' version='2' visible='true'>
                          <b:widget-settings>
                            <b:widget-setting name='numItemsToShow'>10</b:widget-setting>
                            <b:widget-setting name='showThumbnails'>true</b:widget-setting>
                            <b:widget-setting name='showSnippets'>true</b:widget-setting>
                            <b:widget-setting name='timeRange'>LAST_WEEK</b:widget-setting>
                          </b:widget-settings>
                          <b:includable id='main' var='this'>
                            <div class='releases p-y0x15 flex relative jcsb'>
                              <h3 class='c-fff lh-20 fw-500 p-y5x20 fs-15 bg-222 flex aic yt8m r4'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg'><path d='M17.66 11.2c-.23-.3-.51-.56-.77-.82c-.67-.6-1.43-1.03-2.07-1.66C13.33 7.26 13 4.85 13.95 3c-.95.23-1.78.75-2.49 1.32c-2.59 2.08-3.61 5.75-2.39 8.9c.04.1.08.2.08.33c0 .22-.15.42-.35.5c-.23.1-.47.04-.66-.12a.58.58 0 0 1-.14-.17c-1.13-1.43-1.31-3.48-.55-5.12C5.78 10 4.87 12.3 5 14.47c.06.5.12 1 .29 1.5c.14.6.41 1.2.71 1.73c1.08 1.73 2.95 2.97 4.96 3.22c2.14.27 4.43-.12 6.07-1.6c1.83-1.66 2.47-4.32 1.53-6.6l-.13-.26c-.21-.46-.77-1.26-.77-1.26m-3.16 6.3c-.28.24-.74.5-1.1.6c-1.12.4-2.24-.16-2.9-.82c1.19-.28 1.9-1.16 2.11-2.05c.17-.8-.15-1.46-.28-2.23c-.12-.74-.1-1.37.17-2.06c.19.38.39.76.63 1.06c.77 1 1.98 1.44 2.24 2.8c.04.14.06.28.06.43c.03.82-.33 1.72-.93 2.27Z' fill='#ff2800'/></svg><data:title/></h3>
                              <div class='flex aic wh-18-svg gg-10'>
                                <div class='c-fff' id='prev'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><path d='M4.431 12.822l13 9A1 1 0 0 0 19 21V3a1 1 0 0 0-1.569-.823l-13 9a1.003 1.003 0 0 0 0 1.645z' fill='currentColor'/></svg></div>
                                <div class='c-fff' id='next'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><path d='M5.536 21.886a1.004 1.004 0 0 0 1.033-.064l13-9a1 1 0 0 0 0-1.644l-13-9A1 1 0 0 0 5 3v18a1 1 0 0 0 .536.886z' fill='currentColor'/></svg>
                                </div>

                              </div>
                              </div>
                            <div class='grid gtc-f141a gg-20 slide widget-content scroll ul'>
                              <b:include name='snippetedPosts'/>
                            </div>
                         
                          </b:includable>
                          <b:includable id='blogThisShare'>
                            <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=270,width=475\&quot;); return false;&quot;' var='onclick'>
                              <b:include name='platformShare'/>
                            </b:with>
                          </b:includable>
                          <b:includable id='bylineByName' var='byline'>
                            <b:switch var='data:byline.name'>
                              <b:case value='share'/>
                              <b:include cond='data:post.shareUrl' name='postShareButtons'/>
                              <b:case value='comments'/>
                              <b:include cond='data:post.allowComments' name='postCommentsLink'/>
                              <b:case value='location'/>
                              <b:include cond='data:post.location' name='postLocation'/>
                              <b:case value='timestamp'/>
                              <b:include cond='not data:view.isPage' name='postTimestamp'/>
                              <b:case value='author'/>
                              <b:include name='postAuthor'/>
                              <b:case value='labels'/>
                              <b:include cond='data:post.labels' name='postLabels'/>
                              <b:case value='icons'/>
                              <b:include cond='data:post.emailPostUrl' name='emailPostIcon'/>
                              <b:case value='reactions'/>
                              <b:include cond='data:post.reactionsUrl' name='postReactions'/>
                            </b:switch>
                          </b:includable>
                          <b:includable id='bylineRegion' var='regionItems'>
                            <b:loop values='data:regionItems' var='byline'>
                              <b:include data='byline' name='bylineByName'/>
                            </b:loop>
                          </b:includable>
                          <b:includable id='commentsLink'>
                            <a class='comment-link' expr:href='data:post.commentsUrl' expr:onclick='data:post.commentsUrlOnclick'>
                              <b:if cond='data:post.numberOfComments &gt; 0'>
                                <b:message name='messages.numberOfComments'>
                                  <b:param expr:value='data:post.numberOfComments' name='numComments'/>
                                </b:message>
                                <b:else/>
                                <data:messages.postAComment/>
                              </b:if>
                            </a>
                          </b:includable>
                          <b:includable id='commentsLinkIframe'>
                            <!-- G+ comments, no longer available. The includable is retained for backwards-compatibility. -->
                          </b:includable>
                          <b:includable id='emailPostIcon'>
                            <span class='byline post-icons'>
                              <!-- email post links -->
                              <span class='item-action'>
                                <a expr:href='data:post.emailPostUrl' expr:title='data:messages.emailPost'>
                                  <b:include data='{ iconClass: &quot;touch-icon sharing-icon&quot; }' name='emailIcon'/>
                                </a>
                              </span>
                            </span>
                          </b:includable>
                          <b:includable id='facebookShare'>
                            <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=430,width=640\&quot;); return false;&quot;' var='onclick'>
                              <b:include name='platformShare'/>
                            </b:with>
                          </b:includable>
                          <b:includable id='footerBylines'>
                            <b:if cond='data:widgets.Blog.first.footerBylines'>
                              <b:loop index='i' values='data:widgets.Blog.first.footerBylines' var='region'>
                                <b:if cond='not data:region.items.empty'>
                                  <div expr:class='&quot;post-footer-line post-footer-line-&quot; + (data:i + 1)'>
                                    <b:with value='&quot;footer-&quot; + (data:i + 1)' var='regionName'>
                                      <b:include data='region.items' name='bylineRegion'/>
                                    </b:with>
                                  </div>
                                </b:if>
                              </b:loop>
                            </b:if>
                          </b:includable>
                          <b:includable id='googlePlusShare'>
                            <div class='goog-inline-block google-plus-share-container'>
                              <g:plusone annotation='inline' expr:href='data:originalUrl.canonical.http' size='medium' source='blogger:blog:plusone'/>
                            </div>
                          </b:includable>
                          <b:includable id='headerByline'>
                            <b:if cond='data:widgets.Blog.first.headerByline'>
                              <div class='post-header'>
                                <div class='post-header-line-1'>
                                  <b:with value='&quot;header-1&quot;' var='regionName'>
                                    <b:include data='data:widgets.Blog.first.headerByline.items' name='bylineRegion'/>
                                  </b:with>
                                </div>
                              </div>
                            </b:if>
                          </b:includable>
                          <b:includable id='linkShare'>
                            <b:with value='&quot;window.prompt(\&quot;Copy to clipboard: Ctrl+C, Enter\&quot;, \&quot;&quot; + data:originalUrl + &quot;\&quot;); return false;&quot;' var='onclick'>
                              <b:include name='platformShare'/>
                            </b:with>
                          </b:includable>
                          <b:includable id='otherSharingButton'>
                            <span class='sharing-platform-button sharing-element-other' expr:aria-label='data:messages.shareToOtherApps.escaped' expr:data-url='data:originalUrl' expr:title='data:messages.shareToOtherApps.escaped' role='menuitem' tabindex='-1'>
                              <b:with value='{key: &quot;sharingOther&quot;}' var='platform'>
                                <b:include name='sharingPlatformIcon'/>
                              </b:with>
                              <span class='platform-sharing-text'><data:messages.shareOtherApps.escaped/></span>
                            </span>
                          </b:includable>
                          <b:includable id='platformShare'>
                            <a expr:class='&quot;goog-inline-block sharing-&quot; + data:platform.key' expr:data-url='data:originalUrl' expr:href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:onclick='data:onclick ? data:onclick : &quot;&quot;' expr:title='data:platform.shareMessage' target='_blank'>
                              <span class='share-button-link-text'>
                                <data:platform.shareMessage/>
                              </span>
                            </a>
                          </b:includable>
                          <b:includable id='postAuthor'>
                            <span class='byline post-author vcard'>
                              <span class='post-author-label'>
                                <data:byline.label/>
                              </span>
                              <span class='fn'>
                                <b:if cond='data:post.author.profileUrl'>
                                  <meta expr:content='data:post.author.profileUrl'/>
                                  <a class='g-profile' expr:href='data:post.author.profileUrl' rel='author' title='author profile'>
                                    <span><data:post.author.name/></span>
                                  </a>
                                  <b:else/>
                                  <span><data:post.author.name/></span>
                                </b:if>
                              </span>
                            </span>
                          </b:includable>
                          <b:includable id='postCommentsLink'>
                            <span class='byline post-comment-link container'>
                              <b:include cond='data:post.commentSource != 1' name='commentsLink'/>
                            </span>
                          </b:includable>
                          <b:includable id='postJumpLink' var='post'>
                            <div class='jump-link flat-button'>
                              <a expr:href='data:post.url fragment &quot;more&quot;' expr:title='data:post.title'>
                                <b:eval expr='data:blog.jumpLinkMessage'/>
                              </a>
                            </div>
                          </b:includable>
                          <b:includable id='postLabels'>
                            <span class='byline post-labels'>
                              <span class='byline-label'><data:byline.label/></span>
                              <b:loop index='i' values='data:post.labels' var='label'>
                                <a expr:href='data:label.url' rel='tag'>
                                  <data:label.name/>
                                </a>
                              </b:loop>
                            </span>
                          </b:includable>
                          <b:includable id='postLocation'>
                            <span class='byline post-location'>
                              <data:byline.label/>
                              <a expr:href='data:post.location.mapsUrl' target='_blank'><data:post.location.name/></a>
                            </span>
                          </b:includable>
                          <b:includable id='postReactions'>
                            <span class='byline reactions'>
                              <span class='reactions-label'>
                                <data:byline.label/>
                              </span>
                              <iframe allowtransparency='true' class='reactions-iframe' expr:src='data:post.reactionsUrl' frameborder='0' name='reactions' scrolling='no'/>
                            </span>
                          </b:includable>
                          <b:includable id='postShareButtons'>
                            <div class='byline post-share-buttons goog-inline-block'>
                              <b:with value='data:sharingId ?: ((data:widget.instanceId ?: &quot;sharing&quot;) + &quot;-&quot; + (data:regionName ?: &quot;byline&quot;) + &quot;-&quot; + data:post.id)' var='sharingId'>
                                <!-- Note: 'sharingButtons' includable is from the default Sharing widget markup. -->
                                <b:include data='{                                                sharingId: data:sharingId,                                                originalUrl: data:post.url,                                                platforms: data:this.sharing.platforms,                                                shareUrl: data:post.shareUrl,                                                shareTitle: data:post.title,                                              }' name='sharingButtons'/>
                              </b:with>
                            </div>
                          </b:includable>
                          <b:includable id='postTimestamp'>
                            <span class='byline post-timestamp'>
                              <data:byline.label/>
                              <b:if cond='data:post.url'>
                                <meta expr:content='data:post.url.canonical'/>
                                <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'>
                                  <time class='published' expr:datetime='data:post.date.iso8601' expr:title='data:post.date.iso8601'>
                                    <data:post.date/>
                                  </time>
                                </a>
                              </b:if>
                            </span>
                          </b:includable>
                          <b:includable id='sharingButton'>
                            <span expr:aria-label='data:platform.shareMessage' expr:class='&quot;sharing-platform-button sharing-element-&quot; + data:platform.key' expr:data-href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:data-url='data:originalUrl' expr:title='data:platform.shareMessage' role='menuitem' tabindex='-1'>
                              <b:include name='sharingPlatformIcon'/>
                              <span class='platform-sharing-text'><data:platform.name/></span>
                            </span>
                          </b:includable>
                          <b:includable id='sharingButtonContent'>
                            <div class='flat-icon-button ripple'>
                              <b:include name='shareIcon'/>
                            </div>
                          </b:includable>
                          <b:includable id='sharingButtons'>
                            <div class='sharing' expr:aria-owns='&quot;sharing-popup-&quot; + data:sharingId' expr:data-title='data:shareTitle'>
                              <button class='sharing-button touch-icon-button' expr:aria-controls='&quot;sharing-popup-&quot; + data:sharingId' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-button-&quot; + data:sharingId' role='button'>
                                <b:include name='sharingButtonContent'/>
                              </button>
                              <b:include name='sharingButtonsMenu'/>
                            </div>
                          </b:includable>
                          <b:includable id='sharingButtonsMenu'>
                            <div class='share-buttons-container'>
                              <ul aria-hidden='true' class='share-buttons hidden' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-popup-&quot; + data:sharingId' role='menu'>
                                <b:loop values='(data:platforms ?: data:blog.sharing.platforms) filter (p =&gt; p.key not in {&quot;blogThis&quot;})' var='platform'>
                                  <li>
                                    <b:include name='sharingButton'/>
                                  </li>
                                </b:loop>
                                <li aria-hidden='true' class='hidden'>
                                  <b:include name='otherSharingButton'/>
                                </li>
                              </ul>
                            </div>
                          </b:includable>
                          <b:includable id='sharingPlatformIcon'>
                            <b:include data='{ iconClass: (&quot;touch-icon sharing-&quot; + data:platform.key) }' expr:name='data:platform.key + &quot;Icon&quot;'/>
                          </b:includable>
                          <b:includable id='snippetedPostByline'>
                            <b:with value='(data:widgets first (w =&gt; w.type == &quot;Blog&quot;)).allBylineItems' var='blogBylines'>
                              <div class='item-byline'>
                                <b:with value='data:blogBylines first (i =&gt; i.name == &quot;author&quot;)' var='byline'>
                                  <b:include cond='data:byline and data:this.postDisplay.showAuthor' data='post' name='postAuthor'/>
                                </b:with>
                                <b:with value='data:blogBylines first (i =&gt; i.name == &quot;timestamp&quot;)' var='byline'>
                                  <b:include cond='data:byline and data:this.postDisplay.showDate' data='post' name='postTimestamp'/>
                                </b:with>
                              </div>
                            </b:with>
                          </b:includable>
                          <b:includable id='snippetedPostContent'>
                            <b:include cond='data:this.postDisplay.showFeaturedImage and data:post.featuredImage' name='snippetedPostThumbnail'/>
                            <b:include name='snippetedPostTitle'/>
                          </b:includable>
                          <b:includable id='snippetedPostThumbnail'>
                            <div class='full-i h-220 relative b-img oh'>
                              <a class='block' expr:href='data:post.url'>
                                <b:include data='{                         image: data:post.featuredImage,                         imageSizes: [141, 198],                         imageRatio: &quot;1:2&quot;,                         sourceSizes: &quot;198px&quot;                        }' name='responsiveImage'/>
                              </a>
                              <b:include name='Category'/>
                              <b:include name='cfs'/>
                            </div>
                          </b:includable>
                          <b:includable id='snippetedPostTitle'>
                            <b:if cond='data:post.title != &quot;&quot;'>
                              
                                <figcaption><a class='clamp toe oh block fs-15 lh-20 mt8 ck' expr:href='data:post.url'><data:post.title/></a>
                               <div class='flex aic jcsb yt8m'>
                                <b:include name='Status'/>
                                <b:include name='postEnclosures'/>
                                </div>
                              <b:include name='ScoreMultiItem'/>
                              </figcaption>
                              
                            </b:if>
                            
                          </b:includable>
                          <b:includable id='snippetedPosts'>
                            <b:with value='data:posts filter (p =&gt; p.labels none (l =&gt; l.name == &quot;Chapter&quot;))' var='posts'>
                              <!-- Don't render the post that we're currently already looking at. -->
                              <b:loop index='i' values='data:posts filter (p =&gt; p.id != data:view.postId)' var='post'>
                                <b:with value='data:i + 1' var='num'>
                                  <figure class='link:hover sac' expr:id='&quot;s&quot; + data:num'>
                                    <b:include name='snippetedPostContent'/>
                                  </figure>
                                </b:with>
                              </b:loop>
                              
                            </b:with>
                          </b:includable>
                        </b:widget>
                      </b:section>
                      <main class='mla mra grid gg-20 relative mx-feed mt-sv15'>
                        <b:class cond='data:view.isMultipleItems and !data:view.isLabelSearch' name='gtc-main'/>
                        <b:tag class='grid gg-20 gtr-mc min' cond='data:view.isMultipleItems' name='section'>
                        <b:section class='grid gg-15' cond='data:view.isHomepage' id='feed' showaddelement='true'>
                          <b:widget id='HTML9' locked='false' title='Project Update' type='HTML' version='2' visible='false'>
                            <b:widget-settings>
                              <b:widget-setting name='content'>&lt;div id=&quot;Update&quot; class=&quot;myGridv2&quot;&gt;
  &lt;script&gt;update.run(&#39;Project&#39;, 150)&lt;/script&gt;
&lt;/div&gt;</b:widget-setting>
                            </b:widget-settings>
                            <b:includable id='main'>
  <h3 class='title flex aic jcsb'>
    <span class='flex aic g5'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 2048 1408' width='1.46em' xmlns='http://www.w3.org/2000/svg'><path d='M1024 384H640v384h384V384zm128 640v128H512v-128h640zm0-768v640H512V256h640zm640 768v128h-512v-128h512zm0-256v128h-512V768h512zm0-256v128h-512V512h512zm0-256v128h-512V256h512zM256 1216V256H128v960q0 26 19 45t45 19t45-19t19-45zm1664 0V128H384v1088q0 33-11 64h1483q26 0 45-19t19-45zM2048 0v1216q0 80-56 136t-136 56H192q-80 0-136-56T0 1216V128h256V0h1792z' fill='currentColor'/></svg>
    <data:title/></span>
    <a class='bg-main ttu p-3y6x fs-9 r2 c-fff' href='/search/label/Update'>View All</a>
</h3>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                          </b:widget>
                          <b:widget id='HTML13' locked='false' title='Latest Release' type='HTML' version='2' visible='true'>
                            <b:widget-settings>
                              <b:widget-setting name='content'>&lt;div id=&quot;myManga&quot; class=&quot;myGrid&quot;&gt;
  &lt;script&gt;mangaPost.run(&#39;Project&#39;, 150)&lt;/script&gt;
&lt;/div&gt;</b:widget-setting>
                            </b:widget-settings>
                            <b:includable id='main'>
  <h3 class='title flex jcsb aic'>
    <span class='flex aic g5'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><g fill='none'><path d='M12.552 8a1 1 0 1 0 0 2h4a1 1 0 1 0 0-2h-4z' fill='currentColor' fill-opacity='.5'/><path d='M12.552 17a1 1 0 1 0 0 2h4a1 1 0 1 0 0-2h-4z' fill='currentColor' fill-opacity='.5'/><path d='M12.552 5a1 1 0 1 0 0 2h8a1 1 0 1 0 0-2h-8z' fill='currentColor' fill-opacity='.8'/><path d='M12.552 14a1 1 0 1 0 0 2h8a1 1 0 1 0 0-2h-8z' fill='currentColor' fill-opacity='.8'/><path d='M3.448 4.002a1 1 0 0 0-1 1v5a1 1 0 0 0 1 1h5a1 1 0 0 0 1-1v-5a1 1 0 0 0-1-1h-5z' fill='currentColor'/><path d='M3.448 12.998a1 1 0 0 0-1 1v5a1 1 0 0 0 1 1h5a1 1 0 0 0 1-1v-5a1 1 0 0 0-1-1h-5z' fill='currentColor'/></g></svg>
      <data:title/></span>
    <a class='bg-main ttu p-3y6x fs-9 r2 c-fff' href='#'>View All</a>
</h3>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                          </b:widget>
                          <b:widget id='HTML11' locked='false' title='Chat' type='HTML' version='2' visible='true'>
                            <b:widget-settings>
                              <b:widget-setting name='content'><![CDATA[<script id="cid0020000363175860127" data-cfasync="false" async="async" src="//st.chatango.com/js/gz/emb.js" style="width: 250px;height: 350px;" >{"handle":"kilatkomik","arch":"js","styles":{"a":"CC0000","b":100,"c":"FFFFFF","d":"FFFFFF","k":"CC0000","l":"CC0000","m":"CC0000","n":"FFFFFF","p":"10","q":"CC0000","r":100,"fwtickm":1}}</script>]]></b:widget-setting>
                            </b:widget-settings>
                            <b:includable id='main'>
  <h3 class='title flex aic'>
    <svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><path d='M4 16h16V7.9A5 5 0 0 1 14.1 4H4v12z' fill='currentColor' opacity='.3'/><path d='M20 7.9c.74-.15 1.42-.48 2-.92V16c0 1.1-.9 2-2 2H6l-4 4V4c0-1.1.9-2 2-2h10.1c-.06.32-.1.66-.1 1s.04.68.1 1H4v12h16V7.9zM16 3c0 1.66 1.34 3 3 3s3-1.34 3-3s-1.34-3-3-3s-3 1.34-3 3z' fill='currentColor'/></svg>
<data:title/>
</h3>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                          </b:widget>
                          <b:widget cond='data:view.isHomepage' id='HTML14' locked='false' title='About' type='HTML' version='2' visible='true'>
                            <b:widget-settings>
                              <b:widget-setting name='content'>KomikKilat merupakan situs baca komik online dengan koleksi terlengkap dan terupdate. Kamu bisa membaca ribuan koleksi komik yang kami update setiap hari secara gratis. Memiliki desain yang responsif dan modern, website ini adalah tempat terbaik untuk kalian yang ingin Baca Manga terbaru, Manhwa (komik Korea) dan Manhua (komik China).</b:widget-setting>
                            </b:widget-settings>
                            <b:includable id='main'>
  <h3 class='title flex aic'>
    <svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><path d='M12 4c-4.41 0-8 3.59-8 8s3.59 8 8 8s8-3.59 8-8s-3.59-8-8-8zm1 13h-2v-6h2v6zm0-8h-2V7h2v2z' fill='currentColor' opacity='.3'/><path d='M11 7h2v2h-2zm0 4h2v6h-2zm1-9C6.48 2 2 6.48 2 12s4.48 10 10 10s10-4.48 10-10S17.52 2 12 2zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8s8 3.59 8 8s-3.59 8-8 8z' fill='currentColor'/></svg>
<data:title/>
</h3>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                          </b:widget>
                          <b:widget id='HTML15' locked='false' title='Manhwa' type='HTML' version='2' visible='false'>
                            <b:widget-settings>
                              <b:widget-setting name='content'>&lt;div id=&quot;myProject2&quot; class=&quot;myGrid&quot;&gt;
  &lt;script&gt;bookPost2.run(&#39;Project&#39;, 150)&lt;/script&gt;
&lt;/div&gt;</b:widget-setting>
                            </b:widget-settings>
                            <b:includable id='main'>
  <h3 class='title flex aic'>
    <svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 20 20' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><g fill='none'><rect height='10' rx='3' stroke='currentColor' stroke-linecap='round' stroke-width='2' transform='rotate(33.038 12.784 2.384)' width='6' x='12.784' y='2.384'/><rect height='10' rx='3' stroke='currentColor' stroke-linecap='round' stroke-width='2' transform='rotate(33.038 7.836 6.323)' width='6' x='7.836' y='6.323'/></g></svg>
<data:title/>
</h3>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                          </b:widget>
                          <b:widget id='HTML16' locked='false' title='Fantasy' type='HTML' visible='false'>
                            <b:widget-settings>
                              <b:widget-setting name='content'>&lt;div class=&quot;grid gtc-142 gg-20&quot;  id=&quot;customPost5&quot;&gt;
  &lt;script type=&quot;text/javascript&quot;&gt;
    customPost.run(&#39;customPost5&#39;, &#39;Fantasy&#39;, 6);
  &lt;/script&gt;
&lt;/div&gt;</b:widget-setting>
                            </b:widget-settings>
                            <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                          </b:widget>
                        </b:section>
                        <b:section class='grid gg-20 mb-15' id='main' showaddelement='true'>
                          <b:widget id='HTML12' locked='false' title='' type='HTML' visible='true'>
                            <b:widget-settings>
                              <b:widget-setting name='content'>&lt;script type=&quot;text/javascript&quot;&gt;
	atOptions = {
		&#39;key&#39; : &#39;69ac9c0ed5647d10df8819090b3fa563&#39;,
		&#39;format&#39; : &#39;iframe&#39;,
		&#39;height&#39; : 60,
		&#39;width&#39; : 468,
		&#39;params&#39; : {}
	};
	document.write(&#39;&lt;scr&#39; + &#39;ipt type=&quot;text/javascript&quot; src=&quot;//wokm8isd4zit.com/69ac9c0ed5647d10df8819090b3fa563/invoke.js&quot;&gt;&lt;/scr&#39; + &#39;ipt&gt;&#39;);
&lt;/script&gt;</b:widget-setting>
                            </b:widget-settings>
                            <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                          </b:widget>
                          <b:widget cond='!data:view.isHomepage' id='Blog1' locked='true' title='Postingan Blog' type='Blog' version='2' visible='true'>
                            <b:widget-settings>
                              <b:widget-setting name='commentLabel'>Komentar</b:widget-setting>
                              <b:widget-setting name='showShareButtons'>true</b:widget-setting>
                              <b:widget-setting name='authorLabel'>Oleh</b:widget-setting>
                              <b:widget-setting name='style.unittype'>TextAndImage</b:widget-setting>
                              <b:widget-setting name='timestampLabel'>Pada</b:widget-setting>
                              <b:widget-setting name='reactionsLabel'/>
                              <b:widget-setting name='showAuthorProfile'>false</b:widget-setting>
                              <b:widget-setting name='style.layout'>1x1</b:widget-setting>
                              <b:widget-setting name='showLocation'>false</b:widget-setting>
                              <b:widget-setting name='showTimestamp'>true</b:widget-setting>
                              <b:widget-setting name='postsPerAd'>1</b:widget-setting>
                              <b:widget-setting name='style.bordercolor'>#ffffff</b:widget-setting>
                              <b:widget-setting name='showDateHeader'>false</b:widget-setting>
                              <b:widget-setting name='style.textcolor'>#ffffff</b:widget-setting>
                              <b:widget-setting name='showCommentLink'>true</b:widget-setting>
                              <b:widget-setting name='style.urlcolor'>#ffffff</b:widget-setting>
                              <b:widget-setting name='postLocationLabel'>Location:</b:widget-setting>
                              <b:widget-setting name='showAuthor'>true</b:widget-setting>
                              <b:widget-setting name='style.linkcolor'>#ffffff</b:widget-setting>
                              <b:widget-setting name='style.bgcolor'>#ffffff</b:widget-setting>
                              <b:widget-setting name='showLabels'>true</b:widget-setting>
                              <b:widget-setting name='postLabelsLabel'>Like</b:widget-setting>
                              <b:widget-setting name='showBacklinks'>false</b:widget-setting>
                              <b:widget-setting name='showInlineAds'>false</b:widget-setting>
                              <b:widget-setting name='showReactions'>false</b:widget-setting>
                            </b:widget-settings>
                            <b:includable id='main' var='this'>
                              <b:class cond='!data:view.isHomepage' name='not-home-mb20'/>
                              <b:if cond='data:posts.empty'>
                                <div class='no-posts-message bg-main c-fff p-10 r4'><b:eval expr='data:view.isSearch ? data:messages.noResultsFound : data:messages.theresNothingHere'/></div>
                              </b:if>
                              <b:with value='data:widgets.FeaturedPost filter (w =&gt; w.sectionId == &quot;main&quot;) map (w =&gt; w.postId)' var='featuredPostIds'>
                                <b:with value='data:view.isHomepage ? data:posts filter (post =&gt; post.id not in data:featuredPostIds): data:posts' var='posts'>

                                  <b:if cond='data:view.isHomepage'>
                                    <b:with value='data:posts filter (p =&gt; p.labels none (l =&gt; l.name in [&quot;Chapter&quot;,&quot;Episode&quot;,&quot;Novel&quot;]))' var='posts'>   
                                      <b:tag class='r2 s1 bc-fff' name='section'>
                                        <b:include name='dataMessages'/>
                                        <b:tag class='grid gg-20 hfeed p-13' name='div'>
                                          <b:loop index='i' values='data:posts' var='post'>

                                            <b:include data='post' name='Series'/>

                                          </b:loop>
                                        </b:tag>
                                      </b:tag>
                                    </b:with>
                                  </b:if>
                                  <b:if cond='data:view.isSingleItem'>
                                    <b:loop index='i' values='data:posts' var='post'>
                                      <b:if cond='data:post.labels any (l =&gt; l.name == &quot;Chapter&quot;)'>
                                        <b:include data='post' name='postChapter'/>
                                        <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Novel&quot;)'/> 
                                        <b:include data='post' name='postNovel'/>
                                        <b:else/>
                                        <b:include data='post' name='postCommentsAndAd'/>
                                      </b:if>
                                    </b:loop>
                                  </b:if>
                                  <b:if cond='data:view.isSearch and !data:view.isLabelSearch'>
                                    <b:with value='data:posts filter (p =&gt; p.labels none (l =&gt; l.name in [&quot;Chapter&quot;,&quot;Novel&quot;]))' var='posts'>
                                      <b:include name='viewAll'/>
                                    </b:with>
                                  </b:if>
                                </b:with>
                              </b:with>
                              <b:if cond='data:view.isLabelSearch'>
                                <section class='r2 s1 bc-fff mt-24'>
                                  <b:include name='dataMessages'/>
                                  <div class='grid gtc-f141a gg-20 p-13'>
                                    <b:loop index='i' values='data:posts' var='post'>
                                      <b:include cond='data:post.labels any ( l =&gt; l.name in [&quot;Series&quot;,&quot;Chapter&quot;] )' name='Series'/>
                                    </b:loop>
                                  </div>
                                  <b:include name='postPagination'/>
                                </section>
                              </b:if>
                            </b:includable>
                            <b:includable id='Disqus' var='post'>
                             <div class='bc-fff r2 s1 a4'> 
<h2 class='c-theme m-0 bb-1pxsf y9x19p fs-15 flex aic'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 48 48' width='1em' xmlns='http://www.w3.org/2000/svg'><mask id='svgIDa'><g fill='none' stroke='#fff' stroke-linecap='round' stroke-width='4'><path d='M33 38H22v-8h14v-8h8v16h-5l-3 3l-3-3Z' stroke-linejoin='round'/><path d='M4 6h32v24H17l-4 4l-4-4H4V6Z' fill='#555' stroke-linejoin='round'/><path d='M12 22h6m-6-8h12'/></g></mask><path d='M0 0h48v48H0z' fill='currentColor' mask='url(#svgIDa)'/></svg>Komentar</h2>
          <script>
          let disqus_config = () =&gt; {
          this.page.url = &#39;<data:post.url.canonical/>&#39;;
          this.page.identifier = &#39;<data:post.id/>&#39;;
          }
          const disqusLaz = (e) =&gt; {
          if (!e.classList.contains(&#39;loaded&#39;)) {
          let script = document.createElement(&#39;script&#39;);
          script.src = &#39;//scanslation.disqus.com/embed.js&#39;;
          document.body.appendChild(script);
          e.classList.add(&#39;loaded&#39;);
          }
          }
        </script>
        <div id='disqus_thread'>
          <div class='flex jcc'>
            <div id='buttonDisqs' onclick='disqusLaz(this)' role='button'>Show Comments</div>
          </div>
        </div>

</div>
        </b:includable>
                            <b:includable id='Series'>  
                              <div>
                                <div class='b-img full-i i-mage oh relative'>
                                  <a class='block pt-140p' expr:href='data:post.url'>
                                    <b:include data='{                         image: data:post.featuredImage,                         imageSizes: [141, 198],                         imageRatio: &quot;1:2&quot;,                         sourceSizes: &quot;198px&quot;                        }' name='responsiveImage'/>
                                  </a>
                                  <b:include name='Category'/>
                                  <b:include name='cfs'/>
                                </div>    
                                <a class='clamp toe oh block fs-15 lh-20 mt8 ck fw-600' expr:href='data:post.url'><data:post.title/></a>
                                <div class='flex aic jcsb yt8m'>
                                <b:include name='Status'/>
                                <b:include name='postEnclosures'/>
                                </div>
                                <b:include name='ScoreMultiItem'/>
                              </div>
                            </b:includable>
                            <b:includable id='aboutPostAuthor'>
                              <div class='author-name'>
                                <a class='g-profile' expr:href='data:post.author.profileUrl' rel='author' title='author profile'>
                                  <span>
                                    <data:post.author.name/>
                                  </span>
                                </a>
                              </div>
                              <div>
                                <span class='author-desc'>
                                  <data:post.author.aboutMe/>
                                </span>
                              </div>
                            </b:includable>
                            <b:includable id='addComments'>
                              <a expr:href='data:post.commentsUrl' expr:onclick='data:post.commentsUrlOnclick'>
                                <b:message name='messages.postAComment'/>
                              </a>
                            </b:includable>
                            <b:includable id='blogThisShare'>
                              <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=270,width=475\&quot;); return false;&quot;' var='onclick'>
                                <b:include name='platformShare'/>
                              </b:with>
                            </b:includable>
                            <b:includable id='breadCrumb' var='post'>
                              <div class='bc-fff r2 oh s1 p-y10x15 fs-14'>
                                <ol class='lsn m-0 pl-0 m-y0x4-li fw-600 fs-13' itemscope='itemscope' itemtype='http://schema.org/BreadcrumbList'>
                                  <li class='i-block' itemprop='itemListElement' itemscope='itemscope' itemtype='http://schema.org/ListItem'>
                                    <a expr:href='data:blog.homepageUrl' itemprop='item'><span itemprop='name'><data:blog.title/></span></a>
                                    <meta content='1' itemprop='position'/>
                                  </li>
                                  &#8250;
                                  <li class='i-block' itemprop='itemListElement' itemscope='itemscope' itemtype='http://schema.org/ListItem'>
                                    <a expr:href='data:post.url' itemprop='item'><span itemprop='name'><data:post.title/></span></a>
                                    <meta content='2' itemprop='position'/>
                                  </li>
                                </ol>
                              </div>
                </b:includable>
                            <b:includable id='bylineByName' var='byline'>
                              <b:switch var='data:byline.name'>
                                <b:case value='share'/>
                                <b:include cond='data:post.shareUrl' name='postShareButtons'/>
                                <b:case value='comments'/>
                                <b:include cond='data:post.allowComments' name='postCommentsLink'/>
                                <b:case value='location'/>
                                <b:include cond='data:post.location' name='postLocation'/>
                                <b:case value='timestamp'/>
                                <b:include cond='not data:view.isPage' name='postTimestamp'/>
                                <b:case value='author'/>
                                <b:include name='postAuthor'/>
                                <b:case value='labels'/>
                                <b:include cond='data:post.labels' name='postLabels'/>
                                <b:case value='icons'/>
                                <b:include cond='data:post.emailPostUrl' name='emailPostIcon'/>
                                <b:case value='reactions'/>
                                <b:include cond='data:post.reactionsUrl' name='postReactions'/>
                              </b:switch>
                            </b:includable>
                            <b:includable id='bylineRegion' var='regionItems'>
                              <b:loop values='data:regionItems' var='byline'>
                                <b:include data='byline' name='bylineByName'/>
                              </b:loop>
                            </b:includable>
                            <b:includable id='chapNextPrev'>
                                <b:loop values='data:post.labels' var='label'>
                                  <b:if cond='data:label.name not in [&quot;Chapter&quot;, &quot;Project&quot;]'>
                                    <div id='nPL'>
                                      <script>nPL.run(&#39;<data:label.name/>&#39;)</script>
                                    </div>
                                  </b:if>
                                </b:loop>
                            </b:includable>
                            <b:includable id='chapNextPrev-bottom'>
                                <b:loop values='data:post.labels' var='label'>
                                  <b:if cond='data:label.name not in [&quot;Chapter&quot;, &quot;Project&quot;]'>
                                    <div class='flex aic jcsb mt-15' id='nPL2'>
                                      <script>nPL2.run(&#39;<data:label.name/>&#39;)</script>
                                    </div>
                                  </b:if>
                                </b:loop>
                            </b:includable>
                            <b:includable id='chapterTags'>
                            <div class='chaptertags mb-15 bc-22 r2 fs-13'>
<b:with value='[&quot;Chapter&quot;,&quot;Project&quot;]' var='chf'>
                              <p class='p-y10x15'>Tags: baca manga <b:loop index='i' values='data:post.labels' var='label'><b:if cond='data:label.name not in data:chf'><data:label.name/></b:if></b:loop> <data:post.title/> bahasa Indonesia, komik <b:loop index='i' values='data:post.labels' var='label'><b:if cond='data:label.name not in data:chf'><data:label.name/></b:if></b:loop> <data:post.title/> bahasa komik Indonesia, baca <data:post.title/> online, <data:post.title/> baru komiku, <b:loop index='i' values='data:post.labels' var='label'><b:if cond='data:label.name not in data:chf'><data:label.name/></b:if></b:loop> <data:post.title/> chapter, high quality sub indo, <b:loop index='i' values='data:post.labels' var='label'><b:if cond='data:label.name not in data:chf'><data:label.name/></b:if></b:loop> manga scan terbaru, manhwa web, <time expr:datetime='data:post.date.iso8601' expr:title='data:post.date.iso8601'><data:post.date/></time>, <span><data:post.author.name/></span></p>
                              </b:with>
</div>
                            </b:includable>
                            <b:includable id='commentAuthorAvatar'>
                              <div class='avatar-image-container'>
                                <img class='author-avatar' expr:src='data:comment.authorAvatarSrc' height='35' width='35'/>
                              </div>
                            </b:includable>
                            <b:includable id='commentDeleteIcon' var='comment'>
                              <span expr:class='&quot;item-control &quot; + data:comment.adminClass'>
                                <b:if cond='data:showCmtPopup'>
                                  <div class='goog-toggle-button'>
                                    <div class='goog-inline-block comment-action-icon'/>
                                  </div>
                                  <b:else/>
                                  <a class='comment-delete' expr:href='data:comment.deleteUrl' expr:title='data:messages.deleteComment'>
                                    <img src='https://resources.blogblog.com/img/icon_delete13.gif'/>
                                  </a>
                                </b:if>
                              </span>
                            </b:includable>
                            <b:includable id='commentForm' var='post'>
                              <div class='comment-form'>
                                <a name='comment-form'/>
                                <b:if cond='data:this.messages.blogComment != &quot;&quot;'>
                                  <p class='alr royal p-15 ml-20 mr-20'><data:this.messages.blogComment/></p>
                                </b:if>
                                <b:include data='post' name='commentFormIframeSrc'/>
                                <iframe allowtransparency='allowtransparency' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight ?: &quot;90px&quot;' frameborder='0' id='comment-editor' name='comment-editor' src='' width='100%'/>
                                <data:post.cmtfpIframe/>
                                <script type='text/javascript'>
                                  BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;);
                                </script>
                              </div>
                            </b:includable>
                            <b:includable id='commentFormIframeSrc' var='post'>
                              <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
                            </b:includable>
                            <b:includable id='commentItem' var='comment'>
                              <div class='comment' expr:id='&quot;c&quot; + data:comment.id'>
                                <b:include cond='data:blog.enabledCommentProfileImages' name='commentAuthorAvatar'/>

                                <div class='comment-block'>
                                  <div class='comment-author'>
                                    <b:if cond='data:comment.authorUrl'>
                                      <b:message name='messages.authorSaidWithLink'>
                                        <b:param expr:value='data:comment.author' name='authorName'/>
                                        <b:param expr:value='data:comment.authorUrl' name='authorUrl'/>
                                      </b:message>
                                      <b:else/>
                                      <b:message name='messages.authorSaid'>
                                        <b:param expr:value='data:comment.author' name='authorName'/>
                                      </b:message>
                                    </b:if>
                                  </div>
                                  <div expr:class='&quot;comment-body&quot; + (data:comment.isDeleted ? &quot; deleted&quot; : &quot;&quot;)'>
                                    <data:comment.body/>
                                  </div>
                                  <div class='comment-footer'>
                                    <span class='comment-timestamp'>
                                      <a expr:href='data:comment.url' title='comment permalink'>
                                        <data:comment.timestamp/>
                                      </a>
                                      <b:include data='comment' name='commentDeleteIcon'/>
                                    </span>
                                  </div>
                                </div>
                              </div>
                            </b:includable>
                            <b:includable id='commentList' var='comments'>
                              <div id='comments-block'>
                                <b:loop values='data:comments' var='comment'>
                                  <b:include data='comment' name='commentItem'/>
                                </b:loop>
                              </div>
                            </b:includable>
                            <b:includable id='commentPicker' var='post'>
                              <b:if cond='data:post.showThreadedComments'>
                                <b:include data='post' name='threadedComments'/>
                                <b:else/>
                                <b:include data='post' name='threadedComments'/> 
                              </b:if>
                            </b:includable>
                            <b:includable id='commentblock' var='cb'>
                  <div class='avatar-image-container'>
                    <div>
                      <b:if cond='data:cb.level.authorAvatarSrc != &quot;//resources.blogblog.com/img/blank.gif&quot;'>
                        <img class='post-thumb lazy' expr:alt='data:cb.level.author' expr:data-src='resizeImage(data:cb.level.authorAvatarSrc, 100, &quot;1:1&quot;)' expr:title='data:cb.level.author' src='data:image/png;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs='/>
                      </b:if>
                    </div>
                  </div>
                  
                  <div class='comment-block' itemscope='itemscope' itemtype='https://schema.org/Comment'>
                    <div class='comment-header'>
                      <b:if cond='data:cb.level.author != &quot;Anonymous&quot;'>
                        <span class='user' itemprop='author' itemscope='itemscope' itemtype='https://schema.org/Person'>
                          <span itemprop='name'><data:cb.level.author/></span>                          
                          <b:if cond='data:post.author.name == data:cb.level.author'>
                            <svg class='icon blog-author' viewBox='0 0 24 24'><path d='M12,2A10,10 0 0,1 22,12A10,10 0 0,1 12,22A10,10 0 0,1 2,12A10,10 0 0,1 12,2M11,16.5L18,9.5L16.59,8.09L11,13.67L7.91,10.59L6.5,12L11,16.5Z'/></svg>
                          </b:if>
                        </span>
                      </b:if>
                      <span class='datetime secondary-text' itemprop='datePublished'>
                        <a expr:href='&quot;#c&quot; + data:cb.level.id' itemprop='url'>
                          <data:cb.level.timestamp/>
                        </a>
                      </span>
                    </div>

                     <div class='comment-content' itemprop='text'>
                       <!--<b:if cond='data:cb.level.authorUrl != data:post.author.profileUrl'>-->
                         <b:eval expr='data:cb.level.body snippet { links: false }'/>
                         <!--<b:else/>
                         <data:cb.level.body/>
                       </b:if>-->
                    </div>
                    
                  </div>
                  
                  <!--<b:if cond='data:cb.d and data:commentL2.size != &quot;2&quot;'>
                    <div class='comment-actions secondary-text'>
                      <a class='comment-reply reply-to' expr:data-comment-id='data:commentLevel1.id' expr:data-reply-to='data:commentLevel1.id' href='javascript:;' target='_self'>Balas</a>
                      <span expr:class='&quot;item-control &quot; + data:cb.level.adminClass'>
                        <a expr:href='data:cb.level.deleteUrl' expr:title='data:messages.deleteComment' rel='noopener external nofollow' target='_self'>Hapus</a>
                      </span>
                    </div>
                  </b:if>-->
                </b:includable>
                            <b:includable id='comments' var='post'>
                              <section expr:class='&quot;bc-fff r2 s1 a4 oh comments&quot; + (data:post.embedCommentForm ? &quot; embed&quot; : &quot;&quot;)' expr:data-num-comments='data:post.numberOfComments' id='comments'>
                                <b:include name='commentsTitle'/>
                                <a name='comments'/>
                                <b:if cond='data:post.allowComments'>
                                  <div expr:id='data:widget.instanceId + &quot;_comments-block-wrapper&quot;'>
                                    <b:include cond='data:post.comments' data='post.comments' name='commentList'/>
                                  </div>

                                  <b:if cond='data:post.commentPagingRequired'>
                                    <div class='paging-control-container'>
                                      <b:if cond='data:post.hasOlderLinks'>
                                        <a expr:class='data:post.oldLinkClass' expr:href='data:post.oldestLinkUrl'>
                                          <data:messages.oldest/>
                                        </a>
                                        <a expr:class='data:post.oldLinkClass' expr:href='data:post.olderLinkUrl'>
                                          <data:messages.older/>
                                        </a>
                                      </b:if>

                                      <span class='comment-range-text'>
                                        <data:post.commentRangeText/>
                                      </span>

                                      <b:if cond='data:post.hasNewerLinks'>
                                        <a expr:class='data:post.newLinkClass' expr:href='data:post.newerLinkUrl'>
                                          <data:messages.newer/>
                                        </a>
                                        <a expr:class='data:post.newLinkClass' expr:href='data:post.newestLinkUrl'>
                                          <data:messages.newest/>
                                        </a>
                                      </b:if>
                                    </div>
                                  </b:if>

                                  <div class='footer'>
                                    <b:if cond='data:post.embedCommentForm'>
                                      <b:if cond='data:post.allowNewComments'>
                                        <b:include data='post' name='commentForm'/>
                                        <b:else/>
                                        <data:post.noNewCommentsText/>
                                      </b:if>
                                      <b:else/>
                                      <b:if cond='data:post.allowComments'>
                                        <b:include data='post' name='addComments'/>
                                      </b:if>
                                    </b:if>
                                    <b:if cond='data:post.showManageComments'>
                                      <b:include data='post' name='manageComments'/>
                                    </b:if>
                                  </div>
                                </b:if>
                                <b:if cond='data:showCmtPopup'>
                                  <div id='comment-popup'>
                                    <iframe allowtransparency='allowtransparency' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'>
                                    </iframe>
                                  </div>
                                </b:if>
                              </section>
                            </b:includable>
                            <b:includable id='commentsLink'>
                              <a class='comment-link' expr:href='data:post.commentsUrl' expr:onclick='data:post.commentsUrlOnclick'>
                                <b:if cond='data:post.numberOfComments &gt; 0'>
                                  <b:message name='messages.numberOfComments'>
                                    <b:param expr:value='data:post.numberOfComments' name='numComments'/>
                                  </b:message>
                                  <b:else/>
                                  <data:messages.postAComment/>
                                </b:if>
                              </a>
                            </b:includable>
                            <b:includable id='commentsLinkIframe'>
                              <!-- G+ comments, no longer available. The includable is retained for backwards-compatibility. -->
                            </b:includable>
                            <b:includable id='commentsTitle'>
                              <div class='flex jcsb aic bb-1pxsf y9x19p'>
                              <h2 class='c-theme m-0 fs-15 flex aic'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><path d='M20 17.17V4H4v12h14.83L20 17.17zM18 14H6v-2h12v2zm0-3H6V9h12v2zm0-3H6V6h12v2z' fill='currentColor' opacity='.3'/><path d='M4 18h14l4 4l-.01-18c0-1.1-.89-2-1.99-2H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2zM4 4h16v13.17L18.83 16H4V4zm2 8h12v2H6zm0-3h12v2H6zm0-3h12v2H6z' fill='currentColor'/></svg><data:messages.comments/> (<data:post.numberOfComments/>)</h2>
                                <label aria-label='' class='s' data-new='Newest' data-text='Oldest' for='forAllCm'/>
                              </div>
                            </b:includable>
                            <b:includable id='dataChapterTitle'>
                              <div class='flex aic jcsb bb-1pxsf y9x19p'>
                                <h3 class='m-0 c-theme'>
                                  <b:if cond='data:view.isHomepage'><data:messages.latestPosts/></b:if>
                                  <b:if cond='data:view.search.query'><data:messages.search/>: <b><data:view.search.query/></b></b:if>
                                  <b:if cond='data:view.search.label'>Daftar Chapter Manga <b><data:blog.pageName/></b></b:if>
                                  <b:if cond='data:view.isArchive'><data:messages.blogArchive/>: <b><data:blog.pageName/></b></b:if>
                                  <b:if cond='data:view.search and !data:view.search.label and !data:view.search.query and !data:view.isArchive'><data:messages.posts/></b:if>
                                </h3>
                              </div>
                            </b:includable>
                            <b:includable id='dataMessages'>
                              <div class='flex aic jcsb bb-1pxsf y9x19p yb10m'>
                                  <h3 class='m-0 c-theme'><b:if cond='data:view.isHomepage'><data:messages.latestPosts/></b:if>
                                    <b:if cond='data:view.search.query'><data:messages.search/>: <b><data:view.search.query/></b></b:if>
                                    <b:if cond='data:view.search.label'>Rekomendasi Komik <b><data:blog.pageName/></b> Terbaik</b:if>
                                    <b:if cond='data:view.isArchive'>Arsip Komik Tanggal: <b><data:blog.pageName/></b></b:if>
                                    <b:if cond='data:view.search and !data:view.search.label and !data:view.search.query and !data:view.isArchive'><data:messages.posts/></b:if></h3>
                                  <svg class='feather feather-filter' fill='none' height='24' id='toggle' stroke='var(--primary-color)' stroke-linecap='round' stroke-linejoin='round' stroke-width='2' viewBox='0 0 24 24' width='24' xmlns='http://www.w3.org/2000/svg'><polygon points='22 3 2 3 10 12.46 10 19 14 21 14 12.46 22 3'/></svg>
                                </div>
                                <div class='p-20 bc-e8' id='content'>
                                  <dl>
                                    <dt class='pb-15 fs-15 fw-600'>Status</dt>
                                    <div class='flex fs-13 fdc'>
                                      <dd class='md-ml-0'><a expr:href='data:blog.homepageUrl + &quot;search/label/Ongoing?&amp;max-results=20&quot;'>Ongoing</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Completed?&amp;max-results=20&quot;'>Completed</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Cancelled?&amp;max-results=20&quot;'>Cancelled</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Hiatus?&amp;max-results=20&quot;'>Hiatus</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Dropped?&amp;max-results=20&quot;'>Dropped</a></dd>
                                    </div>
                                  </dl>
                                  <dl>
                                    <dt class='pb-15 fs-15 fw-600'>Format</dt>
                                    <div class='flex fs-13 fdc'>
                                      <dd class='md-ml-0'><a expr:href='data:blog.homepageUrl + &quot;search/label/Manga?&amp;max-results=20&quot;'>Manga</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Manhua?&amp;max-results=20&quot;'>Manhua</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Manhwa?&amp;max-results=20&quot;'>Manhwa</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Web Novel (JP)?&amp;max-results=20&quot;'>Web Novel (JP)</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Web Novel (KR)?&amp;max-results=20&quot;'>Web Novel (KR)</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Web Novel (CN)?&amp;max-results=20&quot;'>Web Novel (CN)</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Doujinshi?&amp;max-results=20&quot;'>Doujinshi</a></dd>
                                    </div>
                                  </dl>

                                </div>
                            </b:includable>
                            <b:includable id='defaultAdUnit'>
                              <ins class='adsbygoogle' data-ad-format='auto' expr:data-ad-client='data:adClientId ?: data:blog.adsenseClientId' expr:data-ad-host='data:blog.adsenseHostId' expr:data-analytics-uacct='data:blog.analyticsAccountNumber' expr:style='data:style ?: &quot;display: block;&quot;'/>
                              <script>
                                (adsbygoogle = window.adsbygoogle || []).push({});
                              </script>
                            </b:includable>
                            <b:includable id='dlBox'>
                              <b:if cond='data:view.isPost'>
                                <b:include name='select_chapter'/>
                              </b:if>
                             <b:comment> 
                               <div id='cl'/>
                               <div id='there'/>
                              </b:comment>
                            </b:includable>
                            <b:includable id='emailPostIcon'>
                              <span class='byline post-icons'>
                                <!-- email post links -->
                                <span class='item-action'>
                                  <a expr:href='data:post.emailPostUrl' expr:title='data:messages.emailPost'>
                                    <b:include data='{ iconClass: &quot;touch-icon sharing-icon&quot; }' name='emailIcon'/>
                                  </a>
                                </span>
                              </span>
                            </b:includable>
                            <b:includable id='facebookShare'>
                              <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=430,width=640\&quot;); return false;&quot;' var='onclick'>
                                <b:include name='platformShare'/>
                              </b:with>
                            </b:includable>
                            <b:includable id='feedHome'>
                              <div class='gtc-101 gg-10 grid'>
                                <a class='block relative' expr:href='data:post.link ?: data:post.url'>
                                  <b:if cond='data:post.featuredImage'>
                                    <b:with value='data:post.featuredImage.isResizable ? resizeImage(data:post.featuredImage, 200, &quot;1:2&quot;) : data:post.thumbnail' var='image'>
                                      <img class='h-135 full block ofc oh' expr:alt='data:post.title' expr:src='data:image'/>
                                    </b:with>
                                    <b:else/>
                                    <img class='h-200 full ofc' expr:alt='data:post.title' src='https://1.bp.blogspot.com/-h2nZWROnFpg/X4P2w57lrKI/AAAAAAAAGZo/OVOgTRFPsS420HyhTIAcKXQAm1YjlX-7gCLcBGAsYHQ/s300/default-placeholder-image-300x300.png'/>
                                  </b:if>
                                  <b:include name='Category'/>

                                </a>

                                <div>
                                  <a class='clamp toe oh block fs-15 lh-20 mb-6 ck' expr:href='data:post.url'>

                                    <b:if cond='data:post.labels any (l =&gt; l.name == &quot;Hot&quot;)'>
                                      <span class='hot'/>
                                    </b:if>
                                    <b:if cond='data:post.labels any (l =&gt; l.name == &quot;New&quot;)'>
                                      <span class='new'/>
                                    </b:if>
                                    <data:post.title/></a>
                                  <div class='flex jcsb c-666 fs-13 bt-2sf'>

                                    <b:loop values='data:post.labels' var='label'>
                                      <b:if cond='data:label.name not in data:Status and data:label.name not in data:Score and data:label.name not in data:Other and data:label.name not in data:Other and data:label.name not in data:Genre and data:label.name not in data:Genre2 and data:label.name not in data:Alphabet and data:label.name not in data:Format and data:label.name not in data:Demographic and data:label.name not in data:Content'>


                                        <script expr:src='&quot;/feeds/posts/default/-/&quot; + data:label.name + &quot;?orderby=published&amp;alt=json-in-script&amp;start-index=2&amp;callback=rcentbytag&quot;'/>

                                      </b:if>
                                    </b:loop>
                                  </div>

                                </div>
                              </div>
                            </b:includable>
                            <b:includable id='feedLinks'>
                              <b:if cond='!data:view.isPost'> <!-- Blog feed links -->
                                <b:if cond='data:feedLinks'>
                                  <div class='blog-feeds'>
                                    <b:include data='feedLinks' name='feedLinksBody'/>
                                  </div>
                                </b:if>
                                <b:else/> <!--Post feed links -->
                                <div class='post-feeds'>
                                  <b:loop values='data:posts' var='post'>
                                    <b:if cond='data:post.allowComments and data:post.feedLinks'>
                                      <b:include data='post.feedLinks' name='feedLinksBody'/>
                                    </b:if>
                                  </b:loop>
                                </div>
                              </b:if>
                            </b:includable>
                            <b:includable id='feedLinksBody' var='links'>
                              <div class='feed-links'>
                                <data:messages.subscribeTo/>
                                <b:loop values='data:links' var='f'>
                                  <a class='feed-link' expr:href='data:f.url' expr:type='data:f.mimeType' target='_blank'><data:f.name/> (<data:f.feedType/>)</a>
                                </b:loop>
                              </div>
                            </b:includable>
                            <b:includable id='figure'>
                              <figure class='grid min gg-10 mb-15'>
                                <a class='md-auto' expr:href='data:post.link ?: data:post.url'>
                                  <b:with value='data:post.featuredImage.isResizable ? resizeImage(data:post.featuredImage, 600, &quot;1:2&quot;) : data:post.thumbnail' var='image'>
                                    <img class='full r2 md-w120' expr:alt='data:post.title' expr:src='data:image'/>
                                  </b:with>
                                </a>

                              </figure>
                            </b:includable>
                            <b:includable id='footerBylines'>
                              <b:if cond='data:widgets.Blog.first.footerBylines'>
                                <b:loop index='i' values='data:widgets.Blog.first.footerBylines' var='region'>
                                  <b:if cond='not data:region.items.empty'>
                                    <div expr:class='&quot;post-footer-line post-footer-line-&quot; + (data:i + 1)'>
                                      <b:with value='&quot;footer-&quot; + (data:i + 1)' var='regionName'>
                                        <b:include data='region.items' name='bylineRegion'/>
                                      </b:with>
                                    </div>
                                  </b:if>
                                </b:loop>
                              </b:if>
                            </b:includable>
                            <b:includable id='googlePlusShare'>
                              <div class='goog-inline-block google-plus-share-container'>
                                <g:plusone annotation='inline' expr:href='data:originalUrl.canonical.http' size='medium' source='blogger:blog:plusone'/>
                              </div>
                            </b:includable>
                            <b:includable id='headerByline'>
                              <b:if cond='data:widgets.Blog.first.headerByline'>
                                <div class='post-header'>
                                  <div class='post-header-line-1'>
                                    <b:with value='&quot;header-1&quot;' var='regionName'>
                                      <b:include data='data:widgets.Blog.first.headerByline.items' name='bylineRegion'/>
                                    </b:with>
                                  </div>
                                </div>
                              </b:if>
                            </b:includable>
                            <b:includable id='homePageLink'>
                              <a class='home-link' expr:href='data:blog.homepageUrl'>
                                <data:messages.home/>
                              </a>
                            </b:includable>
                            <b:includable id='iframeComments' var='post'>
                              <!-- G+ comments, no longer available. The includable is retained for backwards-compatibility. -->
                            </b:includable>
                            <b:includable id='inlineAd' var='post'>
                              <b:if cond='!data:view.isPreview'>
                                <b:if cond='data:this.adCode or data:this.adClientId or data:blog.adsenseClientId'>
                                  <!-- Ad -->
                                  <div class='inline-ad'>
                                    <b:if cond='data:this.adCode != &quot;&quot;'>
                                      <data:this.adCode/>
                                      <b:else/>
                                      <b:include cond='data:this.adClientId or data:blog.adsenseClientId' name='defaultAdUnit'/>
                                    </b:if>
                                  </div>
                                </b:if>
                                <b:else/>
                                <div class='inline-ad'>
                                  <div class='inline-ad-placeholder'>
                                    <span><b:message name='messages.adsGoHere'/></span>
                                  </div>
                                </div>
                              </b:if>
                            </b:includable>
                            <b:includable id='linkShare'>
                              <b:with value='&quot;window.prompt(\&quot;Copy to clipboard: Ctrl+C, Enter\&quot;, \&quot;&quot; + data:originalUrl + &quot;\&quot;); return false;&quot;' var='onclick'>
                                <b:include name='platformShare'/>
                              </b:with>
                            </b:includable>
                            <b:includable id='manageComments'>
                              <a expr:href='data:post.manageCommentsUrl' expr:onclick='data:post.manageCommentsUrlOnclick'>
                                <b:message name='messages.manageComments'/>
                              </a>
                            </b:includable>
                            <b:includable id='nextPageLink'>
                              <a class='blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' expr:title='data:messages.olderPosts'>
                                <data:messages.olderPosts/>
                              </a>
                            </b:includable>
                            <b:includable id='otherSharingButton'>
                              <span class='sharing-platform-button sharing-element-other' expr:aria-label='data:messages.shareToOtherApps.escaped' expr:data-url='data:originalUrl' expr:title='data:messages.shareToOtherApps.escaped' role='menuitem' tabindex='-1'>
                                <b:with value='{key: &quot;sharingOther&quot;}' var='platform'>
                                  <b:include name='sharingPlatformIcon'/>
                                </b:with>
                                <span class='platform-sharing-text'><data:messages.shareOtherApps.escaped/></span>
                              </span>
                            </b:includable>
                            <b:includable id='page'>
                              <div class='bc-fff max-w mb-15 mla mra r2 s1 mt-24 full'>
                                <h1 class='c-theme m-0 bb-1pxsf y9x19p fs-20 flex jcsb'><data:post.title/>
                                  <b:if cond='data:view.url == data:blog.homepageUrl path &quot;/p/bookmark.html&quot;'>
                                <div class='clearAll flex aic'>Clear All</div>
                                </b:if>
                                </h1>
                                <div class='bc-fff s1 r2 p-13'>
                                <data:post.body/>
                                </div>
                              </div>
                              </b:includable>
                            <b:includable id='platformShare'>
                              <a expr:class='&quot;goog-inline-block sharing-&quot; + data:platform.key' expr:data-url='data:originalUrl' expr:href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:onclick='data:onclick ? data:onclick : &quot;&quot;' expr:title='data:platform.shareMessage' target='_blank'>
                                <span class='share-button-link-text'>
                                  <data:platform.shareMessage/>
                                </span>
                              </a>
                            </b:includable>
                            <b:includable id='post' var='post'>
                              <script>histories.addHistory(&quot;<data:post.id/>&quot;,&quot;<data:post.title/>&quot;,&quot;<data:post.url/>&quot;);</script>
                              <b:if cond='data:view.isPost'>
                                <b:if cond='data:widgets.Blog.first.posts.first.featuredImage'>
                                  <b:include data='{                                  image: data:widgets.Blog.first.posts.first.featuredImage,                                  selector: &quot;.hero-background&quot;                                }' name='responsiveImageStyle'/>
                                  <div class='bg-photo-container' id='myhero'>
                                    <div class='hero-background'/>
                                  </div>
                                </b:if>
                              </b:if>
                              <div class='grid gtc-235fr max-w mra mla mtn150 relative gg-15'> 
                                <div class='a1'>
                                  <b:include name='figure'/>
                                  <div class='hartomy-bookmark-btn bg-main bookmark' data-quantity='1' expr:data-borkimage='resizeImage(data:post.featuredImage, 400, &quot;16:9&quot;)' expr:data-id='data:post.id' expr:data-link='data:post.url' expr:data-title='data:post.title'>Bookmark <svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 16 16' width='1em' xmlns='http://www.w3.org/2000/svg'><path d='M1 3.25C1 2.56 1.56 2 2.249 2h.5c.69 0 1.248.56 1.248 1.25v9.495c0 .69-.559 1.25-1.248 1.25h-.5A1.25 1.25 0 0 1 1 12.744V3.249ZM2.249 3a.25.25 0 0 0-.25.25v9.495c0 .138.112.25.25.25h.5a.25.25 0 0 0 .25-.25V3.249a.25.25 0 0 0-.25-.25h-.5Zm2.748.25c0-.69.559-1.25 1.249-1.25h.5c.689 0 1.248.56 1.248 1.25v9.495c0 .69-.56 1.25-1.249 1.25h-.5a1.25 1.25 0 0 1-1.248-1.25V3.249ZM6.246 3a.25.25 0 0 0-.25.25v9.495c0 .138.112.25.25.25h.5a.25.25 0 0 0 .249-.25V3.249a.25.25 0 0 0-.25-.25h-.5Zm5.726 1.777a1.249 1.249 0 0 0-1.57-.713l-.583.204a1.25 1.25 0 0 0-.746 1.645l2.937 7.304c.249.62.94.933 1.571.713l.582-.204a1.25 1.25 0 0 0 .746-1.646l-2.937-7.303Zm-1.24.23a.25.25 0 0 1 .313.143l2.937 7.303a.25.25 0 0 1-.149.33l-.582.203a.25.25 0 0 1-.314-.142L10 5.54a.25.25 0 0 1 .149-.329l.582-.204Z' fill='currentColor'/></svg></div>

                                  <b:include name='ScoreMultiItem'/>
                                  <b:if cond='data:post.numberOfComments gt &quot;0&quot;'>
                                    <div class='progress-custom mb-15'>
                                      <div class='progress bc-fff s1'>
                                        <div aria-valuemax='100' aria-valuemin='0' aria-valuenow='70' class='progress-bar' expr:style='&quot;width:calc(100% / 15 * &quot; + data:post.numberOfComments + &quot;)&quot;' role='progressbar'><b:eval expr='100 / 15 * data:post.numberOfComments'/></div>
                                      </div>
                                    </div>
                                  </b:if>
                                  <aside class='s1 bc-fff r2 fs-14 lh-1d7 oh'>
                                    <div class='y6x11p'>Status <span class='dt'>
                                      <b:loop index='i' values='data:post.labels' var='label'>
                                        <b:if cond='data:label.name in data:Status'>
                                          <a expr:data='data:label.name' expr:href='data:label.url' rel='tag'>
                                            <data:label.name/>
                                          </a>
                                        </b:if>
                                      </b:loop>
                                      </span></div>
                                    <div class='y6x11p'>Type <span class='dt'>
                                      <b:loop index='i' values='data:post.labels' var='label'>
                                        <b:if cond='data:label.name in data:Format'>
                                          <a expr:data='data:label.name' expr:href='data:label.url' rel='tag'>
                                            <data:label.name/>
                                          </a>
                                        </b:if>
                                      </b:loop>
                                      </span></div>
                                    <div id='extra-target'/>
                                    <div class='y6x11p'>Posted By <span class='dt'><data:post.author.name/></span></div>
                                    <div class='y6x11p'>Post <time class='dt' expr:datetime='data:post.date.iso8601' expr:title='data:post.date.iso8601'><data:post.date/></time></div>
                                    <div class='y6x11p'>Update <time class='dt timeago' expr:datetime='data:post.lastUpdated.iso8601' expr:title='data:post.lastUpdated.iso8601'><data:post.lastUpdated.jsonEscaped/></time></div>
                                  </aside>
                                  <div id='character-target'/>
                                </div>
                                <article class='oh a2'>
                                  <div class='fs-15 s1 p-20 bc-fff r2'>
                                    <header>
                                      <b:include data='post' name='postTitle'/>
                                      <p class='m-0 c-999 fs-14'><data:blog.metaDescription/></p>
                                    </header>
                                    <div class='mt-15'>
                                      <b:include name='postLabels'/>
                                    </div>
                                    <article>
                                      <h2 class='fs-15'>Baca <data:post.title/></h2>
                                      <div id='syn-target'/>
                                      <p class='fs-14'>Baca Komik <strong><data:post.title/></strong> bahasa Indonesia lengkap dan baru di <strong><data:blog.title/></strong>. Kami menyediakan Komik, Manhua, Manhwa, dan Novel yang dapat kalian baca online gratis. </p>   
                                    </article>

                                  </div>                               
                                  <b:include cond='data:view.isPost' name='postShareButtons'/>
                                  <!-- Show ad outside post container (between posts) for feed pages. -->
                                  <b:include cond='data:view.isMultipleItems and data:post.includeAd' data='post' name='inlineAd'/>
                                  <!-- <b:include data='post' name='inlineAd2'/> -->
                                  
                                  <b:include data='post' name='postBody'/>
                                  <b:include data='post' name='breadCrumb'/>
                                </article>
                                <b:include name='relatedPost'/>
                                <!-- Comments -->
                                <b:include data='post' name='commentPicker'/>
                              </div>
                            </b:includable>
                            <b:includable id='postAuthor'>
                              <span class='byline post-author vcard'>
                                <span class='post-author-label'>
                                  <data:byline.label/>
                                </span>
                                <span class='fn'>
                                  <b:if cond='data:post.author.profileUrl'>
                                    <meta expr:content='data:post.author.profileUrl'/>
                                    <a class='g-profile' expr:href='data:post.author.profileUrl' rel='author' title='author profile'>
                                      <span><data:post.author.name/></span>
                                    </a>
                                    <b:else/>
                                    <span><data:post.author.name/></span>
                                  </b:if>
                                </span>
                              </span>
                            </b:includable>
                            <b:includable id='postBody' var='post'>

                              <b:if cond='data:post.labels any ( l =&gt; l.name in [&quot;Ecchi&quot;, &quot;Gore&quot;, &quot;Sexual Violence&quot;, &quot;Smut&quot;] )'>
                                <div class='alr grid aic p-15'><svg class='scale-2' viewBox='0 0 24 24'>
                                  <path d='M12 2C11.5 2 11 2.19 10.59 2.59L2.59 10.59C1.8 11.37 1.8 12.63 2.59 13.41L10.59 21.41C11.37 22.2 12.63 22.2 13.41 21.41L21.41 13.41C22.2 12.63 22.2 11.37 21.41 10.59L13.41 2.59C13 2.19 12.5 2 12 2M11 7H13V13H11V7M11 15H13V17H11V15Z' fill='currentColor'/>
                                  </svg> <p class='m-0'>Warning, the series titled &quot;<strong><data:post.title/></strong>&quot; may contain violence, blood or sexual content that is not appropriate for minors.</p></div>
                              </b:if>
                              
                              <b:if cond='data:post.labels any ( l =&gt; l.name in [&quot;Warning&quot;] )'>
                                <div class='alr grid aic p-15' style='background-color: purple;'><svg aria-hidden='true' class='scale-2' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg'><path d='M21.993 7.95a.96.96 0 0 0-.029-.214c-.007-.025-.021-.049-.03-.074c-.021-.057-.04-.113-.07-.165c-.016-.027-.038-.049-.057-.075c-.032-.045-.063-.091-.102-.13c-.023-.022-.053-.04-.078-.061c-.039-.032-.075-.067-.12-.094c-.004-.003-.009-.003-.014-.006l-.008-.006l-8.979-4.99a1.002 1.002 0 0 0-.97-.001l-9.021 4.99c-.003.003-.006.007-.011.01l-.01.004c-.035.02-.061.049-.094.073c-.036.027-.074.051-.106.082c-.03.031-.053.067-.079.102c-.027.035-.057.066-.079.104c-.026.043-.04.092-.059.139c-.014.033-.032.064-.041.1a.975.975 0 0 0-.029.21c-.001.017-.007.032-.007.05V16c0 .363.197.698.515.874l8.978 4.987l.001.001l.002.001l.02.011c.043.024.09.037.135.054c.032.013.063.03.097.039a1.013 1.013 0 0 0 .506 0c.033-.009.064-.026.097-.039c.045-.017.092-.029.135-.054l.02-.011l.002-.001l.001-.001l8.978-4.987c.316-.176.513-.511.513-.874V7.998c0-.017-.006-.031-.007-.048zm-10.021 3.922L5.058 8.005L7.82 6.477l6.834 3.905l-2.682 1.49zm.048-7.719L18.941 8l-2.244 1.247l-6.83-3.903l2.153-1.191zM13 19.301l.002-5.679L16 11.944V15l2-1v-3.175l2-1.119v5.705l-7 3.89z' fill='currentColor'/></svg> <p class='m-0'>Your waning message</p></div>
                              </b:if>
                              

                              <div class='bc-fff r2 mb-15 s1 post oh'>
                                <h2 class='c-theme m-0 bb-1pxsf y9x19p fs-15 flex aic'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><path d='M3 6h8v13H3z' fill='currentColor' opacity='.3'/><path d='M21 4H3c-1.1 0-2 .9-2 2v13c0 1.1.9 2 2 2h18c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zM11 19H3V6h8v13zm10 0h-8V6h8v13zm-7-9.5h6V11h-6zm0 2.5h6v1.5h-6zm0 2.5h6V16h-6z' fill='currentColor'/></svg>Read <data:post.title/></h2>
                                <div class='bc-fff s1 r2 p-13'>
                                  <b:class cond='data:view.isPage' name='page-view'/>
                                  <data:post.body/>
                                </div>
                              </div>
                            </b:includable>
                            <b:includable id='postBodySnippet' var='post'>
                              <b:include data='post' name='postBody'/>
                            </b:includable>
                            <b:includable id='postChapter' var='post'>
                              <style>main,body {background-color: #16151d}</style>
                              <script>histories.addHistory(&quot;<data:post.id/>&quot;,&quot;<data:post.title/>&quot;,&quot;<data:post.url/>&quot;);</script>
                              <div class='max-w mla mra pen c-999 mt-35 full oh'>
                                <!-- <b:include data='post' name='inlineAd2'/> -->
                            <h1 class='m-0 fs-25 tac c-ddd fs-20'>
                                    <b:with value='[&quot;Chapter&quot;,&quot;Project&quot;]' var='chf'>
                                      <b:loop index='i' values='data:post.labels' var='label'>
                                        <b:if cond='data:label.name not in data:chf'>
                                          <a class='c-ddd' expr:data='data:label.name' expr:href='data:label.url' rel='tag'>
                                            <data:label.name/>
                                            <script>document.title = &quot;<data:label.name/> - <data:post.title/>&quot;;</script>
                                          </a>
                                        </b:if>
                                      </b:loop>
                                    </b:with>
                             - <data:post.title/>
                                  </h1>
                                <div class='tac'>All chapters are in <b:with value='[&quot;Chapter&quot;,&quot;Project&quot;]' var='chf'>
                                      <b:loop index='i' values='data:post.labels' var='label'>
                                        <b:if cond='data:label.name not in data:chf'>
                                          <a class='c-theme fw-600' expr:data='data:label.name' expr:href='data:label.url' rel='tag'>
                                            <data:label.name/>
                                            
                                          </a>
                                        </b:if>
                                      </b:loop>
                                    </b:with></div>
                                <b:include cond='data:post.shareUrl' name='postShareButtons'/>
                                <div class='oh tac r2 mb-20 fs-13 p-y10x15 bg-222'>
                                  <ol class='lsn m-0 pl-0 m-y0x4-li' itemscope='itemscope' itemtype='http://schema.org/BreadcrumbList'>
                                    <li class='i-block' itemprop='itemListElement' itemscope='itemscope' itemtype='http://schema.org/ListItem'>
                                      <a class='c-999' expr:href='data:blog.homepageUrl' itemprop='item'><span itemprop='name'><data:blog.title/></span></a>
                                      <meta content='1' itemprop='position'/>
                                    </li>
                                    &#8250;
                                    <li class='i-block' itemprop='itemListElement' itemscope='itemscope' itemtype='http://schema.org/ListItem'>
                                      <b:with value='[&quot;Chapter&quot;,&quot;Project&quot;]' var='chf'>
                                        <b:loop index='i' values='data:post.labels' var='label'>
                                          <b:if cond='data:label.name not in data:chf'>
                                            <a class='c-999' expr:data='data:label.name' expr:href='data:label.url' itemprop='item'><span itemprop='name'>
                                              <data:label.name/>
                                              </span>
                                            </a>
                                          </b:if>
                                        </b:loop>
                                      </b:with>
                                      <meta content='2' itemprop='position'/>
                                    </li>
                                    &#8250;
                                    <li class='i-block' itemprop='itemListElement' itemscope='itemscope' itemtype='http://schema.org/ListItem'>
                                      <a class='c-999' expr:href='data:post.url' itemprop='item'><span itemprop='name'><data:post.title/></span></a>
                                      <meta content='3' itemprop='position'/>
                                    </li>
                                  </ol>
                                </div>
                                <b:with value='[&quot;Chapter&quot;,&quot;Project&quot;]' var='chf'>
                                  <p class='tac fs-14'>
                                    Baca manga <b>
                                    <b:loop index='i' values='data:post.labels' var='label'>
                                      <b:if cond='data:label.name not in data:chf'>
                                        <data:label.name/>
                                      </b:if>
                                    </b:loop>
                                    <data:post.title/></b> bahasa Indonesia terbaru di <b><data:blog.title/></b>. Manga <b>
                                    <b:loop index='i' values='data:post.labels' var='label'>
                                      <b:if cond='data:label.name not in data:chf'>
                                        <data:label.name/>
                                      </b:if>
                                    </b:loop>
                                    </b> bahasa Indonesia selalu update di <b><data:blog.title/></b>. Jangan lupa membaca update manga lainnya ya. Daftar koleksi manga <b><data:blog.title/></b> ada di menu Daftar Manga. </p></b:with>
                                
<h4 class='tac mla mra bg-main' style='color:white;padding:6px;border-radius:5px;max-width: 950px;'>Lapor Gambar Rusak / Tidak Sesuai / Tidak Terload Lapor [<a href='https://kilatkomik.chatango.com/' target='_blank'><span style='color: blue;'><strong>DISINI</strong></span></a>]</h4>
                                
                                <b:include name='chapNextPrev'/>
                                <div class='check-box'>
                                  <data:post.body/>
                                </div>
								<b:include name='chapNextPrev-bottom'/>
                                <!-- <b:include data='post' name='inlineAd2'/> -->
                                <div class='dark-mode'>
                                  <b:include name='chapterTags'/>
                                  <div class='mb-15'><b:include name='relatedPost'/></div>
                                  <b:include data='post' name='commentPicker'/>
                                </div>
                              </div>
                            </b:includable>
                            <b:includable id='postCommentsAndAd' var='post'>
                              <b:tag class='link:hover' cond='data:view.isMultipleItems' expr:title='data:post.title' name='section'>

                                

                                  <!-- Feed view -->
                                  <b:include cond='data:view.isHomepage' name='feedHome'/>


                                  <!-- Post title and body -->
                                  <b:include cond='data:view.isPost' data='post' name='post'/>
                                  
                                  <b:include cond='data:view.isPage' name='page'/>

                                  <!-- Show ad inside post container, after comments, if single item. -->
                                  <b:include cond='data:view.isSingleItem and data:post.includeAd' data='post' name='inlineAd'/>
                                </b:tag>

                            </b:includable>
                            <b:includable id='postCommentsLink'>
                              <b:if cond='data:view.isMultipleItems'>
                                <span class='byline post-comment-link container'>
                                  <b:include cond='data:post.commentSource != 1' name='commentsLink'/>
                                </span>
                              </b:if>
                            </b:includable>
                            <b:includable id='postFooter' var='post'>
                              <div class='post-footer'>
                                <b:include cond='data:post.shareUrl' name='postShareButtons'/>
                                <b:include data='post' name='postFooterAuthorProfile'/>
                              </div>
                            </b:includable>
                            <b:includable id='postFooterAuthorProfile' var='post'>
                              <b:if cond='data:post.author.aboutMe and data:view.isPost'>
                                <div class='author-profile'>
                                  <b:if cond='data:post.author.authorPhoto.url'>
                                    <img class='author-image' expr:src='data:post.author.authorPhoto.url' width='50px'/>
                                    <div class='author-about'>
                                      <b:include data='post' name='aboutPostAuthor'/>
                                    </div>
                                    <b:else/>
                                    <b:include data='post' name='aboutPostAuthor'/>
                                  </b:if>
                                </div>
                              </b:if>
                            </b:includable>
                            <b:includable id='postHeader' var='post'>
                              <b:include name='headerByline'/>
                            </b:includable>
                            <b:includable id='postJumpLink' var='post'>
                              <div class='jump-link flat-button'>
                                <a expr:href='data:post.url fragment &quot;more&quot;' expr:title='data:post.title'>
                                  <b:eval expr='data:blog.jumpLinkMessage'/>
                                </a>
                              </div>
                            </b:includable>
                            <b:includable id='postLabelNovel'>
                              <b:loop index='i' values='data:post.labels' var='label'>
                                <a class='i-block bg-main r4 c-fff fs-14 y5x10p dim:hover white:hover' expr:href='data:label.url + &quot;?&amp;max-results=20&quot;' rel='tag'>
                                  <svg class='feather feather-tag' fill='none' height='24' stroke='currentColor' stroke-linecap='round' stroke-linejoin='round' stroke-width='2' viewBox='0 0 24 24' width='24' xmlns='http://www.w3.org/2000/svg'><path d='M20.59 13.41l-7.17 7.17a2 2 0 0 1-2.83 0L2 12V2h10l8.59 8.59a2 2 0 0 1 0 2.82z'/><line x1='7' x2='7.01' y1='7' y2='7'/></svg>
                                  <data:label.name/>
                                </a>
                              </b:loop>
                            </b:includable>
                            <b:includable id='postLabels'>
                              <b:loop index='i' values='data:post.labels' var='label'>
                                <b:if cond='data:label.name in data:Genre or data:label.name in data:Genre2 or data:label.name in data:Demographic'>
                                  <a class='label mr-7 mb-6 fs-13 r4 i-block' expr:href='data:label.url + &quot;?&amp;max-results=20&quot;' rel='tag'>
                                    <data:label.name/>
                                  </a>
                                </b:if>
                              </b:loop>
                            </b:includable>
                            <b:includable id='postLocation'>
                              <span class='byline post-location'>
                                <data:byline.label/>
                                <a expr:href='data:post.location.mapsUrl' target='_blank'><data:post.location.name/></a>
                              </span>
                            </b:includable>
                            <b:includable id='postMeta' var='post'>
                              <b:include data='post' name='postMetadataJSON'/>
                            </b:includable>
                            <b:includable id='postMetadataJSONImage'>
                              <script type='application/ld+json'>{
                              &quot;image&quot;: {
                              &quot;@type&quot;: &quot;ImageObject&quot;,
                              <b:if cond='data:post.featuredImage.isResizable'>
                                &quot;url&quot;: &quot;<b:eval expr='resizeImage(data:post.featuredImage, 1200, &quot;1200:630&quot;)'/>&quot;,
                                &quot;height&quot;: 630,
                                &quot;width&quot;: 1200
                                <b:else/>
                                &quot;url&quot;: &quot;https://lh3.googleusercontent.com/ULB6iBuCeTVvSjjjU1A-O8e9ZpVba6uvyhtiWRti_rBAs9yMYOFBujxriJRZ-A=w1200&quot;,
                                &quot;height&quot;: 348,
                                &quot;width&quot;: 1200
                              </b:if>
                              },
                              }</script>
                            </b:includable>
                            <b:includable id='postMetadataJSONPublisher'>
                              <script type='application/ld+json'>{
                              &quot;publisher&quot;: {
                              &quot;@type&quot;: &quot;Organization&quot;,
                              &quot;name&quot;: &quot;<data:blog.title/>&quot;,
                              &quot;logo&quot;: {
                              &quot;@type&quot;: &quot;ImageObject&quot;,
                              &quot;url&quot;: &quot;https://lh3.googleusercontent.com/ULB6iBuCeTVvSjjjU1A-O8e9ZpVba6uvyhtiWRti_rBAs9yMYOFBujxriJRZ-A=h60&quot;,
                              &quot;width&quot;: 206,
                              &quot;height&quot;: 60
                              }
                              </script>
                            </b:includable>
                            <b:includable id='postNovel' var='post'>
                              <style>#comments,.a4 {
  grid-area: unset;
  max-width: 1080px;
  margin: 0 auto;
  width: 100%;
}</style>
                              <article class='s1 p-20 bc-fff r2 max-w mla mra mt-24'>
                                <header class='bb-2pxsec mb-15 pb-15'>
                                  <b:include name='postLabelNovel'/>
                                  <h1><data:post.title/></h1>
                                  <div class='flex aic c-666 fs-14'>
                                    <address class='mr-13 flex aic' rel='author'>
                                      <b:include data='{image: data:post.author.authorPhoto.image,imageRatio: &quot;1:1&quot;, imageSizes: [84, 168],sourceSizes: &quot;23px&quot;,imageClass: &quot;r50p mr-7&quot;}' name='responsiveImage'/>
                                      <span><data:post.author.name/></span>
                                    </address>
                                    <time><data:post.date/></time>
                                  </div>
                                </header>
                                <div class='lh-1d7 link post c-ee'>
                                  <data:post.body/>
                                </div>
                              </article>
                              <b:include cond='data:view.isSingleItem' data='post' name='commentPicker'/>
                            </b:includable>
                            <b:includable id='postPagination'>
                              <div class='blog-pager container' id='blog-pager'>
                                <b:include cond='data:newerPageUrl' name='previousPageLink'/>
                                <b:include cond='data:olderPageUrl' name='nextPageLink'/>
                                <b:include cond='data:view.url != data:blog.homepageUrl' name='homePageLink'/>
                              </div>
                            </b:includable>
                            <b:includable id='postReactions'>
                              <span class='byline reactions'>
                                <span class='reactions-label'>
                                  <data:byline.label/>
                                </span>
                                <iframe allowtransparency='true' class='reactions-iframe' expr:src='data:post.reactionsUrl' frameborder='0' name='reactions' scrolling='no'/>
                              </span>
                            </b:includable>
                            <b:includable id='postShareButtons'>
                              <div class='grid jcc yt8m'>
                                <div class='post-share flex aic' expr:data-share='data:messages.share'>
                                  <!-- Bagikan ke Facebook -->
                                  <div class='share-icon r4 facebookThis'>
                                    <a aria-label='Share button' class='flex aic c-fff white:hover' expr:href='&quot;https://www.facebook.com/sharer.php?u=&quot; + data:blog.url.canonical' rel='nofollow noreferrer' role='button' target='_blank'>
                                      <svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><path d='M14 13.5h2.5l1-4H14v-2c0-1.03 0-2 2-2h1.5V2.14c-.326-.043-1.557-.14-2.857-.14C11.928 2 10 3.657 10 6.7v2.8H7v4h3V22h4v-8.5z' fill='currentColor'/></svg>
                                      <span>Facebook</span>
                                    </a>
                                  </div>
                                  <!-- Bagikan ke Twitter -->
                                  <div class='share-icon r4 twitterThis'>
                                    <a aria-label='Share button' class='flex aic c-fff white:hover' expr:href='&quot;https://twitter.com/share?url=&quot; + data:blog.url.canonical' rel='nofollow noreferrer' role='button' target='_blank'>
                                      <svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><g fill='none'><path d='M23.643 4.937c-.835.37-1.732.62-2.675.733a4.67 4.67 0 0 0 2.048-2.578a9.3 9.3 0 0 1-2.958 1.13a4.66 4.66 0 0 0-7.938 4.25a13.229 13.229 0 0 1-9.602-4.868c-.4.69-.63 1.49-.63 2.342A4.66 4.66 0 0 0 3.96 9.824a4.647 4.647 0 0 1-2.11-.583v.06a4.66 4.66 0 0 0 3.737 4.568a4.692 4.692 0 0 1-2.104.08a4.661 4.661 0 0 0 4.352 3.234a9.348 9.348 0 0 1-5.786 1.995a9.5 9.5 0 0 1-1.112-.065a13.175 13.175 0 0 0 7.14 2.093c8.57 0 13.255-7.098 13.255-13.254c0-.2-.005-.402-.014-.602a9.47 9.47 0 0 0 2.323-2.41l.002-.003z' fill='currentColor'/></g></svg>
                                      <span>Twitter</span>
                                    </a>
                                  </div>
                                  <!-- Bagikan ke Whatsapp -->
                                  <div class='share-icon r4 whatsappThis'>
                                    <a aria-label='Share button' class='flex aic c-fff white:hover' expr:href='&quot;https://api.whatsapp.com/send?text=&quot; + data:blog.url.canonical' rel='nofollow noreferrer' role='button' target='_blank'>
                                      <svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 32 32' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><path d='M23.328 19.177c-.401-.203-2.354-1.156-2.719-1.292c-.365-.13-.63-.198-.896.203c-.26.391-1.026 1.286-1.26 1.547s-.464.281-.859.104c-.401-.203-1.682-.62-3.203-1.984c-1.188-1.057-1.979-2.359-2.214-2.76c-.234-.396-.026-.62.172-.818c.182-.182.401-.458.604-.698c.193-.24.255-.401.396-.661c.13-.281.063-.5-.036-.698s-.896-2.161-1.229-2.943c-.318-.776-.651-.677-.896-.677c-.229-.021-.495-.021-.76-.021s-.698.099-1.063.479c-.365.401-1.396 1.359-1.396 3.297c0 1.943 1.427 3.823 1.625 4.104c.203.26 2.807 4.26 6.802 5.979c.953.401 1.693.641 2.271.839c.953.302 1.823.26 2.51.161c.76-.125 2.354-.964 2.688-1.901c.339-.943.339-1.724.24-1.901c-.099-.182-.359-.281-.76-.458zM16.083 29h-.021c-2.365 0-4.703-.641-6.745-1.839l-.479-.286l-5 1.302l1.344-4.865l-.323-.5a13.166 13.166 0 0 1-2.021-7.01c0-7.26 5.943-13.182 13.255-13.182c3.542 0 6.865 1.38 9.365 3.88a13.058 13.058 0 0 1 3.88 9.323C29.328 23.078 23.39 29 16.088 29zM27.359 4.599C24.317 1.661 20.317 0 16.062 0C7.286 0 .14 7.115.135 15.859c0 2.792.729 5.516 2.125 7.927L0 32l8.448-2.203a16.13 16.13 0 0 0 7.615 1.932h.005c8.781 0 15.927-7.115 15.932-15.865c0-4.234-1.651-8.219-4.661-11.214z' fill='currentColor'/></svg>
                                      <span>Whatsapp</span>
                                    </a>
                                  </div>
		
<!-- Bagikan ke Pinterest -->
                                  <div class='share-icon r4 pinterestThis'>
                                    <a aria-label='Share button' class='flex aic c-fff white:hover' expr:href='&quot;//pinterest.com/pin/create/button/?url=&quot; + data:post.title + &quot;%20%2D%20&quot; + data:post.url' rel='nofollow noreferrer' role='button' target='_blank'>
                                      <svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><path d='M11.99 2C6.472 2 2 6.473 2 11.99c0 4.232 2.633 7.85 6.35 9.306c-.088-.79-.166-2.006.034-2.868c.182-.78 1.172-4.966 1.172-4.966s-.299-.599-.299-1.484c0-1.388.805-2.425 1.808-2.425c.853 0 1.264.64 1.264 1.407c0 .858-.546 2.139-.827 3.327c-.235.994.499 1.805 1.479 1.805c1.775 0 3.141-1.872 3.141-4.575c0-2.392-1.719-4.064-4.173-4.064c-2.843 0-4.512 2.132-4.512 4.335c0 .858.331 1.779.744 2.28a.3.3 0 0 1 .069.286c-.076.315-.245.994-.277 1.133c-.044.183-.145.222-.335.134c-1.247-.581-2.027-2.405-2.027-3.871c0-3.151 2.289-6.045 6.601-6.045c3.466 0 6.159 2.469 6.159 5.77c0 3.444-2.171 6.213-5.184 6.213c-1.013 0-1.964-.525-2.29-1.146l-.623 2.374c-.225.868-.834 1.956-1.241 2.62a10 10 0 0 0 2.958.445c5.517 0 9.99-4.473 9.99-9.99S17.507 2 11.99 2' fill='currentColor'/></svg>
                                      <span>Pinterest</span>
                                    </a>
                                  </div>
                                </div>
                              </div>
                            </b:includable>
                            <b:includable id='postTimestamp'>
                              <span class='byline post-timestamp'>
                                <data:byline.label/>
                                <b:if cond='data:post.url'>
                                  <meta expr:content='data:post.url.canonical'/>
                                  <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'>
                                    <time class='published' expr:datetime='data:post.date.iso8601' expr:title='data:post.date.iso8601'>
                                      <data:post.date/>
                                    </time>
                                  </a>
                                </b:if>
                              </span>
                            </b:includable>
                            <b:includable id='postTitle' var='post'>
                              <b:if cond='data:post.title != &quot;&quot;'>
                                <b:tag class='mt-0 mb-6 fs-20' cond='data:view.isSingleItem' name='h1'>
                                  <b:tag class='mt-0 c-fff fs-20' cond='data:view.isLabelSearch' name='h1'>
                                    <b:tag class='m-0 c-22 fs-14 y6x0p s3f5 wsn oh toe' cond='data:view.isHomepage' name='h3'>
                                      <b:if cond='data:post.link or (data:post.url and data:view.url != data:post.url)'>
                                        <a class='ck' expr:href='data:post.link ?: data:post.url'><data:post.title/></a>
                                        <b:else/>
                                        <data:post.title/>
                                      </b:if>
                                    </b:tag>
                                  </b:tag>
                                </b:tag>
                              </b:if>
                            </b:includable>
                            <b:includable id='previousPageLink'>
                              <a class='blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' expr:title='data:messages.newerPosts'>
                                <data:messages.newerPosts/>
                              </a>
                            </b:includable>
                            <b:includable id='score'>
                              <b:if cond='data:post.labels any (l =&gt; l.name == &quot;Score 0.5&quot;)'>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='0-5'/>
                                  </div>
                                  <div>0.5</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 1.0&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='0-5'/>
                                  </div>
                                  <div>1.0</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 1.5&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='1-0'/>
                                  </div>
                                  <div>1.5</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 2.0&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='1-0'/>
                                  </div>
                                  <div>2.0</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 2.5&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='1-0'/>
                                  </div>
                                  <div>2.5</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 3.0&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='1-5'/>
                                  </div>
                                  <div>3.0</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 3.5&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='1-5'/>
                                  </div>
                                  <div>3.5</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 4.0&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='2-0'/>
                                  </div>
                                  <div>4.0</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 4.5&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='2-0'/>
                                  </div>
                                  <div>4.5</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 5.0&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='2-5'/>
                                  </div>
                                  <div>5.0</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 5.5&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='2-5'/>
                                  </div>
                                  <div>5.5</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 6.0&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='2-5'/>
                                  </div>
                                  <div>6.0</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 6.5&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='3-0'/>
                                  </div>
                                  <div>6.5</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 7.0&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='3-0'/>
                                  </div>
                                  <div>7.0</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 7.5&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='3-5'/>
                                  </div>
                                  <div>7.5</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 8.0&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='3-5'/>
                                  </div>
                                  <div>8.0</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 8.5&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='4-0'/>
                                  </div>
                                  <div>8.5</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 9.0&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='4-5'/>
                                  </div>
                                  <div>9.0</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 9.5&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='5-0'/>
                                  </div>
                                  <div>9.5</div>
                                </aside>
                                <b:elseif cond='data:post.labels any (l =&gt; l.name == &quot;Score 10.0&quot;)'/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='5-0'/>
                                  </div>
                                  <div>10.0</div>
                                </aside>
                                <b:else/>
                                <aside class='p-10 bc-f5 grid pic oh'>
                                  <div>
                                    <b:include name='0-0'/>
                                  </div>
                                  <div>0.0</div>
                                </aside>
                              </b:if>
                            </b:includable>
                            <b:includable id='select_chapter'>
                              <b:loop values='data:post.labels' var='label'>
                                <b:if cond='data:label.name not in data:Status and data:label.name not in data:Score and data:label.name not in data:Other and data:label.name not in data:Other and data:label.name not in data:Genre and data:label.name not in data:Genre2 and data:label.name not in data:Alphabet and data:label.name not in data:Format and data:label.name not in data:Demographic and data:label.name not in data:Content'>
                                  <script>
                                    var postID = <data:post.id/>;
                                    //<![CDATA[
if(autlist==true){function autolist(e){for(var t=0;t<e.feed.entry.length;t++){for(var r=0;r<e.feed.entry[t].link.length;r++)if("alternate"==e.feed.entry[t].link[r].rel){var n=e.feed.entry[t].link[r].href;break}var f=e.feed.entry[t].title.$t;e.feed.entry[t].id.$t.substr(51,19)!=postID&&document.write("<div class='index-list'><a href="+n+">"+f+"</a></div>")}}}
//]]>
                                  </script>
                                  <div class='auto-listchap'><script expr:src='&quot;/feeds/posts/default/-/&quot; + data:label.name + &quot;?orderby=published&amp;max-results=500&amp;alt=json-in-script&amp;callback=autolist&quot;' type='text/javascript'/></div></b:if></b:loop>
                            </b:includable>
                            <b:includable id='sharingButton'>
                              <span expr:aria-label='data:platform.shareMessage' expr:class='&quot;sharing-platform-button sharing-element-&quot; + data:platform.key' expr:data-href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:data-url='data:originalUrl' expr:title='data:platform.shareMessage' role='menuitem' tabindex='-1'>
                                <b:include name='sharingPlatformIcon'/>
                                <span class='platform-sharing-text'><data:platform.name/></span>
                              </span>
                            </b:includable>
                            <b:includable id='sharingButtonContent'>
                              <div class='flat-icon-button ripple'>
                                <b:include name='shareIcon'/>
                              </div>
                            </b:includable>
                            <b:includable id='sharingButtons'>
                              <div class='sharing' expr:aria-owns='&quot;sharing-popup-&quot; + data:sharingId' expr:data-title='data:shareTitle'>
                                <button class='sharing-button touch-icon-button' expr:aria-controls='&quot;sharing-popup-&quot; + data:sharingId' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-button-&quot; + data:sharingId' role='button'>
                                  <b:include name='sharingButtonContent'/>
                                </button>
                                <b:include name='sharingButtonsMenu'/>
                              </div>
                            </b:includable>
                            <b:includable id='sharingButtonsMenu'>
                              <div class='share-buttons-container'>
                                <ul aria-hidden='true' class='share-buttons hidden' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-popup-&quot; + data:sharingId' role='menu'>
                                  <b:loop values='(data:platforms ?: data:blog.sharing.platforms) filter (p =&gt; p.key not in {&quot;blogThis&quot;})' var='platform'>
                                    <li>
                                      <b:include name='sharingButton'/>
                                    </li>
                                  </b:loop>
                                  <li aria-hidden='true' class='hidden'>
                                    <b:include name='otherSharingButton'/>
                                  </li>
                                </ul>
                              </div>
                            </b:includable>
                            <b:includable id='sharingPlatformIcon'>
                              <b:include data='{ iconClass: (&quot;touch-icon sharing-&quot; + data:platform.key) }' expr:name='data:platform.key + &quot;Icon&quot;'/>
                            </b:includable>
                            <b:includable id='threadedCommentForm' var='post'>
                              <div class='comment-form'>
                                <a name='comment-form'/>
                                <h4 id='comment-post-message'><data:messages.postAComment/></h4>
                                <b:if cond='data:this.messages.blogComment != &quot;&quot;'>
                                  <p class='alr royal p-15 ml-20 mr-20'><data:this.messages.blogComment/></p>
                                </b:if>
                                <b:include data='post' name='commentFormIframeSrc'/>
                                <iframe allowtransparency='allowtransparency' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight ?: &quot;90px&quot;' frameborder='0' id='comment-editor' name='comment-editor' src='' width='100%'/>
                                <data:post.cmtfpIframe/>
                                <script type='text/javascript'>
                                  BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;);
                                </script>
                              </div>
                            </b:includable>
                            <b:includable id='threadedCommentJs' var='cb'>
  <div class='avatar-image-container grid'>
		<div class='tar'>
			<b:if cond='data:cb.level.authorAvatarSrc != &quot;//resources.blogblog.com/img/blank.gif&quot;'>
				<img class='lazy' expr:alt='data:cb.level.author' expr:src='resizeImage(data:cb.level.authorAvatarSrc, 100, &quot;1:1&quot;)' expr:title='data:cb.level.author'/>
			</b:if>
		</div>
    <div class='fs-12 jsc mt-5'><span class='power'>+<b:eval expr='data:cb.level.body.size'/></span></div>
	</div>
	<div class='comment-block' itemscope='itemscope' itemtype='https://schema.org/Comment'>
		<div class='comment-header'>
			<b:if cond='data:cb.level.author != &quot;Anonymous&quot;'> <span class='user' itemprop='author' itemscope='itemscope' itemtype='https://schema.org/Person'>
                          <span itemprop='name'><data:cb.level.author/></span> 
				<b:if cond='data:post.author.name == data:cb.level.author'>
					<svg class='blog-author' viewBox='0 0 24 24'>
						<path d='M12,2A10,10 0 0,1 22,12A10,10 0 0,1 12,22A10,10 0 0,1 2,12A10,10 0 0,1 12,2M11,16.5L18,9.5L16.59,8.09L11,13.67L7.91,10.59L6.5,12L11,16.5Z'/>
					</svg>
				</b:if>
				</span>
			</b:if> <time class='datetime secondary-text' expr:datetime='data:cb.level.timestamp' expr:title='data:cb.level.timestamp' itemprop='datePublished'>
                        <a expr:href='&quot;#c&quot; + data:cb.level.id' itemprop='url'>
                          <data:cb.level.timestamp/>
                        </a>
                      </time>
		</div>
		<div class='comment-content' itemprop='text'>
			<!--<b:if cond='data:cb.level.authorUrl != data:post.author.profileUrl'>--><b:eval expr='data:cb.level.body snippet { links: false }'/>
			<!--<b:else/>
                         <data:cb.level.body/>
                       </b:if>-->
		</div>
	</div>
	<b:if cond='data:cb.d and data:commentL2.size != &quot;2&quot;'>
                    <div class='comment-actions secondary-text'>
                      <a class='comment-reply reply-to' expr:data-comment-id='data:commentLevel1.id' expr:data-reply-to='data:commentLevel1.id' href='javascript:;' target='_self'>Balas</a>
                      <span expr:class='&quot;item-control &quot; + data:cb.level.adminClass'>
                        <a expr:href='data:cb.level.deleteUrl' expr:title='data:messages.deleteComment' rel='noopener external nofollow' target='_self'>Hapus</a>
                      </span>
                    </div>
                  </b:if>
</b:includable>
                            <b:includable id='threadedComments' var='post'>
                  <section class='comments threaded' expr:data-embed='data:post.embedCommentForm' expr:data-num-comments='data:post.numberOfComments' id='comments'>
                    <input class='cmAl hidden' id='forAllCm' type='checkbox'/>
                    <b:include name='commentsTitle'/>                   
                    <b:if cond='data:post.numberOfComments &gt; 0'>
                      <div class='comments-content'>                        
                        <ol id='comment-holder'>
                          <b:loop values='data:post.comments where (c =&gt; not c.inReplyTo or c.inReplyTo == 0)' var='commentLevel1'>
                            <li class='comment' expr:id='&quot;c&quot; + data:commentLevel1.id'>
                              <b:class cond='data:post.adminClass' name='author-comment'/>
                              <b:class cond='not data:post.adminClass' name='user-comment'/>
                              <b:include data='{level: data:commentLevel1,d: true}' name='commentblock'/>
                              <!--<div class='comment-actions'>
                                <span class='reply-to' expr:data-reply-to='data:commentLevel1.id'>Balas</span>
                              </div>-->
                              <b:with value='data:post.comments where (c =&gt; c.inReplyTo == data:commentLevel1.id)' var='commentL2'>
                                <b:if cond='data:commentL2.size != &quot;0&quot;'>
                                  <div class='comment-replies'>
                                    <input class='thread-show hidden' expr:id='&quot;off-&quot; + data:commentLevel1.id' type='checkbox'/>
                                    <div class='comment-thread inline-thread' expr:id='&quot;c&quot; + data:commentLevel1.id + &quot;-rt&quot;'>
                                      <label class='thread-toggle thread-expanded' expr:for='&quot;off-&quot; + data:commentLevel1.id'>
                                        <svg class='thread-arrow line' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'><polyline points='6 9 12 15 18 9'/></svg>
                                        <span class='thread-count'>Balasan</span>
                                      </label>
                                    
                                      <ul class='thread-chrome thread-expanded'>
                                        <b:loop values='data:commentL2' var='commentLevel2'>
                                          <li class='comment' expr:id='&quot;c&quot; + data:commentLevel2.id'>
                                            <b:class cond='data:post.adminClass' name='author-comment'/>
                                            <b:class cond='not data:post.adminClass' name='user-comment'/>
                                            <b:include data='{level: data:commentLevel2,d: true}' name='commentblock'/>
                                          </li>
                                        </b:loop>
                                      </ul>
                                      
                                    </div>
                                    <b:if cond='data:post.allowNewComments'>
                                      <div class='comment-reply'>
                                        <a class='reply-to' expr:data-reply-to='data:commentLevel1.id' href='javascript:;' target='_self'><svg class='line' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'><polyline points='15 14 20 9 15 4'/><path d='M4 20v-7a4 4 0 0 1 4-4h12'/></svg>Balas</a>
                                      </div>
                                    </b:if>
                                  </div>
                                </b:if>
                              </b:with>
                              
                              <b:if cond='data:commentL2.size != &quot;2&quot; and data:post.allowNewComments'>
                                <div class='comment-actions secondary-text'>
                                  <a class='comment-reply reply-to' expr:data-comment-id='data:commentLevel1.id' expr:data-reply-to='data:commentLevel1.id' href='javascript:;' target='_self'><svg class='line' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'><polyline points='15 14 20 9 15 4'/><path d='M4 20v-7a4 4 0 0 1 4-4h12'/></svg>Balas</a>
                                </div>
                              </b:if>
                            </li>
                          </b:loop>
                        </ol>
                      </div>
                      
                      <b:if cond='data:post.allowNewComments'>
                        <div class='comment-add'>
                          <script>var comment = true;</script>
                          <div aria-label='Berkomentar' class='hidden' id='addcomment' role='button'><data:messages.postAComment/></div>
                        </div>
                      </b:if>
                      <b:else/>
                      <script>var comment = false;</script>
                    </b:if>
                    
                    <div class='comment-form'>
                      <b:if cond='data:post.allowNewComments'>
                        <div id='threaded-comment-form'>
                          <b:if cond='data:this.messages.blogComment != &quot;&quot;'>
                            <div class='alr grid aic p-15'>
                              <svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg'><path d='m16 7.58l-5.5-2.4L5 7.58v3.6c0 3.5 2.33 6.74 5.5 7.74c.25-.08.49-.2.73-.3c-.15-.51-.23-1.06-.23-1.62c0-2.97 2.16-5.43 5-5.91V7.58z' fill='currentColor' opacity='.3'/><path d='M17 13c-2.21 0-4 1.79-4 4s1.79 4 4 4s4-1.79 4-4s-1.79-4-4-4zm0 1.38c.62 0 1.12.51 1.12 1.12s-.51 1.12-1.12 1.12s-1.12-.51-1.12-1.12s.5-1.12 1.12-1.12zm0 5.37c-.93 0-1.74-.46-2.24-1.17c.05-.72 1.51-1.08 2.24-1.08s2.19.36 2.24 1.08c-.5.71-1.31 1.17-2.24 1.17z' fill='currentColor' opacity='.3'/><circle cx='17' cy='15.5' fill='currentColor' r='1.12'/><path d='M18 11.09V6.27L10.5 3L3 6.27v4.91c0 4.54 3.2 8.79 7.5 9.82c.55-.13 1.08-.32 1.6-.55A5.973 5.973 0 0 0 17 23c3.31 0 6-2.69 6-6c0-2.97-2.16-5.43-5-5.91zM11 17c0 .56.08 1.11.23 1.62c-.24.11-.48.22-.73.3c-3.17-1-5.5-4.24-5.5-7.74v-3.6l5.5-2.4l5.5 2.4v3.51c-2.84.48-5 2.94-5 5.91zm6 4c-2.21 0-4-1.79-4-4s1.79-4 4-4s4 1.79 4 4s-1.79 4-4 4z' fill='currentColor'/><path d='M17 17.5c-.73 0-2.19.36-2.24 1.08c.5.71 1.32 1.17 2.24 1.17s1.74-.46 2.24-1.17c-.05-.72-1.51-1.08-2.24-1.08z' fill='currentColor'/></svg>
                            <p><data:this.messages.blogComment/></p>
                            </div>
                          </b:if>
                          <b:include data='post' name='commentFormIframeSrc'/>
            <iframe allowtransparency='allowtransparency' class='blogger-iframe-colorize blogger-comment-from-post' data-resized='true' expr:data-src='data:post.commentFormIframeSrc appendParams {skin: &quot;contempo&quot;}' expr:height='data:cmtIframeInitialHeight ?: &quot;90px&quot;' expr:src='data:post.commentFormIframeSrc appendParams {skin: &quot;contempo&quot;}' frameborder='0' id='comment-editor' name='comment-editor' width='100%'/>
            <data:post.cmtfpIframe/>
            <script type='text/javascript'>
              BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;);
            </script>
                        </div>
                        <b:else/>
                        <div class='comment-disable'>
                          <data:post.noNewCommentsText/>
                        </div>
                      </b:if>
                    </div>
                    
                    <b:if cond='data:showCmtPopup'>
                      <div id='comment-popup'>
                        <iframe allowtransparency='allowtransparency' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'/>
                      </div>
                    </b:if>
                  </section>
                  
                  <b:if cond='data:post.allowNewComments'>
                    <script>/*<![CDATA[*/ document.addEventListener("DOMContentLoaded", function() { var a=document, b = a.getElementById("comment-editor"), d = b.getAttribute("data-src"); if (b.setAttribute("src", d), 1 == comment) { var f = a.getElementsByClassName("reply-to"), c = a.getElementById("threaded-comment-form"), h = f.length, k = function(b, d, e, f) { b.addEventListener("click", function() { var c = b.getAttribute("data-reply-to"); a.getElementById("c" + c).appendChild(d); a.getElementById("threaded-comment-form").className = 'comment-replybox-single'; a.getElementById("addcomment").className = 'comment-reply button outline'; e.src = f + "&parentID=" + c }) }; for (i = 0; i < h; i++) k(f[i], c, b, d); var l = a.getElementsByClassName("comment-form")[0]; a.getElementById("addcomment").addEventListener("click", function() { l.appendChild(c); a.getElementById("threaded-comment-form").className = 'comment-replybox-thread'; a.getElementById("addcomment").className = 'comment-reply hidden'; b.src = d }) } }); /*]]>*/</script>
                    </b:if>
                    </b:includable>
                            <b:includable id='viewAll'>
                              <article class='r2 s1 bc-fff'>
                                <div class='flex aic jcsb bb-1pxsf y9x19p yb10m'>
                                  <h3 class='m-0 c-theme'><b:if cond='data:view.isHomepage'><data:messages.latestPosts/></b:if>
                                    <b:if cond='data:view.search.query'><data:messages.search/>: <b><data:view.search.query/></b></b:if>
                                    <b:if cond='data:view.search.label'>Rekomendasi Komik <b><data:blog.pageName/></b> Terbaik</b:if>
                                    <b:if cond='data:view.isArchive'>Arsip Komik Tanggal: <b><data:blog.pageName/></b></b:if>
                                    <b:if cond='data:view.search and !data:view.search.label and !data:view.search.query and !data:view.isArchive'><data:messages.posts/></b:if></h3>
                                  <svg class='feather feather-filter' fill='none' height='24' id='toggle' stroke='var(--primary-color)' stroke-linecap='round' stroke-linejoin='round' stroke-width='2' viewBox='0 0 24 24' width='24' xmlns='http://www.w3.org/2000/svg'><polygon points='22 3 2 3 10 12.46 10 19 14 21 14 12.46 22 3'/></svg>
                                </div>
                                <div class='p-20 bc-e8' id='content'>
                                  <dl>
                                    <dt class='pb-15 fs-15 fw-600'>Status</dt>
                                    <div class='flex fs-13 fdc'>
                                      <dd class='md-ml-0'><a expr:href='data:blog.homepageUrl + &quot;search/label/Ongoing?&amp;max-results=20&quot;'>Ongoing</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Completed?&amp;max-results=20&quot;'>Completed</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Cancelled?&amp;max-results=20&quot;'>Cancelled</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Hiatus?&amp;max-results=20&quot;'>Hiatus</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Dropped?&amp;max-results=20&quot;'>Dropped</a></dd>
                                    </div>
                                  </dl>
                                  <dl>
                                    <dt class='pb-15 fs-15 fw-600'>Format</dt>
                                    <div class='flex fs-13 fdc'>
                                      <dd class='md-ml-0'><a expr:href='data:blog.homepageUrl + &quot;search/label/Manga?&amp;max-results=20&quot;'>Manga</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Manhua?&amp;max-results=20&quot;'>Manhua</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Manhwa?&amp;max-results=20&quot;'>Manhwa</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Web Novel (JP)?&amp;max-results=20&quot;'>Web Novel (JP)</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Web Novel (KR)?&amp;max-results=20&quot;'>Web Novel (KR)</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Web Novel (CN)?&amp;max-results=20&quot;'>Web Novel (CN)</a></dd>
                                      <dd><a expr:href='data:blog.homepageUrl + &quot;search/label/Doujinshi?&amp;max-results=20&quot;'>Doujinshi</a></dd>
                                    </div>
                                  </dl>

                                </div>
                               <div class='grid gtc-f141a gg-20 p-13'>
                                  
                                  <b:loop index='i' values='data:posts' var='post'>
                                    
                                                                 

                                <b:include name='Series'/>
                                    
                                  </b:loop>
                                </div>
                                <b:include cond='data:view.isMultipleItems and !data:view.isHomepage' name='postPagination'/>
                              </article>
                            </b:includable>
                          </b:widget>
                          <b:widget cond='data:view.isHomepage' id='HTML7' locked='true' title='Ads' type='HTML' version='2' visible='true'>
                            <b:widget-settings>
                              <b:widget-setting name='content'>&lt;script async src=&quot;https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-6196240383890230&quot;
     crossorigin=&quot;anonymous&quot;&gt;&lt;/script&gt;</b:widget-setting>
                            </b:widget-settings>
                            <b:includable id='main'>
                              <b:class name='ads'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                          </b:widget>
                          <b:widget cond='data:view.isHomepage' id='HTML1' locked='false' title='Recomendation' type='HTML' version='2' visible='true'>
                            <b:widget-settings>
                              <b:widget-setting name='content'>&lt;section id=&quot;mTP_Slider&quot; class=&quot;top&quot;&gt;
&lt;script&gt;mTP.run(jQuery, false, 5, 5)&lt;/script&gt;
&lt;/section&gt;</b:widget-setting>
                            </b:widget-settings>
                            <b:includable id='main'>
                              

                              <h3 class='title flex jcsb aic'>
    <span class='flex aic g5'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 20 20' width='1em' xmlns='http://www.w3.org/2000/svg'><path d='M18 6.01L14 9V7h-4l-5 8H2v-2h2l5-8h5V3zM2 5h3l1.15 2.17l-1.12 1.8L4 7H2V5zm16 9.01L14 17v-2H9l-1.15-2.17l1.12-1.8L10 13h4v-2z' fill='currentColor'/></svg>
      <data:title/></span>
    <span class='bg-main ttu p-3y6x fs-9 r2 c-fff cp' onclick='mTP.run(jQuery, &apos;Series&apos;, 5, 5)'>Reload</span>
</h3>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                          </b:widget>
                          <b:widget cond='data:view.isHomepage' id='HTML5' locked='false' title='Blog' type='HTML' version='2' visible='false'>
                            <b:widget-settings>
                              <b:widget-setting name='content'>&lt;style&gt;

.side h2:before{content:&quot;&quot;;position:absolute;left:0;bottom:-2px;width:100%;height:2px;background:#eee;}
.side h2:after{content:&quot;&quot;;position:absolute;left:0;bottom:-2px;width:35%;height:2px;background:#542a78;}
.recentposts{column-count: 3;padding-left: 0;font-size:14px;line-height:1.4em;column-width: 200px;}
.recentposts li{overflow:hidden;}
.recentposts li a{transition:all 0.2s;text-decoration:none;}
.recentposts li a:hover{opacity:0.8;}
.recentposts .thumbnail img{width:100%;max-height: 140px;object-fit: cover;}
.recentposts .title a{color:#e74c3c;}
.recentposts .recent-info{display: flex;margin-top:5px;font-size:13px;color:#888;}
.recentposts .recent-info a{color:#888;}
.recentposts .recent-info span:not(:last-of-type):after{content:&quot;-&quot;;margin:0 4px;}
.recentposts .snippet{margin-top: 5px;margin-bottom: 0;color:#999;}
.dark-mode .recentposts .snippet{color:#444;}
.recent-title{margin-top: 10px;margin-bottom: 0;line-height: 1.5;font-size:16px;overflow:hidden;text-overflow:ellipsis;display:-webkit-box;-webkit-box-orient:vertical;-webkit-line-clamp:2;font-weight: 500;min-height: 45px;}
&lt;/style&gt;

&lt;div class=&#39;side&#39; id=&#39;side&#39;&gt;

  &lt;ul class=&#39;recentposts&#39; id=&#39;recentposts&#39;&gt;&lt;/ul&gt;
&lt;/div&gt;
&lt;script type=&quot;text/javascript&quot;&gt;
  function embed_post(){
    var totalpost = 6;
    var elements = &quot;&quot;;
    for (var i = 0; i &lt; 6; i++){
      elements += &quot;&lt;div class=&#39;post&#39;&gt;&lt;/div&gt;&quot;;
    }
    document.getElementById(&#39;main&#39;).innerHTML = elements;
  }

  var rp_blogUrl = &quot;https://www.yoursite.in&quot;;
  var rp_totalItem = 3;
  var rp_showThumbnail = 1;
  var rp_showInfo = 1;
  var rp_showSnippet = 1;
  var rp_thumbnailSize = [256,144];
  var rp_snippetLength = 70;
  (function(){
    function filterTags(g, h) {
      var e = g.split(&quot;&lt;&quot;);
      for (var f = 0; f &lt; e.length; f++) {
        if (e[f].indexOf(&quot;&gt;&quot;) != -1) {
          e[f] = e[f].substring(e[f].indexOf(&quot;&gt;&quot;) + 1, e[f].length)
        }
      }
      e = e.join(&quot;&quot;);
      e = e.substring(0, h - 1);
      return e
    }

    var callback = &quot;recentposts&quot;;
    var containerID = document.getElementById(&quot;recentposts&quot;);
    window[callback] = function(data){
      var elements = &quot;&quot;;
      for (var i = 0; i &lt; rp_totalItem; i++){
        if (i == data.feed.entry.length){
          break;
        }

        var entry = data.feed.entry[i];
        var item_title = entry.title.$t, item_comment = [], item_url, item_thumb, item_date, item_label, item_snippet;

        for (var j = 0; j &lt; entry.link.length; j++) {
          if (&quot;replies&quot; == entry.link[j].rel &amp;&amp; &quot;text/html&quot; == entry.link[j].type) {
                  item_comment[0] = entry.link[j].title;
                  item_comment[1] = entry.link[j].href;
          }
          if (&quot;alternate&quot; == entry.link[j].rel) {
            item_url = entry.link[j].href;
            break;
          }
        }

        item_thumb = &quot;//3.bp.blogspot.com/-FHhLnZncaZE/XF-c-Ey_n2I/AAAAAAAAAkA/TXD5_-NJvH0nWEVliT1vS0RR_R2lsr0TQCLcBGAs/s72-c/no-image.jpg&quot;;
        if (&quot;media$thumbnail&quot; in entry) {
          item_thumb = entry.media$thumbnail.url.replace(&quot;/s72-c/&quot;, &quot;/w&quot; + rp_thumbnailSize[0] + &quot;-h&quot; + rp_thumbnailSize[1] + &quot;-p-k-no-nu/&quot;);
        }

        var date = entry.published.$t,
        year = date.substring(0, 4),
        digit = date.substring(5, 7),
        day = date.substring(8, 10),
        month = [&quot;&quot;, &quot;January&quot;, &quot;Februari&quot;, &quot;Maret&quot;, &quot;April&quot;, &quot;Mei&quot;, &quot;Juni&quot;, &quot;Juli&quot;, &quot;Agustus&quot;, &quot;September&quot;, &quot;Oktober&quot;, &quot;November&quot;, &quot;Desember&quot;];
        item_date = month[parseInt(digit)] + &quot; &quot;+ day + &quot;, &quot; + year;

        item_label = &quot;&quot;;
        for (var n = 0; n &lt; entry.category.length; n++){
          var urlLabels = rp_blogUrl.replace(/\/$/, &quot;&quot;) + &quot;/search/label/&quot; + entry.category[n].term + &quot;?max-results=6&quot;; 
          item_label += &quot;&lt;a href=&#39;&quot; + urlLabels + &quot;&#39;&gt;&quot; + entry.category[n].term + &quot;&lt;/a&gt;&quot;;
        }

        item_snippet = &quot;&quot;;
        if (&quot;content&quot; in entry) {
          item_snippet = entry.content.$t
        } else {
          if (&quot;summary&quot; in entry) {
            item_snippet = entry.summary.$t
          }
        }
        item_snippet = filterTags(item_snippet, rp_snippetLength);

        elements += &quot;&lt;li&gt;&quot;;
        if (rp_showThumbnail){ 
          elements += &quot;&lt;div class=&#39;thumbnail&#39;&gt;&lt;a href=&#39;&quot;+item_url+&quot;&#39;&gt;&lt;img class=&#39;r2&#39; src=&#39;&quot;+item_thumb+&quot;&#39;/&gt;&lt;/a&gt;&lt;/div&gt;&quot;;
        }
        elements += &quot;&lt;h4 class=&#39;recent-title&#39;&gt;&lt;a href=&#39;&quot;+item_url+&quot;&#39;&gt;&quot;+item_title+&quot;&lt;/a&gt;&lt;/h4&gt;&quot;;
        if (rp_showInfo){
          elements += &quot;&lt;div class=&#39;recent-info&#39;&gt;&quot;;
          elements += &quot;&lt;time class=&#39;times&#39;&gt;&quot;+item_date+&quot;&lt;/time&gt;&lt;span class=&#39;mla&#39;&gt;&lt;a href=&#39;&quot;+item_comment[1]+&quot;&#39;&gt;&quot;+item_comment[0]+&quot;&lt;/a&gt;&lt;/span&gt;&quot;;
          elements += &quot;&lt;/div&gt;&quot;;
        }
        if (rp_showSnippet){
          elements += &quot;&lt;p class=&#39;snippet&#39;&gt;&quot;+item_snippet+&quot;...&lt;/p&gt;&quot;;
        }
        elements += &quot;&lt;/li&gt;&quot;;
      }
      containerID.innerHTML = elements;
    }
    var js = document.createElement(&quot;script&quot;);
    var blogUrl = rp_blogUrl.replace(/\/$/, &quot;&quot;);
    js.src = blogUrl + &quot;/feeds/posts/default/-/Tema?orderby=published&amp;alt=json-in-script&amp;max-results=&quot; + rp_totalItem + &quot;&amp;callback=&quot; + callback;
    document.getElementsByTagName(&quot;head&quot;)[0].appendChild(js);
  })();
&lt;/script&gt;</b:widget-setting>
                            </b:widget-settings>
                            <b:includable id='main'>
  <h3 class='title flex aic'>
    <svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg'><circle cx='6.18' cy='17.82' fill='currentColor' r='2.18'/><path d='M4 4.44v2.83c7.03 0 12.73 5.7 12.73 12.73h2.83c0-8.59-6.97-15.56-15.56-15.56zm0 5.66v2.83c3.9 0 7.07 3.17 7.07 7.07h2.83c0-5.47-4.43-9.9-9.9-9.9z' fill='currentColor'/></svg>
<data:title/>
</h3>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                          </b:widget>
                        </b:section>
                        </b:tag>
                        <b:tag cond='data:view.isMultipleItems and !data:view.isLabelSearch' id='sidebar' name='div'>
                        <b:section cond='data:view.isMultipleItems and !data:view.isLabelSearch' id='search' showaddelement='true'>
                          <b:widget id='BlogSearch2' locked='true' title='Search' type='BlogSearch' version='2' visible='true'>
                            <b:includable id='main'>
            <h3 class='title flex aic'>
    <svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 16 16' width='1em' xmlns='http://www.w3.org/2000/svg'><path d='M6 12v-1h4v1H6zM4 7h8v1H4V7zm10-4v1H2V3h12z' fill='currentColor'/></svg>
<data:title/>
</h3>
            <b:include name='content'/>
          </b:includable>
                            <b:includable id='content'>
            <section class='quickfilter' role='search'>
              <div class='filters'>
                <div class='opt'>
                  <!-- List Label -->
                  <div class='filter'>
                    <input class='hidden chk' id='Genre' name='genre' type='checkbox'/>
                    <label class='dropdown-toggle' data-toggle='dropdown' for='Genre'> Genre <span class='value' data-label-placement='true'>All</span> </label>
                    <ul class='dropdown-menu lg c4'>
                      <li>
                        <input class='genre' id='Action' type='checkbox' value='Action'/>
                        <label for='Action'>Action</label>
                      </li>
                      <li>
                        <input class='genre' id='Adventurer' type='checkbox' value='Adventurer'/>
                        <label for='Adventurer'>Adventurer</label>
                      </li>
                      <li>
                        <input class='genre' id='Comedy' type='checkbox' value='Comedy'/>
                        <label for='Comedy'>Comedy</label>
                      </li>
                      <li>
                        <input class='genre' id='Dementia' type='checkbox' value='Dementia'/>
                        <label for='Dementia'>Dementia</label>
                      </li>
                      <li>
                        <input class='genre' id='Demons' type='checkbox' value='Demons'/>
                        <label for='Demons'>Demons</label>
                      </li>
                      <li>
                        <input class='genre' id='Drama' type='checkbox' value='Drama'/>
                        <label for='Drama'>Drama</label>
                      </li>
                      <li>
                        <input class='genre' id='Ecchi' type='checkbox' value='Ecchi'/>
                        <label for='Ecchi'>Ecchi</label>
                      </li>
                      <li>
                        <input class='genre' id='Fantasy' type='checkbox' value='Fantasy'/>
                        <label for='Fantasy'>Fantasy</label>
                      </li>
                      <li>
                        <input class='genre' id='Game' type='checkbox' value='Game'/>
                        <label for='Game'>Game</label>
                      </li>
                      <li>
                        <input class='genre' id='Harem' type='checkbox' value='Harem'/>
                        <label for='Harem'>Harem</label>
                      </li>
                      <li>
                        <input class='genre' id='Historical' type='checkbox' value='Historical'/>
                        <label for='Historical'>Historical</label>
                      </li>
                      <li>
                        <input class='genre' id='Horror' type='checkbox' value='Horror'/>
                        <label for='Horror'>Horror</label>
                      </li>
                      <li>
                        <input class='genre' id='Josei' type='checkbox' value='Josei'/>
                        <label for='Josei'>Josei</label>
                      </li>
                      <li>
                        <input class='genre' id='Magic' type='checkbox' value='Magic'/>
                        <label for='Magic'>Magic</label>
                      </li>
                      <li>
                        <input class='genre' id='Martial Arts' type='checkbox' value='Martial Arts'/>
                        <label for='Martial Arts'>Martial Arts</label>
                      </li>
                      <li>
                        <input class='genre' id='Mecha' type='checkbox' value='Mecha'/>
                        <label for='Mecha'>Mecha</label>
                      </li>
                      <li>
                        <input class='genre' id='Military' type='checkbox' value='Military'/>
                        <label for='Military'>Military</label>
                      </li>
                      <li>
                        <input class='genre' id='Music' type='checkbox' value='Music'/>
                        <label for='Music'>Music</label>
                      </li>
                      <li>
                        <input class='genre' id='Mystery' type='checkbox' value='Mystery'/>
                        <label for='Mystery'>Mystery</label>
                      </li>
                      <li>
                        <input class='genre' id='Parody' type='checkbox' value='Parody'/>
                        <label for='Parody'>Parody</label>
                      </li>
                      <li>
                        <input class='genre' id='Police' type='checkbox' value='Police'/>
                        <label for='Police'>Police</label>
                      </li>
                      <li>
                        <input class='genre' id='Psychological' type='checkbox' value='Psychological'/>
                        <label for='Psychological'>Psychological</label>
                      </li>
                      <li>
                        <input class='genre' id='Romance' type='checkbox' value='Romance'/>
                        <label for='Romance'>Romance</label>
                      </li>
                      <li>
                        <input class='genre' id='Samurai' type='checkbox' value='Samurai'/>
                        <label for='Samurai'>Samurai</label>
                      </li>
                      <li>
                        <input class='genre' id='School' type='checkbox' value='School'/>
                        <label for='School'>School</label>
                      </li>
                      <li>
                        <input class='genre' id='Sci-Fi' type='checkbox' value='Sci-Fi'/>
                        <label for='Sci-Fi'>Sci-Fi</label>
                      </li>
                      <li>
                        <input class='genre' id='Seinen' type='checkbox' value='Seinen'/>
                        <label for='Seinen'>Seinen</label>
                      </li>
                      <li>
                        <input class='genre' id='Shoujo' type='checkbox' value='Shoujo'/>
                        <label for='Shoujo'>Shoujo</label>
                      </li>
                      <li>
                        <input class='genre' id='Shoujo Ai' type='checkbox' value='Shoujo Ai'/>
                        <label for='Shoujo Ai'>Shoujo Ai</label>
                      </li>
                      <li>
                        <input class='genre' id='Shounen' type='checkbox' value='Shounen'/>
                        <label for='Shounen'>Shounen</label>
                      </li>
                      <li>
                        <input class='genre' id='Slice of Life' type='checkbox' value='Slice of Life'/>
                        <label for='Slice of Life'>Slice of Life</label>
                      </li>
                      <li>
                        <input class='genre' id='Space' type='checkbox' value='Space'/>
                        <label for='Space'>Space</label>
                      </li>
                      <li>
                        <input class='genre' id='Sports' type='checkbox' value='Sports'/>
                        <label for='Sports'>Sports</label>
                      </li>
                      <li>
                        <input class='genre' id='Super Power' type='checkbox' value='Super Power'/>
                        <label for='Super Power'>Super Power</label>
                      </li>
                      <li>
                        <input class='genre' id='Supernatural' type='checkbox' value='Supernatural'/>
                        <label for='Supernatural'>Supernatural</label>
                      </li>
                      <li>
                        <input class='genre' id='Thriller' type='checkbox' value='Thriller'/>
                        <label for='Thriller'>Thriller</label>
                      </li>
                      <li>
                        <input class='genre' id='Vampire' type='checkbox' value='Vampire'/>
                        <label for='Vampire'>Vampire</label>
                      </li>
                      <li>
                        <input class='genre' id='Work Life' type='checkbox' value='Work Life'/>
                        <label for='Work Life'>Work Life</label>
                      </li>
                      <li>
                        <input class='genre' id='Yuri' type='checkbox' value='Yuri'/>
                        <label for='Yuri'>Yuri</label>
                      </li>
                    </ul>
                  </div>
                  <div class='filter'>
                    <input class='hidden chk' id='Status' name='status' type='checkbox'/>
                    <label class='dropdown-toggle' data-toggle='dropdown' for='Status'> Status <span class='value' data-label-placement='true'>All</span> </label>
                    <ul class='dropdown-menu lg c1'>
                      <li>
                        <input class='genre' id='Ongoing' type='checkbox' value='Ongoing'/>
                        <label for='Ongoing'>Ongoing</label>
                      </li>
                      <li>
                        <input class='genre' id='Completed' type='checkbox' value='Completed'/>
                        <label for='Completed'>Completed</label>
                      </li>
                      <li>
                        <input class='genre' id='Dropped' type='checkbox' value='Dropped'/>
                        <label for='Dropped'>Dropped</label>
                      </li>
                      <li>
                        <input class='genre' id='Upcoming' type='checkbox' value='Upcoming'/>
                        <label for='Upcoming'>Upcoming</label>
                      </li>
                    </ul>
                  </div>
                  <div class='filter'>
                    <input class='hidden chk' id='Type' name='type' type='checkbox'/>
                    <label class='dropdown-toggle' data-toggle='dropdown' for='Type'> Type <span class='value' data-label-placement='true'>All</span> </label>
                    <ul class='dropdown-menu lg c1'>
                      <li>
                        <input class='genre' id='Manga' type='checkbox' value='Manga'/>
                        <label for='Manga'>Manga</label>
                      </li>
                      <li>
                        <input class='genre' id='Manhua' type='checkbox' value='Manhua'/>
                        <label for='Manhua'>Manhua</label>
                      </li>
                      <li>
                        <input class='genre' id='Manhwa' type='checkbox' value='Manhwa'/>
                        <label for='Manhwa'>Manhwa</label>
                      </li>
                      <li>
                        <input class='genre' id='Novel' type='checkbox' value='Novel'/>
                        <label for='Novel'>Novel</label>
                      </li>
                    </ul>
                  </div>
                  <div class='filter'>
                    <input class='hidden chk' id='Lang' name='lang' type='checkbox'/>
                    <label class='dropdown-toggle' data-toggle='dropdown' for='Lang'> Language <span class='value' data-label-placement='true'>All</span> </label>
                    <ul class='dropdown-menu lg c1'>
                      <li>
                        <input class='genre' id='Indonesian' type='checkbox' value='Indonesian'/>
                        <label for='Indonesian'>Indonesian</label>
                      </li>
                      <li>
                        <input class='genre' id='English' type='checkbox' value='English'/>
                        <label for='English'>English</label>
                      </li>
                    </ul>
                  </div>
                </div>

                <div class='p-15'>
                <button class='submit' type='submit'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' style='vertical-align: -0.125em;' viewBox='0 0 20 20' width='1em' xmlns='http://www.w3.org/2000/svg'><path d='M8.5 3a5.5 5.5 0 0 1 4.383 8.823l4.147 4.147a.75.75 0 0 1-.976 1.133l-.084-.073l-4.147-4.147A5.5 5.5 0 1 1 8.5 3Zm0 1.5a4 4 0 1 0 0 8a4 4 0 0 0 0-8Z' fill='currentColor'/></svg>Filter  <span class='count'> </span></button>
                </div>
                <!-- Hasil -->
                <div id='result'/>
                
<script>/*<![CDATA[*/
var num = 15;
var newtab = false;
$('.submit').click(function(){
var validator = document.getElementsByClassName('genre');
var o = [];
for(var i=0;i<validator.length;i++){
   if(validator[i].checked){
    o.push(validator[i].value)
	}
}
window.open(location.protocol+ '//' + location.hostname + '/search/label/' + o.join('+') + '?&max-results=' + num, newtab == true ? '_blank' : '_self');
});
/*]]>*/</script>
                
              </div>
            </section>
</b:includable>
                            <b:includable id='searchForm'>
  <form expr:action='data:blog.searchUrl'>
    <b:attr cond='not data:view.isPreview' name='target' value='_top'/>
    <b:include name='urlParamsAsFormInput'/>
    <div class='searchf filter'>
      <input autocomplete='off' expr:aria-label='data:messages.search' expr:placeholder='data:messages.search' expr:value='data:view.isSearch ? data:view.search.query.escaped : &quot;&quot;' name='q'/>
    </div>
    <b:include name='searchSubmit'/>
  </form>
</b:includable>
                            <b:includable id='searchSubmit'>
  
</b:includable>
                          </b:widget>
                        </b:section>
                          <b:tag class='s1 bc-fff r2 mb-20' cond='data:view.isMultipleItems and !data:view.isLabelSearch' name='div'>
<b:if cond='data:view.isMultipleItems and !data:view.isLabelSearch'>
<h3 class='title flex aic'>
<svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg'><path d='M21 7a.78.78 0 0 0 0-.21a.64.64 0 0 0-.05-.17a1.1 1.1 0 0 0-.09-.14a.75.75 0 0 0-.14-.17l-.12-.07a.69.69 0 0 0-.19-.1h-.2A.7.7 0 0 0 20 6h-5a1 1 0 0 0 0 2h2.83l-4 4.71l-4.32-2.57a1 1 0 0 0-1.28.22l-5 6a1 1 0 0 0 .13 1.41A1 1 0 0 0 4 18a1 1 0 0 0 .77-.36l4.45-5.34l4.27 2.56a1 1 0 0 0 1.27-.21L19 9.7V12a1 1 0 0 0 2 0V7Z' fill='currentColor'/></svg>Trending</h3>
<div class='tabx flex lsn p-6 m-10 tac tab r4'>
<span class='active f1 r3 cp' data-tab='PopularPosts3'>Mingguan</span>
<span class='f1 r3 cp' data-tab='PopularPosts4'>Bulanan</span>
<span class='f1 r3 cp' data-tab='PopularPosts5'>Semua</span>
</div>
  <script>
          $(document).ready(function(){

	$(&#39;.tabx span&#39;).click(function(){
		var tab_id = $(this).attr(&#39;data-tab&#39;);

		$(&#39;.tabx span&#39;).removeClass(&#39;active&#39;);
		$(&#39;.PopularPosts&#39;).removeClass(&#39;current&#39;);

		$(this).addClass(&#39;active&#39;);
		$(&quot;#&quot;+tab_id).addClass(&#39;current&#39;);
	})

})
</script>
</b:if>
                          <b:section cond='data:view.isMultipleItems and !data:view.isLabelSearch' id='popular' showaddelement='true'>
                            <b:widget id='PopularPosts3' locked='true' title='Minggu' type='PopularPosts' version='2' visible='true'>
                              <b:widget-settings>
                                <b:widget-setting name='numItemsToShow'>10</b:widget-setting>
                                <b:widget-setting name='showThumbnails'>true</b:widget-setting>
                                <b:widget-setting name='showSnippets'>true</b:widget-setting>
                                <b:widget-setting name='timeRange'>LAST_WEEK</b:widget-setting>
                              </b:widget-settings>
                              <b:includable id='main' var='this'>
                              <b:class name='current'/>

                              
                                <b:include name='snippetedPosts'/>
                              
                            </b:includable>
                              <b:includable id='blogThisShare'>
                              <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=270,width=475\&quot;); return false;&quot;' var='onclick'>
                                <b:include name='platformShare'/>
                              </b:with>
                            </b:includable>
                              <b:includable id='bylineByName' var='byline'>
                              <b:switch var='data:byline.name'>
                                <b:case value='share'/>
                                <b:include cond='data:post.shareUrl' name='postShareButtons'/>
                                <b:case value='comments'/>
                                <b:include cond='data:post.allowComments' name='postCommentsLink'/>
                                <b:case value='location'/>
                                <b:include cond='data:post.location' name='postLocation'/>
                                <b:case value='timestamp'/>
                                <b:include cond='not data:view.isPage' name='postTimestamp'/>
                                <b:case value='author'/>
                                <b:include name='postAuthor'/>
                                <b:case value='labels'/>
                                <b:include cond='data:post.labels' name='postLabels'/>
                                <b:case value='icons'/>
                                <b:include cond='data:post.emailPostUrl' name='emailPostIcon'/>
                              </b:switch>
                            </b:includable>
                              <b:includable id='bylineRegion' var='regionItems'>
                              <b:loop values='data:regionItems' var='byline'>
                                <b:include data='byline' name='bylineByName'/>
                              </b:loop>
                            </b:includable>
                              <b:includable id='commentsLink'>
                              <a class='comment-link' expr:href='data:post.commentsUrl' expr:onclick='data:post.commentsUrlOnclick'>
                                <b:if cond='data:post.numberOfComments &gt; 0'>
                                  <b:message name='messages.numberOfComments'>
                                    <b:param expr:value='data:post.numberOfComments' name='numComments'/>
                                  </b:message>
                                  <b:else/>
                                  <data:messages.postAComment/>
                                </b:if>
                              </a>
                            </b:includable>
                              <b:includable id='commentsLinkIframe'>
                              <!-- G+ comments, no longer available. The includable is retained for backwards-compatibility. -->
                            </b:includable>
                              <b:includable id='emailPostIcon'>
                              <span class='byline post-icons'>
                                <!-- email post links -->
                                <span class='item-action'>
                                  <a expr:href='data:post.emailPostUrl' expr:title='data:messages.emailPost'>
                                    <b:include data='{ iconClass: &quot;touch-icon sharing-icon&quot; }' name='emailIcon'/>
                                  </a>
                                </span>
                              </span>
                            </b:includable>
                              <b:includable id='facebookShare'>
                              <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=430,width=640\&quot;); return false;&quot;' var='onclick'>
                                <b:include name='platformShare'/>
                              </b:with>
                            </b:includable>
                              <b:includable id='footerBylines'>
                              <b:if cond='data:widgets.Blog.first.footerBylines'>
                                <b:loop index='i' values='data:widgets.Blog.first.footerBylines' var='region'>
                                  <b:if cond='not data:region.items.empty'>
                                    <div expr:class='&quot;post-footer-line post-footer-line-&quot; + (data:i + 1)'>
                                      <b:with value='&quot;footer-&quot; + (data:i + 1)' var='regionName'>
                                        <b:include data='region.items' name='bylineRegion'/>
                                      </b:with>
                                    </div>
                                  </b:if>
                                </b:loop>
                              </b:if>
                            </b:includable>
                              <b:includable id='googlePlusShare'>
                            </b:includable>
                              <b:includable id='headerByline'>
                              <b:if cond='data:widgets.Blog.first.headerByline'>
                                <div class='post-header'>
                                  <div class='post-header-line-1'>
                                    <b:with value='&quot;header-1&quot;' var='regionName'>
                                      <b:include data='data:widgets.Blog.first.headerByline.items' name='bylineRegion'/>
                                    </b:with>
                                  </div>
                                </div>
                              </b:if>
                            </b:includable>
                              <b:includable id='linkShare'>
                              <b:with value='&quot;window.prompt(\&quot;Copy to clipboard: Ctrl+C, Enter\&quot;, \&quot;&quot; + data:originalUrl + &quot;\&quot;); return false;&quot;' var='onclick'>
                                <b:include name='platformShare'/>
                              </b:with>
                            </b:includable>
                              <b:includable id='otherSharingButton'>
                              <span class='sharing-platform-button sharing-element-other' expr:aria-label='data:messages.shareToOtherApps.escaped' expr:data-url='data:originalUrl' expr:title='data:messages.shareToOtherApps.escaped' role='menuitem' tabindex='-1'>
                                <b:with value='{key: &quot;sharingOther&quot;}' var='platform'>
                                  <b:include name='sharingPlatformIcon'/>
                                </b:with>
                                <span class='platform-sharing-text'><data:messages.shareOtherApps.escaped/></span>
                              </span>
                            </b:includable>
                              <b:includable id='platformShare'>
                              <a expr:class='&quot;goog-inline-block sharing-&quot; + data:platform.key' expr:data-url='data:originalUrl' expr:href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:onclick='data:onclick ? data:onclick : &quot;&quot;' expr:title='data:platform.shareMessage' target='_blank'>
                                <span class='share-button-link-text'>
                                  <data:platform.shareMessage/>
                                </span>
                              </a>
                            </b:includable>
                              <b:includable id='postAuthor'>
                              <span class='byline post-author vcard'>
                                <span class='post-author-label'>
                                  <data:byline.label/>
                                </span>
                                <span class='fn'>
                                  <b:if cond='data:post.author.profileUrl'>
                                    <meta expr:content='data:post.author.profileUrl'/>
                                    <a class='g-profile' expr:href='data:post.author.profileUrl' rel='author' title='author profile'>
                                      <span><data:post.author.name/></span>
                                    </a>
                                    <b:else/>
                                    <span><data:post.author.name/></span>
                                  </b:if>
                                </span>
                              </span>
                            </b:includable>
                              <b:includable id='postCommentsLink'>
                              <span class='byline post-comment-link container'>
                                <b:include cond='data:post.commentSource != 1' name='commentsLink'/>
                              </span>
                            </b:includable>
                              <b:includable id='postJumpLink' var='post'>
                              <div class='jump-link flat-button'>
                                <a expr:href='data:post.url fragment &quot;more&quot;' expr:title='data:post.title'>
                                  <b:eval expr='data:blog.jumpLinkMessage'/>
                                </a>
                              </div>
                            </b:includable>
                              <b:includable id='postLabels'>
                              <span class='span-spc fs-13'>
                                <b>Genres</b>
                                <b:loop index='i' values='data:post.labels' var='label'>
                                  <b:if cond='data:label.name in data:Genre or data:label.name in data:Genre2 or data:label.name in data:Demographic'>
                                  <a expr:href='data:label.url' rel='tag'>
                                    <data:label.name/>,
                                  </a>
                                  </b:if>
                                </b:loop>
                              </span>
                            </b:includable>
                              <b:includable id='postLocation'>
                              <span class='byline post-location'>
                                <data:byline.label/>
                                <a expr:href='data:post.location.mapsUrl' target='_blank'><data:post.location.name/></a>
                              </span>
                            </b:includable>
                              <b:includable id='postReactions'>
                              <!-- Reaction feature no longer available. The includable is retained for backwards-compatibility. -->
                            </b:includable>
                              <b:includable id='postShareButtons'>
                              <div class='byline post-share-buttons goog-inline-block'>
                                <b:with value='data:sharingId ?: ((data:widget.instanceId ?: &quot;sharing&quot;) + &quot;-&quot; + (data:regionName ?: &quot;byline&quot;) + &quot;-&quot; + data:post.id)' var='sharingId'>
                                  <!-- Note: 'sharingButtons' includable is from the default Sharing widget markup. -->
                                  <b:include data='{                                                sharingId: data:sharingId,                                                originalUrl: data:post.url,                                                platforms: data:this.sharing.platforms,                                                shareUrl: data:post.shareUrl,                                                shareTitle: data:post.title,                                              }' name='sharingButtons'/>
                                </b:with>
                              </div>
                            </b:includable>
                              <b:includable id='postTimestamp'>
                              <span class='byline post-timestamp'>
                                <data:byline.label/>
                                <b:if cond='data:post.url'>
                                  <meta expr:content='data:post.url.canonical'/>
                                  <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'>
                                    <time class='published' expr:datetime='data:post.date.iso8601' expr:title='data:post.date.iso8601'>
                                      <data:post.date/>
                                    </time>
                                  </a>
                                </b:if>
                              </span>
                            </b:includable>
                              <b:includable id='sharingButton'>
                              <span expr:aria-label='data:platform.shareMessage' expr:class='&quot;sharing-platform-button sharing-element-&quot; + data:platform.key' expr:data-href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:data-url='data:originalUrl' expr:title='data:platform.shareMessage' role='menuitem' tabindex='-1'>
                                <b:include name='sharingPlatformIcon'/>
                                <span class='platform-sharing-text'><data:platform.name/></span>
                              </span>
                            </b:includable>
                              <b:includable id='sharingButtonContent'>
                              <div class='flat-icon-button ripple'>
                                <b:include name='shareIcon'/>
                              </div>
                            </b:includable>
                              <b:includable id='sharingButtons'>
                              <div class='sharing' expr:aria-owns='&quot;sharing-popup-&quot; + data:sharingId' expr:data-title='data:shareTitle'>
                                <button class='sharing-button touch-icon-button' expr:aria-controls='&quot;sharing-popup-&quot; + data:sharingId' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-button-&quot; + data:sharingId' role='button'>
                                  <b:include name='sharingButtonContent'/>
                                </button>
                                <b:include name='sharingButtonsMenu'/>
                              </div>
                            </b:includable>
                              <b:includable id='sharingButtonsMenu'>
                              <div class='share-buttons-container'>
                                <ul aria-hidden='true' class='share-buttons hidden' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-popup-&quot; + data:sharingId' role='menu'>
                                  <b:loop values='(data:platforms ?: data:blog.sharing.platforms) filter (p =&gt; p.key not in {&quot;blogThis&quot;})' var='platform'>
                                    <li>
                                      <b:include name='sharingButton'/>
                                    </li>
                                  </b:loop>
                                  <li aria-hidden='true' class='hidden'>
                                    <b:include name='otherSharingButton'/>
                                  </li>
                                </ul>
                              </div>
                            </b:includable>
                              <b:includable id='sharingPlatformIcon'>
                              <b:include data='{ iconClass: (&quot;touch-icon sharing-&quot; + data:platform.key) }' expr:name='data:platform.key + &quot;Icon&quot;'/>
                            </b:includable>
                              <b:includable id='snippetedPostByline'>
                              <b:with value='(data:widgets first (w =&gt; w.type == &quot;Blog&quot;)).allBylineItems' var='blogBylines'>
                                <div class='item-byline'>
                                  <b:with value='data:blogBylines first (i =&gt; i.name == &quot;author&quot;)' var='byline'>
                                    <b:include cond='data:byline and data:this.postDisplay.showAuthor' data='post' name='postAuthor'/>
                                  </b:with>
                                  <b:with value='data:blogBylines first (i =&gt; i.name == &quot;timestamp&quot;)' var='byline'>
                                    <b:include cond='data:byline and data:this.postDisplay.showDate' data='post' name='postTimestamp'/>
                                  </b:with>
                                </div>
                              </b:with>
                            </b:includable>
                              <b:includable id='snippetedPostContent'>
                              <div class='grid pcc'><div class='w-25 h25 tac lh-25px r2f'><b:eval expr='data:num'/></div></div>
                              <b:include cond='data:this.postDisplay.showFeaturedImage and data:post.featuredImage' name='snippetedPostThumbnail'/>
                              <b:include cond='data:this.postDisplay.showTitle' name='snippetedPostTitle'/>
                            </b:includable>
                              <b:includable id='snippetedPostThumbnail'>
                              <div class='item-thumbnail'>
                                <a expr:href='data:post.url'>
                                  <b:include data='{                         image: data:post.featuredImage,                         imageSizes: [72, 144],                         imageRatio: &quot;58:75&quot;,                         sourceSizes: &quot;80px&quot;                        }' name='responsiveImage'/>
                                </a>
                              </div>
                            </b:includable>
                              <b:includable id='snippetedPostTitle'>
                              <div>
                              <b:if cond='data:post.title != &quot;&quot;'>
                                <h3 class='post-title m-0 fs-15'><a expr:href='data:post.url'><data:post.title/></a></h3>
                              </b:if>
                                <b:include name='postLabels'/>
                                <b:include name='rbt'/>
                              </div>
                            </b:includable>
                              <b:includable id='snippetedPosts'>
                              <b:with value='data:posts filter (p =&gt; p.labels none (l =&gt; l.name == &quot;Chapter&quot;))' var='posts'>
                                <!-- Don't render the post that we're currently already looking at. -->
                                <b:loop index='i' values='data:posts filter (p =&gt; p.id != data:view.postId)' var='post'>
                                  <b:with value='data:i + 1' var='num'>
                                  <article class='p-y12x15 grid gtc-3c bb-1pxsf' role='article'>
                                    <b:include name='snippetedPostContent'/>
                                  </article>
                                    </b:with>
                                </b:loop>
                              
                              </b:with>
                            </b:includable>
                            </b:widget>
                            <b:widget id='PopularPosts4' locked='true' title='Bulan' type='PopularPosts' version='2' visible='true'>
                              <b:widget-settings>
                                <b:widget-setting name='numItemsToShow'>10</b:widget-setting>
                                <b:widget-setting name='showThumbnails'>true</b:widget-setting>
                                <b:widget-setting name='showSnippets'>true</b:widget-setting>
                                <b:widget-setting name='timeRange'>LAST_MONTH</b:widget-setting>
                              </b:widget-settings>
                              <b:includable id='main' var='this'>

                                <b:include name='snippetedPosts'/>
                              
                            </b:includable>
                              <b:includable id='blogThisShare'>
                              <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=270,width=475\&quot;); return false;&quot;' var='onclick'>
                                <b:include name='platformShare'/>
                              </b:with>
                            </b:includable>
                              <b:includable id='bylineByName' var='byline'>
                              <b:switch var='data:byline.name'>
                                <b:case value='share'/>
                                <b:include cond='data:post.shareUrl' name='postShareButtons'/>
                                <b:case value='comments'/>
                                <b:include cond='data:post.allowComments' name='postCommentsLink'/>
                                <b:case value='location'/>
                                <b:include cond='data:post.location' name='postLocation'/>
                                <b:case value='timestamp'/>
                                <b:include cond='not data:view.isPage' name='postTimestamp'/>
                                <b:case value='author'/>
                                <b:include name='postAuthor'/>
                                <b:case value='labels'/>
                                <b:include cond='data:post.labels' name='postLabels'/>
                                <b:case value='icons'/>
                                <b:include cond='data:post.emailPostUrl' name='emailPostIcon'/>
                              </b:switch>
                            </b:includable>
                              <b:includable id='bylineRegion' var='regionItems'>
                              <b:loop values='data:regionItems' var='byline'>
                                <b:include data='byline' name='bylineByName'/>
                              </b:loop>
                            </b:includable>
                              <b:includable id='commentsLink'>
                              <a class='comment-link' expr:href='data:post.commentsUrl' expr:onclick='data:post.commentsUrlOnclick'>
                                <b:if cond='data:post.numberOfComments &gt; 0'>
                                  <b:message name='messages.numberOfComments'>
                                    <b:param expr:value='data:post.numberOfComments' name='numComments'/>
                                  </b:message>
                                  <b:else/>
                                  <data:messages.postAComment/>
                                </b:if>
                              </a>
                            </b:includable>
                              <b:includable id='commentsLinkIframe'>
                              <!-- G+ comments, no longer available. The includable is retained for backwards-compatibility. -->
                            </b:includable>
                              <b:includable id='emailPostIcon'>
                              <span class='byline post-icons'>
                                <!-- email post links -->
                                <span class='item-action'>
                                  <a expr:href='data:post.emailPostUrl' expr:title='data:messages.emailPost'>
                                    <b:include data='{ iconClass: &quot;touch-icon sharing-icon&quot; }' name='emailIcon'/>
                                  </a>
                                </span>
                              </span>
                            </b:includable>
                              <b:includable id='facebookShare'>
                              <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=430,width=640\&quot;); return false;&quot;' var='onclick'>
                                <b:include name='platformShare'/>
                              </b:with>
                            </b:includable>
                              <b:includable id='footerBylines'>
                              <b:if cond='data:widgets.Blog.first.footerBylines'>
                                <b:loop index='i' values='data:widgets.Blog.first.footerBylines' var='region'>
                                  <b:if cond='not data:region.items.empty'>
                                    <div expr:class='&quot;post-footer-line post-footer-line-&quot; + (data:i + 1)'>
                                      <b:with value='&quot;footer-&quot; + (data:i + 1)' var='regionName'>
                                        <b:include data='region.items' name='bylineRegion'/>
                                      </b:with>
                                    </div>
                                  </b:if>
                                </b:loop>
                              </b:if>
                            </b:includable>
                              <b:includable id='googlePlusShare'>
                            </b:includable>
                              <b:includable id='headerByline'>
                              <b:if cond='data:widgets.Blog.first.headerByline'>
                                <div class='post-header'>
                                  <div class='post-header-line-1'>
                                    <b:with value='&quot;header-1&quot;' var='regionName'>
                                      <b:include data='data:widgets.Blog.first.headerByline.items' name='bylineRegion'/>
                                    </b:with>
                                  </div>
                                </div>
                              </b:if>
                            </b:includable>
                              <b:includable id='linkShare'>
                              <b:with value='&quot;window.prompt(\&quot;Copy to clipboard: Ctrl+C, Enter\&quot;, \&quot;&quot; + data:originalUrl + &quot;\&quot;); return false;&quot;' var='onclick'>
                                <b:include name='platformShare'/>
                              </b:with>
                            </b:includable>
                              <b:includable id='otherSharingButton'>
                              <span class='sharing-platform-button sharing-element-other' expr:aria-label='data:messages.shareToOtherApps.escaped' expr:data-url='data:originalUrl' expr:title='data:messages.shareToOtherApps.escaped' role='menuitem' tabindex='-1'>
                                <b:with value='{key: &quot;sharingOther&quot;}' var='platform'>
                                  <b:include name='sharingPlatformIcon'/>
                                </b:with>
                                <span class='platform-sharing-text'><data:messages.shareOtherApps.escaped/></span>
                              </span>
                            </b:includable>
                              <b:includable id='platformShare'>
                              <a expr:class='&quot;goog-inline-block sharing-&quot; + data:platform.key' expr:data-url='data:originalUrl' expr:href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:onclick='data:onclick ? data:onclick : &quot;&quot;' expr:title='data:platform.shareMessage' target='_blank'>
                                <span class='share-button-link-text'>
                                  <data:platform.shareMessage/>
                                </span>
                              </a>
                            </b:includable>
                              <b:includable id='postAuthor'>
                              <span class='byline post-author vcard'>
                                <span class='post-author-label'>
                                  <data:byline.label/>
                                </span>
                                <span class='fn'>
                                  <b:if cond='data:post.author.profileUrl'>
                                    <meta expr:content='data:post.author.profileUrl'/>
                                    <a class='g-profile' expr:href='data:post.author.profileUrl' rel='author' title='author profile'>
                                      <span><data:post.author.name/></span>
                                    </a>
                                    <b:else/>
                                    <span><data:post.author.name/></span>
                                  </b:if>
                                </span>
                              </span>
                            </b:includable>
                              <b:includable id='postCommentsLink'>
                              <span class='byline post-comment-link container'>
                                <b:include cond='data:post.commentSource != 1' name='commentsLink'/>
                              </span>
                            </b:includable>
                              <b:includable id='postJumpLink' var='post'>
                              <div class='jump-link flat-button'>
                                <a expr:href='data:post.url fragment &quot;more&quot;' expr:title='data:post.title'>
                                  <b:eval expr='data:blog.jumpLinkMessage'/>
                                </a>
                              </div>
                            </b:includable>
                              <b:includable id='postLabels'>
                              <span class='span-spc fs-13'>
                                <b>Genres</b>
                                <b:loop index='i' values='data:post.labels' var='label'>
                                  <b:if cond='data:label.name in data:Genre or data:label.name in data:Genre2 or data:label.name in data:Demographic'>
                                  <a expr:href='data:label.url' rel='tag'>
                                    <data:label.name/>,
                                  </a>
                                  </b:if>
                                </b:loop>
                              </span>
                            </b:includable>
                              <b:includable id='postLocation'>
                              <span class='byline post-location'>
                                <data:byline.label/>
                                <a expr:href='data:post.location.mapsUrl' target='_blank'><data:post.location.name/></a>
                              </span>
                            </b:includable>
                              <b:includable id='postReactions'>
                              <!-- Reaction feature no longer available. The includable is retained for backwards-compatibility. -->
                            </b:includable>
                              <b:includable id='postShareButtons'>
                              <div class='byline post-share-buttons goog-inline-block'>
                                <b:with value='data:sharingId ?: ((data:widget.instanceId ?: &quot;sharing&quot;) + &quot;-&quot; + (data:regionName ?: &quot;byline&quot;) + &quot;-&quot; + data:post.id)' var='sharingId'>
                                  <!-- Note: 'sharingButtons' includable is from the default Sharing widget markup. -->
                                  <b:include data='{                                                sharingId: data:sharingId,                                                originalUrl: data:post.url,                                                platforms: data:this.sharing.platforms,                                                shareUrl: data:post.shareUrl,                                                shareTitle: data:post.title,                                              }' name='sharingButtons'/>
                                </b:with>
                              </div>
                            </b:includable>
                              <b:includable id='postTimestamp'>
                              <span class='byline post-timestamp'>
                                <data:byline.label/>
                                <b:if cond='data:post.url'>
                                  <meta expr:content='data:post.url.canonical'/>
                                  <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'>
                                    <time class='published' expr:datetime='data:post.date.iso8601' expr:title='data:post.date.iso8601'>
                                      <data:post.date/>
                                    </time>
                                  </a>
                                </b:if>
                              </span>
                            </b:includable>
                              <b:includable id='sharingButton'>
                              <span expr:aria-label='data:platform.shareMessage' expr:class='&quot;sharing-platform-button sharing-element-&quot; + data:platform.key' expr:data-href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:data-url='data:originalUrl' expr:title='data:platform.shareMessage' role='menuitem' tabindex='-1'>
                                <b:include name='sharingPlatformIcon'/>
                                <span class='platform-sharing-text'><data:platform.name/></span>
                              </span>
                            </b:includable>
                              <b:includable id='sharingButtonContent'>
                              <div class='flat-icon-button ripple'>
                                <b:include name='shareIcon'/>
                              </div>
                            </b:includable>
                              <b:includable id='sharingButtons'>
                              <div class='sharing' expr:aria-owns='&quot;sharing-popup-&quot; + data:sharingId' expr:data-title='data:shareTitle'>
                                <button class='sharing-button touch-icon-button' expr:aria-controls='&quot;sharing-popup-&quot; + data:sharingId' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-button-&quot; + data:sharingId' role='button'>
                                  <b:include name='sharingButtonContent'/>
                                </button>
                                <b:include name='sharingButtonsMenu'/>
                              </div>
                            </b:includable>
                              <b:includable id='sharingButtonsMenu'>
                              <div class='share-buttons-container'>
                                <ul aria-hidden='true' class='share-buttons hidden' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-popup-&quot; + data:sharingId' role='menu'>
                                  <b:loop values='(data:platforms ?: data:blog.sharing.platforms) filter (p =&gt; p.key not in {&quot;blogThis&quot;})' var='platform'>
                                    <li>
                                      <b:include name='sharingButton'/>
                                    </li>
                                  </b:loop>
                                  <li aria-hidden='true' class='hidden'>
                                    <b:include name='otherSharingButton'/>
                                  </li>
                                </ul>
                              </div>
                            </b:includable>
                              <b:includable id='sharingPlatformIcon'>
                              <b:include data='{ iconClass: (&quot;touch-icon sharing-&quot; + data:platform.key) }' expr:name='data:platform.key + &quot;Icon&quot;'/>
                            </b:includable>
                              <b:includable id='snippetedPostByline'>
                              <b:with value='(data:widgets first (w =&gt; w.type == &quot;Blog&quot;)).allBylineItems' var='blogBylines'>
                                <div class='item-byline'>
                                  <b:with value='data:blogBylines first (i =&gt; i.name == &quot;author&quot;)' var='byline'>
                                    <b:include cond='data:byline and data:this.postDisplay.showAuthor' data='post' name='postAuthor'/>
                                  </b:with>
                                  <b:with value='data:blogBylines first (i =&gt; i.name == &quot;timestamp&quot;)' var='byline'>
                                    <b:include cond='data:byline and data:this.postDisplay.showDate' data='post' name='postTimestamp'/>
                                  </b:with>
                                </div>
                              </b:with>
                            </b:includable>
                              <b:includable id='snippetedPostContent'>
                              <div class='grid pcc'><div class='w-25 h25 tac lh-25px r2f'><b:eval expr='data:num'/></div></div>
                              <b:include cond='data:this.postDisplay.showFeaturedImage and data:post.featuredImage' name='snippetedPostThumbnail'/>
                              <b:include cond='data:this.postDisplay.showTitle' name='snippetedPostTitle'/>
                            </b:includable>
                              <b:includable id='snippetedPostThumbnail'>
                              <div class='item-thumbnail'>
                                <a expr:href='data:post.url'>
                                  <b:include data='{                         image: data:post.featuredImage,                         imageSizes: [72, 144],                         imageRatio: &quot;58:75&quot;,                         sourceSizes: &quot;80px&quot;                        }' name='responsiveImage'/>
                                </a>
                              </div>
                            </b:includable>
                              <b:includable id='snippetedPostTitle'>
                              <div>
                              <b:if cond='data:post.title != &quot;&quot;'>
                                <h3 class='post-title m-0 fs-15'><a expr:href='data:post.url'><data:post.title/></a></h3>
                              </b:if>
                                <b:include name='postLabels'/>
                                <b:include name='rbt'/>
                              </div>
                            </b:includable>
                              <b:includable id='snippetedPosts'>
                              <b:with value='data:posts filter (p =&gt; p.labels none (l =&gt; l.name == &quot;Chapter&quot;))' var='posts'>
                                <!-- Don't render the post that we're currently already looking at. -->
                                <b:loop index='i' values='data:posts filter (p =&gt; p.id != data:view.postId)' var='post'>
                                  <b:with value='data:i + 1' var='num'>
                                  <article class='p-y12x15 grid gtc-3c bb-1pxsf' role='article'>
                                    <b:include name='snippetedPostContent'/>
                                  </article>
                                    </b:with>
                                </b:loop>
                              
                              </b:with>
                            </b:includable>
                            </b:widget>
                            <b:widget id='PopularPosts5' locked='true' title='Tahun' type='PopularPosts' version='2' visible='true'>
                              <b:widget-settings>
                                <b:widget-setting name='numItemsToShow'>10</b:widget-setting>
                                <b:widget-setting name='showThumbnails'>true</b:widget-setting>
                                <b:widget-setting name='showSnippets'>true</b:widget-setting>
                                <b:widget-setting name='timeRange'>ALL_TIME</b:widget-setting>
                              </b:widget-settings>
                              <b:includable id='main' var='this'>

                                <b:include name='snippetedPosts'/>
                              
                            </b:includable>
                              <b:includable id='blogThisShare'>
                              <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=270,width=475\&quot;); return false;&quot;' var='onclick'>
                                <b:include name='platformShare'/>
                              </b:with>
                            </b:includable>
                              <b:includable id='bylineByName' var='byline'>
                              <b:switch var='data:byline.name'>
                                <b:case value='share'/>
                                <b:include cond='data:post.shareUrl' name='postShareButtons'/>
                                <b:case value='comments'/>
                                <b:include cond='data:post.allowComments' name='postCommentsLink'/>
                                <b:case value='location'/>
                                <b:include cond='data:post.location' name='postLocation'/>
                                <b:case value='timestamp'/>
                                <b:include cond='not data:view.isPage' name='postTimestamp'/>
                                <b:case value='author'/>
                                <b:include name='postAuthor'/>
                                <b:case value='labels'/>
                                <b:include cond='data:post.labels' name='postLabels'/>
                                <b:case value='icons'/>
                                <b:include cond='data:post.emailPostUrl' name='emailPostIcon'/>
                              </b:switch>
                            </b:includable>
                              <b:includable id='bylineRegion' var='regionItems'>
                              <b:loop values='data:regionItems' var='byline'>
                                <b:include data='byline' name='bylineByName'/>
                              </b:loop>
                            </b:includable>
                              <b:includable id='commentsLink'>
                              <a class='comment-link' expr:href='data:post.commentsUrl' expr:onclick='data:post.commentsUrlOnclick'>
                                <b:if cond='data:post.numberOfComments &gt; 0'>
                                  <b:message name='messages.numberOfComments'>
                                    <b:param expr:value='data:post.numberOfComments' name='numComments'/>
                                  </b:message>
                                  <b:else/>
                                  <data:messages.postAComment/>
                                </b:if>
                              </a>
                            </b:includable>
                              <b:includable id='commentsLinkIframe'>
                              <!-- G+ comments, no longer available. The includable is retained for backwards-compatibility. -->
                            </b:includable>
                              <b:includable id='emailPostIcon'>
                              <span class='byline post-icons'>
                                <!-- email post links -->
                                <span class='item-action'>
                                  <a expr:href='data:post.emailPostUrl' expr:title='data:messages.emailPost'>
                                    <b:include data='{ iconClass: &quot;touch-icon sharing-icon&quot; }' name='emailIcon'/>
                                  </a>
                                </span>
                              </span>
                            </b:includable>
                              <b:includable id='facebookShare'>
                              <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=430,width=640\&quot;); return false;&quot;' var='onclick'>
                                <b:include name='platformShare'/>
                              </b:with>
                            </b:includable>
                              <b:includable id='footerBylines'>
                              <b:if cond='data:widgets.Blog.first.footerBylines'>
                                <b:loop index='i' values='data:widgets.Blog.first.footerBylines' var='region'>
                                  <b:if cond='not data:region.items.empty'>
                                    <div expr:class='&quot;post-footer-line post-footer-line-&quot; + (data:i + 1)'>
                                      <b:with value='&quot;footer-&quot; + (data:i + 1)' var='regionName'>
                                        <b:include data='region.items' name='bylineRegion'/>
                                      </b:with>
                                    </div>
                                  </b:if>
                                </b:loop>
                              </b:if>
                            </b:includable>
                              <b:includable id='googlePlusShare'>
                            </b:includable>
                              <b:includable id='headerByline'>
                              <b:if cond='data:widgets.Blog.first.headerByline'>
                                <div class='post-header'>
                                  <div class='post-header-line-1'>
                                    <b:with value='&quot;header-1&quot;' var='regionName'>
                                      <b:include data='data:widgets.Blog.first.headerByline.items' name='bylineRegion'/>
                                    </b:with>
                                  </div>
                                </div>
                              </b:if>
                            </b:includable>
                              <b:includable id='linkShare'>
                              <b:with value='&quot;window.prompt(\&quot;Copy to clipboard: Ctrl+C, Enter\&quot;, \&quot;&quot; + data:originalUrl + &quot;\&quot;); return false;&quot;' var='onclick'>
                                <b:include name='platformShare'/>
                              </b:with>
                            </b:includable>
                              <b:includable id='otherSharingButton'>
                              <span class='sharing-platform-button sharing-element-other' expr:aria-label='data:messages.shareToOtherApps.escaped' expr:data-url='data:originalUrl' expr:title='data:messages.shareToOtherApps.escaped' role='menuitem' tabindex='-1'>
                                <b:with value='{key: &quot;sharingOther&quot;}' var='platform'>
                                  <b:include name='sharingPlatformIcon'/>
                                </b:with>
                                <span class='platform-sharing-text'><data:messages.shareOtherApps.escaped/></span>
                              </span>
                            </b:includable>
                              <b:includable id='platformShare'>
                              <a expr:class='&quot;goog-inline-block sharing-&quot; + data:platform.key' expr:data-url='data:originalUrl' expr:href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:onclick='data:onclick ? data:onclick : &quot;&quot;' expr:title='data:platform.shareMessage' target='_blank'>
                                <span class='share-button-link-text'>
                                  <data:platform.shareMessage/>
                                </span>
                              </a>
                            </b:includable>
                              <b:includable id='postAuthor'>
                              <span class='byline post-author vcard'>
                                <span class='post-author-label'>
                                  <data:byline.label/>
                                </span>
                                <span class='fn'>
                                  <b:if cond='data:post.author.profileUrl'>
                                    <meta expr:content='data:post.author.profileUrl'/>
                                    <a class='g-profile' expr:href='data:post.author.profileUrl' rel='author' title='author profile'>
                                      <span><data:post.author.name/></span>
                                    </a>
                                    <b:else/>
                                    <span><data:post.author.name/></span>
                                  </b:if>
                                </span>
                              </span>
                            </b:includable>
                              <b:includable id='postCommentsLink'>
                              <span class='byline post-comment-link container'>
                                <b:include cond='data:post.commentSource != 1' name='commentsLink'/>
                              </span>
                            </b:includable>
                              <b:includable id='postJumpLink' var='post'>
                              <div class='jump-link flat-button'>
                                <a expr:href='data:post.url fragment &quot;more&quot;' expr:title='data:post.title'>
                                  <b:eval expr='data:blog.jumpLinkMessage'/>
                                </a>
                              </div>
                            </b:includable>
                              <b:includable id='postLabels'>
                              <span class='span-spc fs-13'>
                                <b>Genres</b>
                                <b:loop index='i' values='data:post.labels' var='label'>
                                  <b:if cond='data:label.name in data:Genre or data:label.name in data:Genre2 or data:label.name in data:Demographic'>
                                  <a expr:href='data:label.url' rel='tag'>
                                    <data:label.name/>,
                                  </a>
                                  </b:if>
                                </b:loop>
                              </span>
                            </b:includable>
                              <b:includable id='postLocation'>
                              <span class='byline post-location'>
                                <data:byline.label/>
                                <a expr:href='data:post.location.mapsUrl' target='_blank'><data:post.location.name/></a>
                              </span>
                            </b:includable>
                              <b:includable id='postReactions'>
                              <!-- Reaction feature no longer available. The includable is retained for backwards-compatibility. -->
                            </b:includable>
                              <b:includable id='postShareButtons'>
                              <div class='byline post-share-buttons goog-inline-block'>
                                <b:with value='data:sharingId ?: ((data:widget.instanceId ?: &quot;sharing&quot;) + &quot;-&quot; + (data:regionName ?: &quot;byline&quot;) + &quot;-&quot; + data:post.id)' var='sharingId'>
                                  <!-- Note: 'sharingButtons' includable is from the default Sharing widget markup. -->
                                  <b:include data='{                                                sharingId: data:sharingId,                                                originalUrl: data:post.url,                                                platforms: data:this.sharing.platforms,                                                shareUrl: data:post.shareUrl,                                                shareTitle: data:post.title,                                              }' name='sharingButtons'/>
                                </b:with>
                              </div>
                            </b:includable>
                              <b:includable id='postTimestamp'>
                              <span class='byline post-timestamp'>
                                <data:byline.label/>
                                <b:if cond='data:post.url'>
                                  <meta expr:content='data:post.url.canonical'/>
                                  <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'>
                                    <time class='published' expr:datetime='data:post.date.iso8601' expr:title='data:post.date.iso8601'>
                                      <data:post.date/>
                                    </time>
                                  </a>
                                </b:if>
                              </span>
                            </b:includable>
                              <b:includable id='sharingButton'>
                              <span expr:aria-label='data:platform.shareMessage' expr:class='&quot;sharing-platform-button sharing-element-&quot; + data:platform.key' expr:data-href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:data-url='data:originalUrl' expr:title='data:platform.shareMessage' role='menuitem' tabindex='-1'>
                                <b:include name='sharingPlatformIcon'/>
                                <span class='platform-sharing-text'><data:platform.name/></span>
                              </span>
                            </b:includable>
                              <b:includable id='sharingButtonContent'>
                              <div class='flat-icon-button ripple'>
                                <b:include name='shareIcon'/>
                              </div>
                            </b:includable>
                              <b:includable id='sharingButtons'>
                              <div class='sharing' expr:aria-owns='&quot;sharing-popup-&quot; + data:sharingId' expr:data-title='data:shareTitle'>
                                <button class='sharing-button touch-icon-button' expr:aria-controls='&quot;sharing-popup-&quot; + data:sharingId' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-button-&quot; + data:sharingId' role='button'>
                                  <b:include name='sharingButtonContent'/>
                                </button>
                                <b:include name='sharingButtonsMenu'/>
                              </div>
                            </b:includable>
                              <b:includable id='sharingButtonsMenu'>
                              <div class='share-buttons-container'>
                                <ul aria-hidden='true' class='share-buttons hidden' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-popup-&quot; + data:sharingId' role='menu'>
                                  <b:loop values='(data:platforms ?: data:blog.sharing.platforms) filter (p =&gt; p.key not in {&quot;blogThis&quot;})' var='platform'>
                                    <li>
                                      <b:include name='sharingButton'/>
                                    </li>
                                  </b:loop>
                                  <li aria-hidden='true' class='hidden'>
                                    <b:include name='otherSharingButton'/>
                                  </li>
                                </ul>
                              </div>
                            </b:includable>
                              <b:includable id='sharingPlatformIcon'>
                              <b:include data='{ iconClass: (&quot;touch-icon sharing-&quot; + data:platform.key) }' expr:name='data:platform.key + &quot;Icon&quot;'/>
                            </b:includable>
                              <b:includable id='snippetedPostByline'>
                              <b:with value='(data:widgets first (w =&gt; w.type == &quot;Blog&quot;)).allBylineItems' var='blogBylines'>
                                <div class='item-byline'>
                                  <b:with value='data:blogBylines first (i =&gt; i.name == &quot;author&quot;)' var='byline'>
                                    <b:include cond='data:byline and data:this.postDisplay.showAuthor' data='post' name='postAuthor'/>
                                  </b:with>
                                  <b:with value='data:blogBylines first (i =&gt; i.name == &quot;timestamp&quot;)' var='byline'>
                                    <b:include cond='data:byline and data:this.postDisplay.showDate' data='post' name='postTimestamp'/>
                                  </b:with>
                                </div>
                              </b:with>
                            </b:includable>
                              <b:includable id='snippetedPostContent'>
                              <div class='grid pcc'><div class='w-25 h25 tac lh-25px r2f'><b:eval expr='data:num'/></div></div>
                              <b:include cond='data:this.postDisplay.showFeaturedImage and data:post.featuredImage' name='snippetedPostThumbnail'/>
                              <b:include cond='data:this.postDisplay.showTitle' name='snippetedPostTitle'/>
                            </b:includable>
                              <b:includable id='snippetedPostThumbnail'>
                              <div class='item-thumbnail'>
                                <a expr:href='data:post.url'>
                                  <b:include data='{                         image: data:post.featuredImage,                         imageSizes: [72, 144],                         imageRatio: &quot;58:75&quot;,                         sourceSizes: &quot;80px&quot;                        }' name='responsiveImage'/>
                                </a>
                              </div>
                            </b:includable>
                              <b:includable id='snippetedPostTitle'>
                              <div>
                              <b:if cond='data:post.title != &quot;&quot;'>
                                <h3 class='post-title m-0 fs-15'><a expr:href='data:post.url'><data:post.title/></a></h3>
                              </b:if>
                                <b:include name='postLabels'/>
                                <b:include name='rbt'/>
                              </div>
                            </b:includable>
                              <b:includable id='snippetedPosts'>
                              <b:with value='data:posts filter (p =&gt; p.labels none (l =&gt; l.name == &quot;Chapter&quot;))' var='posts'>
                                <!-- Don't render the post that we're currently already looking at. -->
                                <b:loop index='i' values='data:posts filter (p =&gt; p.id != data:view.postId)' var='post'>
                                  <b:with value='data:i + 1' var='num'>
                                  <article class='p-y12x15 grid gtc-3c bb-1pxsf' role='article'>
                                    <b:include name='snippetedPostContent'/>
                                  </article>
                                    </b:with>
                                </b:loop>
                              
                              </b:with>
                            </b:includable>
                            </b:widget>
                          </b:section>
                            </b:tag>
                          <b:section class='grid gg-20' cond='data:view.isMultipleItems and !data:view.isLabelSearch' id='other' showaddelement='true'>
                            <b:widget id='HTML2' locked='true' title='Donation' type='HTML' version='2' visible='false'>
                              <b:widget-settings>
                                <b:widget-setting name='content'><![CDATA[<a href="#" target="_blank" rel="noopener"><div style="padding: 10px;"><img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhbXzT_YUP8J88nSfO330yDuk14rxXDVKOo_OlgieKyoQpKDK9gtiIrA4YfkL98jNmWB_mAcHL0yLLKHxdXZAGzYDOihrRfClLbx4G-F4hhWZHu7HRxFvxCYCNw1_IvFMhsToh514NppBQzyrCl5uWmJVjB8yhRE5adrYJAdWwW_DtdNMxhoe3iXTUDjA/s800/navbar-logo-lite-beta.png" alt="" /></div></a>]]></b:widget-setting>
                              </b:widget-settings>
                              <b:includable id='main'>
                              <h3 class='title flex aic'>
    <svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg'><path d='M21.909 10.928H24v2.02h-2.091zm-3.635 0h2.091v2.02h-2.091zm-6.022.001l-.657 2.215l-3.772-8.343l-1.954 6.17H0v2.02h7.346l.81-2.551l3.834 8.486l1.76-5.978h2.973v-2.02z' fill='currentColor'/></svg>
<data:title/>
</h3>
                              <div class='widget-content'>
                                <data:content/>
                              </div>
                            </b:includable>
                            </b:widget>
                            <b:widget id='HTML18' locked='false' title='Join Discord' type='HTML' version='2' visible='false'>
                              <b:widget-settings>
                                <b:widget-setting name='content'><![CDATA[<a href="https://telegram.me/protemplates"><img class="image " src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgNdigejeuvgCwYcm5N7IMSQAVG37kSUwS8l11ksU10s0aNljMWJLXmRgI8leCObl82axiEsCnPocPGR9hZnQsTgXBrd_eAnRh-Al5EQdVFVCz4JrYH2otTmJMdVS80fRhTSDsLjTwGmAJng-jbeXPyuMmArao0PNsSWjRXSGiCG0db0NXlNQmO9y-HDg/s800/discord.png" alt="Discord App" width="800" height="272" /></a>]]></b:widget-setting>
                              </b:widget-settings>
                              <b:includable id='main'>
  <h3 class='title flex aic'>
    <svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 24 24' width='1em' xmlns='http://www.w3.org/2000/svg'><path d='M19.27 5.33C17.94 4.71 16.5 4.26 15 4a.09.09 0 0 0-.07.03c-.18.33-.39.76-.53 1.09a16.09 16.09 0 0 0-4.8 0c-.14-.34-.35-.76-.54-1.09c-.01-.02-.04-.03-.07-.03c-1.5.26-2.93.71-4.27 1.33c-.01 0-.02.01-.03.02c-2.72 4.07-3.47 8.03-3.1 11.95c0 .02.01.04.03.05c1.8 1.32 3.53 2.12 5.24 2.65c.03.01.06 0 .07-.02c.4-.55.76-1.13 1.07-1.74c.02-.04 0-.08-.04-.09c-.57-.22-1.11-.48-1.64-.78c-.04-.02-.04-.08-.01-.11c.11-.08.22-.17.33-.25c.02-.02.05-.02.07-.01c3.44 1.57 7.15 1.57 10.55 0c.02-.01.05-.01.07.01c.11.09.22.17.33.26c.04.03.04.09-.01.11c-.52.31-1.07.56-1.64.78c-.04.01-.05.06-.04.09c.32.61.68 1.19 1.07 1.74c.03.01.06.02.09.01c1.72-.53 3.45-1.33 5.25-2.65c.02-.01.03-.03.03-.05c.44-4.53-.73-8.46-3.1-11.95c-.01-.01-.02-.02-.04-.02zM8.52 14.91c-1.03 0-1.89-.95-1.89-2.12s.84-2.12 1.89-2.12c1.06 0 1.9.96 1.89 2.12c0 1.17-.84 2.12-1.89 2.12zm6.97 0c-1.03 0-1.89-.95-1.89-2.12s.84-2.12 1.89-2.12c1.06 0 1.9.96 1.89 2.12c0 1.17-.83 2.12-1.89 2.12z' fill='currentColor'/></svg>
<data:title/>
</h3>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                            </b:widget>
                            <b:widget cond='data:view.isMultipleItems' id='HTML8' locked='true' title='Ads' type='HTML' version='2' visible='false'>
                              <b:widget-settings>
                                <b:widget-setting name='content'/>
                              </b:widget-settings>
                              <b:includable id='main'>
                              <b:class name='ads'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                            </b:widget>
                            <b:widget cond='data:view.isHomepage' id='PopularPosts1' locked='true' title='Popular Post' type='PopularPosts' version='2' visible='false'>
                              <b:widget-settings>
                                <b:widget-setting name='numItemsToShow'>10</b:widget-setting>
                                <b:widget-setting name='showThumbnails'>true</b:widget-setting>
                                <b:widget-setting name='showSnippets'>true</b:widget-setting>
                                <b:widget-setting name='timeRange'>LAST_YEAR</b:widget-setting>
                              </b:widget-settings>
                              <b:includable id='main' var='this'>
                              <article>
                                <div class='flex aic jcsb p-13'>
                                  <h3 class='m-0 c-theme fs-15 flex aic'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 432 488' width='0.89em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><path d='M364 304q2-12 2-20q1-59-24.5-90.5T270 135q10 55-18.5 86.5T179 241q24-39 29-69t-3.5-46.5t-17.5-36T172.5 52T178 2q-44 31-80 104.5T62 242q2 37 7 62q-68 28-68 67q0 37 63 64t152 27t152-27t63-64q0-39-67-67zM134 194q-11 52 12 89.5t56 37.5q63 0 88-100q36 27 39 72q3 49-37 83v1q-12 8-19 12q-1 1-2 1l-8 4l-2 1q-10 4-23 7q-3 0-4 1q-2 0-5 .5t-4 .5q-3 0-4 1h-26q-1 0-4-.5t-4-.5h-1q-8-2-10-2l-1-1l-9-3h-1q-30-12-47.5-39.5T101 293l-1 1q2-48 34-100z' fill='currentColor'/></svg><data:title/></h3>
                                  <a class='bg-main ttu p-3y6x fs-9 r2 c-fff' href=''>View All</a>
                                </div>

                                <b:include name='snippetedPosts'/>
                              </article>
                            </b:includable>
                              <b:includable id='blogThisShare'>
                              <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=270,width=475\&quot;); return false;&quot;' var='onclick'>
                                <b:include name='platformShare'/>
                              </b:with>
                            </b:includable>
                              <b:includable id='bylineByName' var='byline'>
                              <b:switch var='data:byline.name'>
                                <b:case value='share'/>
                                <b:include cond='data:post.shareUrl' name='postShareButtons'/>
                                <b:case value='comments'/>
                                <b:include cond='data:post.allowComments' name='postCommentsLink'/>
                                <b:case value='location'/>
                                <b:include cond='data:post.location' name='postLocation'/>
                                <b:case value='timestamp'/>
                                <b:include cond='not data:view.isPage' name='postTimestamp'/>
                                <b:case value='author'/>
                                <b:include name='postAuthor'/>
                                <b:case value='labels'/>
                                <b:include cond='data:post.labels' name='postLabels'/>
                                <b:case value='icons'/>
                                <b:include cond='data:post.emailPostUrl' name='emailPostIcon'/>
                                <b:case value='reactions'/>
                                <b:include cond='data:post.reactionsUrl' name='postReactions'/>
                              </b:switch>
                            </b:includable>
                              <b:includable id='bylineRegion' var='regionItems'>
                              <b:loop values='data:regionItems' var='byline'>
                                <b:include data='byline' name='bylineByName'/>
                              </b:loop>
                            </b:includable>
                              <b:includable id='commentsLink'>
                              <a class='comment-link' expr:href='data:post.commentsUrl' expr:onclick='data:post.commentsUrlOnclick'>
                                <b:if cond='data:post.numberOfComments &gt; 0'>
                                  <b:message name='messages.numberOfComments'>
                                    <b:param expr:value='data:post.numberOfComments' name='numComments'/>
                                  </b:message>
                                  <b:else/>
                                  <data:messages.postAComment/>
                                </b:if>
                              </a>
                            </b:includable>
                              <b:includable id='commentsLinkIframe'>
                              <!-- G+ comments, no longer available. The includable is retained for backwards-compatibility. -->
                            </b:includable>
                              <b:includable id='emailPostIcon'>
                              <span class='byline post-icons'>
                                <!-- email post links -->
                                <span class='item-action'>
                                  <a expr:href='data:post.emailPostUrl' expr:title='data:messages.emailPost'>
                                    <b:include data='{ iconClass: &quot;touch-icon sharing-icon&quot; }' name='emailIcon'/>
                                  </a>
                                </span>
                              </span>
                            </b:includable>
                              <b:includable id='facebookShare'>
                              <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=430,width=640\&quot;); return false;&quot;' var='onclick'>
                                <b:include name='platformShare'/>
                              </b:with>
                            </b:includable>
                              <b:includable id='footerBylines'>
                              <b:if cond='data:widgets.Blog.first.footerBylines'>
                                <b:loop index='i' values='data:widgets.Blog.first.footerBylines' var='region'>
                                  <b:if cond='not data:region.items.empty'>
                                    <div expr:class='&quot;post-footer-line post-footer-line-&quot; + (data:i + 1)'>
                                      <b:with value='&quot;footer-&quot; + (data:i + 1)' var='regionName'>
                                        <b:include data='region.items' name='bylineRegion'/>
                                      </b:with>
                                    </div>
                                  </b:if>
                                </b:loop>
                              </b:if>
                            </b:includable>
                              <b:includable id='googlePlusShare'>
                              <div class='goog-inline-block google-plus-share-container'>
                                <g:plusone annotation='inline' expr:href='data:originalUrl.canonical.http' size='medium' source='blogger:blog:plusone'/>
                              </div>
                            </b:includable>
                              <b:includable id='headerByline'>
                              <b:if cond='data:widgets.Blog.first.headerByline'>
                                <div class='post-header'>
                                  <div class='post-header-line-1'>
                                    <b:with value='&quot;header-1&quot;' var='regionName'>
                                      <b:include data='data:widgets.Blog.first.headerByline.items' name='bylineRegion'/>
                                    </b:with>
                                  </div>
                                </div>
                              </b:if>
                            </b:includable>
                              <b:includable id='linkShare'>
                              <b:with value='&quot;window.prompt(\&quot;Copy to clipboard: Ctrl+C, Enter\&quot;, \&quot;&quot; + data:originalUrl + &quot;\&quot;); return false;&quot;' var='onclick'>
                                <b:include name='platformShare'/>
                              </b:with>
                            </b:includable>
                              <b:includable id='otherSharingButton'>
                              <span class='sharing-platform-button sharing-element-other' expr:aria-label='data:messages.shareToOtherApps.escaped' expr:data-url='data:originalUrl' expr:title='data:messages.shareToOtherApps.escaped' role='menuitem' tabindex='-1'>
                                <b:with value='{key: &quot;sharingOther&quot;}' var='platform'>
                                  <b:include name='sharingPlatformIcon'/>
                                </b:with>
                                <span class='platform-sharing-text'><data:messages.shareOtherApps.escaped/></span>
                              </span>
                            </b:includable>
                              <b:includable id='platformShare'>
                              <a expr:class='&quot;goog-inline-block sharing-&quot; + data:platform.key' expr:data-url='data:originalUrl' expr:href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:onclick='data:onclick ? data:onclick : &quot;&quot;' expr:title='data:platform.shareMessage' target='_blank'>
                                <span class='share-button-link-text'>
                                  <data:platform.shareMessage/>
                                </span>
                              </a>
                            </b:includable>
                              <b:includable id='postAuthor'>
                              <span class='byline post-author vcard'>
                                <span class='post-author-label'>
                                  <data:byline.label/>
                                </span>
                                <span class='fn'>
                                  <b:if cond='data:post.author.profileUrl'>
                                    <meta expr:content='data:post.author.profileUrl'/>
                                    <a class='g-profile' expr:href='data:post.author.profileUrl' rel='author' title='author profile'>
                                      <span><data:post.author.name/></span>
                                    </a>
                                    <b:else/>
                                    <span><data:post.author.name/></span>
                                  </b:if>
                                </span>
                              </span>
                            </b:includable>
                              <b:includable id='postCommentsLink'>
                              <span class='byline post-comment-link container'>
                                <b:include cond='data:post.commentSource != 1' name='commentsLink'/>
                              </span>
                            </b:includable>
                              <b:includable id='postJumpLink' var='post'>
                              <div class='jump-link flat-button'>
                                <a expr:href='data:post.url fragment &quot;more&quot;' expr:title='data:post.title'>
                                  <b:eval expr='data:blog.jumpLinkMessage'/>
                                </a>
                              </div>
                            </b:includable>
                              <b:includable id='postLabels'>
                              <span class='byline post-labels'>
                                <span class='byline-label'>Genre: </span>
                                <b:loop index='i' values='data:post.labels' var='label'>
                                  <a expr:href='data:label.url' rel='tag'>
                                    <data:label.name/>
                                  </a>,
                                </b:loop>
                              </span>
                            </b:includable>
                              <b:includable id='postLocation'>
                              <span class='byline post-location'>
                                <data:byline.label/>
                                <a expr:href='data:post.location.mapsUrl' target='_blank'><data:post.location.name/></a>
                              </span>
                            </b:includable>
                              <b:includable id='postReactions'>

                              <iframe allowtransparency='true' class='reactions-iframe' expr:src='data:post.reactionsUrl' frameborder='0' name='reactions' scrolling='no'/>

                            </b:includable>
                              <b:includable id='postShareButtons'>
                              <div class='byline post-share-buttons goog-inline-block'>
                                <b:with value='data:sharingId ?: ((data:widget.instanceId ?: &quot;sharing&quot;) + &quot;-&quot; + (data:regionName ?: &quot;byline&quot;) + &quot;-&quot; + data:post.id)' var='sharingId'>
                                  <!-- Note: 'sharingButtons' includable is from the default Sharing widget markup. -->
                                  <b:include data='{                                                sharingId: data:sharingId,                                                originalUrl: data:post.url,                                                platforms: data:this.sharing.platforms,                                                shareUrl: data:post.shareUrl,                                                shareTitle: data:post.title,                                              }' name='sharingButtons'/>
                                </b:with>
                              </div>
                            </b:includable>
                              <b:includable id='postTimestamp'>
                              <span class='byline post-timestamp'>
                                <data:byline.label/>
                                <b:if cond='data:post.url'>
                                  <meta expr:content='data:post.url.canonical'/>
                                  <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'>
                                    <time class='published' expr:datetime='data:post.date.iso8601' expr:title='data:post.date.iso8601'>
                                      <data:post.date/>
                                    </time>
                                  </a>
                                </b:if>
                              </span>
                            </b:includable>
                              <b:includable id='sharingButton'>
                              <span expr:aria-label='data:platform.shareMessage' expr:class='&quot;sharing-platform-button sharing-element-&quot; + data:platform.key' expr:data-href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:data-url='data:originalUrl' expr:title='data:platform.shareMessage' role='menuitem' tabindex='-1'>
                                <b:include name='sharingPlatformIcon'/>
                                <span class='platform-sharing-text'><data:platform.name/></span>
                              </span>
                            </b:includable>
                              <b:includable id='sharingButtonContent'>
                              <div class='flat-icon-button ripple'>
                                <b:include name='shareIcon'/>
                              </div>
                            </b:includable>
                              <b:includable id='sharingButtons'>
                              <div class='sharing' expr:aria-owns='&quot;sharing-popup-&quot; + data:sharingId' expr:data-title='data:shareTitle'>
                                <button class='sharing-button touch-icon-button' expr:aria-controls='&quot;sharing-popup-&quot; + data:sharingId' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-button-&quot; + data:sharingId' role='button'>
                                  <b:include name='sharingButtonContent'/>
                                </button>
                                <b:include name='sharingButtonsMenu'/>
                              </div>
                            </b:includable>
                              <b:includable id='sharingButtonsMenu'>
                              <div class='share-buttons-container'>
                                <ul aria-hidden='true' class='share-buttons hidden' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-popup-&quot; + data:sharingId' role='menu'>
                                  <b:loop values='(data:platforms ?: data:blog.sharing.platforms) filter (p =&gt; p.key not in {&quot;blogThis&quot;})' var='platform'>
                                    <li>
                                      <b:include name='sharingButton'/>
                                    </li>
                                  </b:loop>
                                  <li aria-hidden='true' class='hidden'>
                                    <b:include name='otherSharingButton'/>
                                  </li>
                                </ul>
                              </div>
                            </b:includable>
                              <b:includable id='sharingPlatformIcon'>
                              <b:include data='{ iconClass: (&quot;touch-icon sharing-&quot; + data:platform.key) }' expr:name='data:platform.key + &quot;Icon&quot;'/>
                            </b:includable>
                              <b:includable id='snippetedPostByline'>
                              <b:with value='(data:widgets first (w =&gt; w.type == &quot;Blog&quot;)).allBylineItems' var='blogBylines'>
                                <div class='item-byline'>
                                  <b:with value='data:blogBylines first (i =&gt; i.name == &quot;author&quot;)' var='byline'>
                                    <b:include cond='data:byline and data:this.postDisplay.showAuthor' data='post' name='postAuthor'/>
                                  </b:with>
                                  <b:with value='data:blogBylines first (i =&gt; i.name == &quot;timestamp&quot;)' var='byline'>
                                    <b:include cond='data:byline and data:this.postDisplay.showDate' data='post' name='postTimestamp'/>
                                  </b:with>
                                </div>
                              </b:with>
                            </b:includable>
                              <b:includable id='snippetedPostContent'>
                              <div class='post-content'>

                                <b:include cond='data:this.postDisplay.showDate or data:this.postDisplay.showAuthor' name='snippetedPostByline'/>

                                <b:include cond='data:this.postDisplay.showFeaturedImage and data:post.featuredImage' name='snippetedPostThumbnail'/>
                              </div>
                            </b:includable>
                              <b:includable id='snippetedPostThumbnail'>
                              <div class='item-thumbnail relative overlay'>
                                <a class='block ov-img b-img' expr:href='data:post.url'>
                                  <b:include data='{                         image: data:post.featuredImage,                         imageSizes: [172, 244],                         imageRatio: &quot;1:2&quot;,                         sourceSizes: &quot;272px&quot;                        }' name='responsiveImage'/>
                                  <span class='counter'/>
                                </a>
                                <b:include cond='data:this.postDisplay.showTitle' name='snippetedPostTitle'/>
                              </div>
                            </b:includable>
                              <b:includable id='snippetedPostTitle'>
                              <b:if cond='data:post.title != &quot;&quot;'>
                                <div class='ov-title'>
                                  <h3 class='post-title'><a expr:href='data:post.url'><data:post.title/></a></h3>
                                  <div class='toe oh c-fff'>
                                    <b:include name='postLabels'/>
                                    <div class='date mt-5'><data:post.date/></div>
                                  </div>
                                </div>
                              </b:if>
                            </b:includable>
                              <b:includable id='snippetedPosts'>
                              <b:with value='data:posts filter (p =&gt; p.labels none (l =&gt; l.name == &quot;Chapter&quot;))' var='posts'>
                                <div class='grid col' role='feed'>
                                  <!-- Don't render the post that we're currently already looking at. -->
                                  <b:loop values='data:posts filter (p =&gt; p.id != data:view.postId)' var='post'>
                                    <section class='post' role='article'>
                                      <b:include name='snippetedPostContent'/>
                                    </section>
                                  </b:loop>
                                </div>
                              </b:with>
                            </b:includable>
                            </b:widget>
                            <b:widget id='HTML10' locked='false' title='Reading History' type='HTML' version='2' visible='true'>
                              <b:widget-settings>
                                <b:widget-setting name='content'><![CDATA[<script>history_('#HTML10','#HTML10 .widget-history')</script>]]></b:widget-setting>
                              </b:widget-settings>
                              <b:includable id='main'>
  <h3 class='title flex aic'>
    <svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 28 28' width='1em' xmlns='http://www.w3.org/2000/svg'><path d='M12 21q-3.45 0-6.012-2.287T3.05 13H5.1q.35 2.6 2.313 4.3T12 19q2.925 0 4.963-2.037T19 12q0-2.925-2.037-4.962T12 5q-1.725 0-3.225.8T6.25 8H9v2H3V4h2v2.35q1.275-1.6 3.113-2.475T12 3q1.875 0 3.513.713t2.85 1.924q1.212 1.213 1.925 2.85T21 12q0 1.875-.712 3.513t-1.925 2.85q-1.213 1.212-2.85 1.925T12 21Zm2.8-4.8L11 12.4V7h2v4.6l3.2 3.2l-1.4 1.4Z' fill='currentColor'/></svg>
<data:title/>
</h3>
  <ul class='widget-history m-0 pl-0 lsn'>
    <data:content/>
  </ul>
</b:includable>
                            </b:widget>
                            <b:widget id='HTML4' locked='false' title='Random Manga' type='HTML' version='2' visible='false'>
                              <b:widget-settings>
                                <b:widget-setting name='content'>&lt;style&gt;
                                ul#random-posts {
                                list-style-type: none;
                                padding: 0px;
                                display: grid;
                                grid-template-columns: repeat(3, 32%);
                                gap: 7px;
                                margin: 0;
                                }
                                #random-posts img {
                                width: 100%;
                                height: 100%;
                                object-fit: cover;
                                }
                                #random-posts img:hover{opacity: 0.6;}
                                ul#random-posts {list-style-type: none;padding: 0px;}
                                #random-posts a {font-size: 12px;text-transform:uppercase; padding: 0px auto 5px;}
                                #random-posts a:hover {text-decoration: none;}
                                .rp-snippet {font-size: 11px;background: none; padding: 5px; margin-right: 8px;}
                                #random-posts span {}

                                &lt;/style&gt;
                                &lt;ul id=&#39;random-posts&#39;&gt;
                                &lt;script type=&#39;text/javaScript&#39;&gt;
                                var rdp_numposts=6;
                                var rdp_snippet_length=0;
                                var rdp_info=&#39;no&#39;;
                                var rdp_comment=&#39;comment&#39;;
                                var rdp_disable=&#39;Comments Disabled&#39;;
                                var rdp_current=[];var rdp_total_posts=0;var rdp_current=new Array(rdp_numposts);function totalposts(json){rdp_total_posts=json.feed.openSearch$totalResults.$t}document.write(&#39;&lt;script type=\&quot;text/javascript\&quot; src=\&quot;/feeds/posts/default/-/Series?alt=json-in-script&amp;max-results=0&amp;callback=totalposts\&quot;&gt;&lt;\/script&gt;&#39;);function getvalue(){for(var i=0;i&lt;rdp_numposts;i++){var found=false;var rndValue=get_random();for(var j=0;j&lt;rdp_current.length;j++){if(rdp_current[j]==rndValue){found=true;break}};if(found){i--}else{rdp_current[i]=rndValue}}};function get_random(){var ranNum=1+Math.round(Math.random()*(rdp_total_posts-1));return ranNum};
                                &lt;/script&gt;
                                &lt;script type=&#39;text/javaScript&#39;&gt; 
                                function random_posts(json){for(var i=0;i&lt;rdp_numposts;i++){var entry=json.feed.entry[i];var rdp_posttitle=entry.title.$t;if(&#39;content&#39;in entry){var rdp_get_snippet=entry.content.$t}else{if(&#39;summary&#39;in entry){var rdp_get_snippet=entry.summary.$t}else{var rdp_get_snippet=&quot;&quot;;}};rdp_get_snippet=rdp_get_snippet.replace(/&lt;[^&gt;]*&gt;/g,&quot;&quot;);if(rdp_get_snippet.length&lt;rdp_snippet_length){var rdp_snippet=rdp_get_snippet}else{rdp_get_snippet=rdp_get_snippet.substring(0,rdp_snippet_length);var space=rdp_get_snippet.lastIndexOf(&quot; &quot;);rdp_snippet=rdp_get_snippet.substring(0,space)+&quot;&amp;#133;&quot;;};for(var j=0;j&lt;entry.link.length;j++){if(&#39;thr$total&#39;in entry){var rdp_commentsNum=entry.thr$total.$t+&#39; &#39;+rdp_comment}else{rdp_commentsNum=rdp_disable};if(entry.link[j].rel==&#39;alternate&#39;){var rdp_posturl=entry.link[j].href;var rdp_postdate=entry.published.$t;if(&#39;media$thumbnail&#39;in entry){var rdp_thumb=entry.media$thumbnail.url.replace(/\/s72\-c\//,&#39;/s200/&#39;)}else{rdp_thumb=&quot;http://1.bp.blogspot.com/-PPTJQCe-atQ/U4ca2QTr_5I/AAAAAAAAEEc/TRrKNK1fqQY/s1600/no-image-available.jpg&quot;}}};document.write(&#39;&lt;li&gt;&#39;);document.write(&#39;&lt;a href=&quot;&#39;+rdp_posturl+&#39;&quot; rel=&quot;nofollow&quot;&gt;&lt;img alt=&quot;&#39;+rdp_posttitle+&#39;&quot; loading=&quot;lazy&quot; src=&quot;&#39;+rdp_thumb+&#39;&quot;/&gt;&lt;/a&gt;&#39;);document.write(&#39;&lt;div class=&quot;hidden&quot;&gt;&lt;a href=&quot;&#39;+rdp_posturl+&#39;&quot; rel=&quot;nofollow&quot; title=&quot;&#39;+rdp_snippet+&#39;&quot;&gt;&#39;+rdp_posttitle+&#39;&lt;/a&gt;&lt;/div&gt;&#39;);if(rdp_info==&#39;yes&#39;){document.write(&#39;&lt;span&gt;&lt;div  class=&quot;rp-info&quot;&gt;&#39;+rdp_postdate.substring(8,10)+&#39;/&#39;+rdp_postdate.substring(5,7)+&#39;/&#39;+rdp_postdate.substring(0,4)+&#39; - &#39;+rdp_commentsNum)+&#39;&lt;/div&gt;&lt;/span&gt;&#39;};document.write(&#39;&lt;div class=&quot;hidden&quot;&gt;&#39;+rdp_snippet+&#39;&lt;/div&gt;&lt;/li&gt;&#39;)}};getvalue();for(var i=0;i&lt;rdp_numposts;i++){document.write(&#39;&lt;script type=\&quot;text/javascript\&quot; src=\&quot;/feeds/posts/default/-/Series?alt=json-in-script&amp;start-index=&#39;+rdp_current[i]+&#39;&amp;max-results=1&amp;callback=random_posts\&quot;&gt;&lt;\/script&gt;&#39;)};
                                &lt;/script&gt;
                                &lt;/ul&gt;</b:widget-setting>
                              </b:widget-settings>
                              <b:includable id='main'>
                              <b:include name='widget-title'/>
                              <div class='widget-content'>
                                <data:content/>
                              </div>
                            </b:includable>
                            </b:widget>
                            <b:widget id='Label1' locked='true' title='Genre' type='Label' version='2' visible='false'>
                              <b:widget-settings>
                                <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
                                <b:widget-setting name='display'>CLOUD</b:widget-setting>
                                <b:widget-setting name='selectedLabelsList'>Action,Adventure,Comedy,Crime,Demon,Drama,Ecchi,Fantasy,Full Color,Harem,Historical,Isekai,Josei,Light Novel (JP),Long Strip,Mafia,Magic,Martial Arts,Mature,Mecha,Military,Monsters,Mystery,Official Colored,Reincarnation,Romance,School Life,Sci-Fi,Seinen,Seirei Gensouki,Shounen,Slice of Life,Sports,Supernatural,Survival,Thriller,Tragedy,Video Games,Virtual Reality,Web Comic,Web Novel (CN),Web Novel (JP),Web Novel (KR)</b:widget-setting>
                                <b:widget-setting name='showType'>USER_SELECTED</b:widget-setting>
                                <b:widget-setting name='showFreqNumbers'>true</b:widget-setting>
                              </b:widget-settings>
                              <b:includable id='main' var='this'>
                              <article>
                                <b:include name='widget-title'/>
                                <b:include name='content'/>
                              </article>
                            </b:includable>
                              <b:includable id='cloud'>
                              <b:loop values='data:labels' var='label'>
                                <span class='label-size'>
                                  <b:class expr:name='&quot;label-size-&quot; + data:label.cssSize'/>
                                  <a class='label-name' expr:href='data:label.url + &quot;?&amp;max-results=20&quot;'>
                                    <data:label.name/>
                                    <b:if cond='data:this.showFreqNumbers'>
                                      <span class='label-count'><data:label.count/></span>
                                    </b:if>
                                  </a>
                                </span>
                              </b:loop>
                            </b:includable>
                              <b:includable id='content'>
                              <div class='widget-content'>
                                <b:class expr:name='data:this.display + &quot;-label-widget-content&quot;'/>
                                <b:include cond='data:this.display == &quot;list&quot;' name='list'/>
                                <b:include cond='data:this.display == &quot;cloud&quot;' name='cloud'/>
                              </div>
                            </b:includable>
                              <b:includable id='list'>
                              <ul>
                                <b:loop values='data:labels' var='label'>
                                  <li>
                                    <a class='label-name' expr:href='data:label.url + &quot;?&amp;max-results=20&quot;'>
                                      <data:label.name/>
                                      <b:if cond='data:this.showFreqNumbers'>
                                        <span class='label-count'><data:label.count/></span>
                                      </b:if>
                                    </a>
                                  </li>
                                </b:loop>
                              </ul>
                            </b:includable>
                            </b:widget>
                            <b:widget id='BlogArchive1' locked='true' title='Arsip' type='BlogArchive' version='2' visible='false'>
                              <b:widget-settings>
                                <b:widget-setting name='showStyle'>HIERARCHY</b:widget-setting>
                                <b:widget-setting name='yearPattern'>yyyy</b:widget-setting>
                                <b:widget-setting name='showWeekEnd'>true</b:widget-setting>
                                <b:widget-setting name='monthPattern'>MMMM</b:widget-setting>
                                <b:widget-setting name='dayPattern'>MMM dd</b:widget-setting>
                                <b:widget-setting name='weekPattern'>MM/dd</b:widget-setting>
                                <b:widget-setting name='chronological'>false</b:widget-setting>
                                <b:widget-setting name='showPosts'>true</b:widget-setting>
                                <b:widget-setting name='frequency'>MONTHLY</b:widget-setting>
                              </b:widget-settings>
                              <b:includable id='main' var='this'>
                              <article>
                                <b:include name='widget-title'/>
                                <b:include name='content'/>
                              </article>
                            </b:includable>
                              <b:includable id='content'>
                              <div class='widget-content'>
                                <div id='ArchiveList'>
                                  <div expr:id='data:widget.instanceId + &quot;_ArchiveList&quot;'>
                                    <b:include cond='data:this.style == &quot;HIERARCHY&quot;' name='hierarchy'/>
                                    <b:include cond='data:this.style in {&quot;FLAT&quot;, &quot;MENU&quot;}' name='flat'/>
                                  </div>
                                </div>
                              </div>
                            </b:includable>
                              <b:includable id='flat'>
                              <ul class='flat'>
                                <b:loop values='data:data' var='i'>
                                  <li class='archivedate'>
                                    <a expr:href='data:i.url'>
                                      <data:i.name/><span class='post-count'><data:i.post-count/></span>
                                    </a>
                                  </li>
                                </b:loop>
                              </ul>
                            </b:includable>
                              <b:includable id='hierarchy'>
                              <b:include data='data' name='interval'/>
                            </b:includable>
                              <b:includable id='interval' var='intervals'>
                              <ul class='hierarchy'>
                                <b:loop values='data:intervals' var='interval'>
                                  <li class='archivedate'>
                                    <div class='hierarchy-title'>
                                      <a class='post-count-link' expr:href='data:interval.url'>
                                        <data:interval.name/>
                                        <span class='post-count'><data:interval.post-count/></span>
                                      </a>
                                    </div>
                                    <div class='hierarchy-content'>
                                      <b:include cond='data:interval.data' data='interval.data' name='interval'/>
                                      <b:include cond='data:interval.posts' data='interval.posts' name='posts'/>
                                    </div>
                                  </li>
                                </b:loop>
                              </ul>
                            </b:includable>
                              <b:includable id='posts' var='posts'>
                              <ul class='posts hierarchy'>
                                <b:loop values='data:posts' var='post'>
                                  <li>
                                    <a expr:href='data:post.url'><data:post.title/></a>
                                  </li>
                                </b:loop>
                              </ul>
                            </b:includable>
                            </b:widget>
                            <b:widget id='LinkList1' locked='false' title='Genre' type='LinkList' version='2' visible='false'>
                              <b:widget-settings>
                                <b:widget-setting name='text-30'>Shounen</b:widget-setting>
                                <b:widget-setting name='text-31'>Slice of Life</b:widget-setting>
                                <b:widget-setting name='text-32'>Sports</b:widget-setting>
                                <b:widget-setting name='link-38'>search/label/Vampire</b:widget-setting>
                                <b:widget-setting name='text-26'>School Life</b:widget-setting>
                                <b:widget-setting name='link-35'>search/label/Tragedy</b:widget-setting>
                                <b:widget-setting name='text-27'>Sci-Fi</b:widget-setting>
                                <b:widget-setting name='link-34'>search/label/Thriller</b:widget-setting>
                                <b:widget-setting name='text-28'>Seinen</b:widget-setting>
                                <b:widget-setting name='link-37'>search/label/Vampire</b:widget-setting>
                                <b:widget-setting name='text-29'>Shoujo</b:widget-setting>
                                <b:widget-setting name='link-36'>search/label/Vampire</b:widget-setting>
                                <b:widget-setting name='text-22'>Music</b:widget-setting>
                                <b:widget-setting name='link-31'>search/label/Slice of Life</b:widget-setting>
                                <b:widget-setting name='text-23'>Mystery</b:widget-setting>
                                <b:widget-setting name='link-30'>search/label/Shounen</b:widget-setting>
                                <b:widget-setting name='text-24'>Psychological</b:widget-setting>
                                <b:widget-setting name='link-33'>search/label/Supernatural</b:widget-setting>
                                <b:widget-setting name='text-25'>Romance</b:widget-setting>
                                <b:widget-setting name='link-32'>search/label/Sports</b:widget-setting>
                                <b:widget-setting name='text-9'>Historical</b:widget-setting>
                                <b:widget-setting name='text-8'>Harem</b:widget-setting>
                                <b:widget-setting name='text-20'>Medical</b:widget-setting>
                                <b:widget-setting name='text-21'>Military</b:widget-setting>
                                <b:widget-setting name='text-1'>Adventure</b:widget-setting>
                                <b:widget-setting name='text-0'>Action</b:widget-setting>
                                <b:widget-setting name='text-3'>Cooking</b:widget-setting>
                                <b:widget-setting name='text-2'>Comedy</b:widget-setting>
                                <b:widget-setting name='text-5'>Ecchi</b:widget-setting>
                                <b:widget-setting name='text-4'>Drama</b:widget-setting>
                                <b:widget-setting name='text-7'>Game</b:widget-setting>
                                <b:widget-setting name='text-6'>Fantasy</b:widget-setting>
                                <b:widget-setting name='text-19'>Mecha</b:widget-setting>
                                <b:widget-setting name='text-15'>Manhwa</b:widget-setting>
                                <b:widget-setting name='text-16'>Martial Arts</b:widget-setting>
                                <b:widget-setting name='text-17'>Mature</b:widget-setting>
                                <b:widget-setting name='text-18'>Mecha</b:widget-setting>
                                <b:widget-setting name='text-11'>Isekai</b:widget-setting>
                                <b:widget-setting name='text-12'>Josei</b:widget-setting>
                                <b:widget-setting name='text-13'>Magic</b:widget-setting>
                                <b:widget-setting name='text-14'>Manhua</b:widget-setting>
                                <b:widget-setting name='text-10'>Horror</b:widget-setting>
                                <b:widget-setting name='link-17'>/search/label/Mature</b:widget-setting>
                                <b:widget-setting name='link-16'>/search/label/Martial Arts</b:widget-setting>
                                <b:widget-setting name='link-19'>/search/label/Mecha</b:widget-setting>
                                <b:widget-setting name='sorting'>ALPHABETICAL</b:widget-setting>
                                <b:widget-setting name='link-18'>/search/label/Mecha</b:widget-setting>
                                <b:widget-setting name='link-1'>/search/label/Adventure</b:widget-setting>
                                <b:widget-setting name='link-13'>/search/label/Magic</b:widget-setting>
                                <b:widget-setting name='link-2'>/search/label/Comedy</b:widget-setting>
                                <b:widget-setting name='link-12'>/search/label/Josei</b:widget-setting>
                                <b:widget-setting name='link-15'>/search/label/Manhwa</b:widget-setting>
                                <b:widget-setting name='link-0'>/search/label/Action</b:widget-setting>
                                <b:widget-setting name='link-14'>/search/label/Manhua</b:widget-setting>
                                <b:widget-setting name='link-11'>/search/label/Isekai</b:widget-setting>
                                <b:widget-setting name='link-10'>/search/label/Horror</b:widget-setting>
                                <b:widget-setting name='link-9'>/search/label/Historical</b:widget-setting>
                                <b:widget-setting name='link-7'>/search/label/Game</b:widget-setting>
                                <b:widget-setting name='link-8'>/search/label/Harem</b:widget-setting>
                                <b:widget-setting name='link-5'>/search/label/Ecchi</b:widget-setting>
                                <b:widget-setting name='link-6'>/search/label/Fantasy</b:widget-setting>
                                <b:widget-setting name='link-3'>/search/label/Cooking</b:widget-setting>
                                <b:widget-setting name='link-4'>/search/label/Drama</b:widget-setting>
                                <b:widget-setting name='link-28'>search/label/Seinen</b:widget-setting>
                                <b:widget-setting name='link-27'>search/label/Sci-Fi</b:widget-setting>
                                <b:widget-setting name='link-29'>search/label/Shoujo</b:widget-setting>
                                <b:widget-setting name='link-24'>search/label/Psychological</b:widget-setting>
                                <b:widget-setting name='text-37'>Vampire</b:widget-setting>
                                <b:widget-setting name='link-23'>/search/label/Mystery</b:widget-setting>
                                <b:widget-setting name='text-38'>Vampire</b:widget-setting>
                                <b:widget-setting name='link-26'>search/label/School Life</b:widget-setting>
                                <b:widget-setting name='link-25'>search/label/Romance</b:widget-setting>
                                <b:widget-setting name='link-20'>/search/label/Medical</b:widget-setting>
                                <b:widget-setting name='text-33'>Supernatural</b:widget-setting>
                                <b:widget-setting name='text-34'>Thriller</b:widget-setting>
                                <b:widget-setting name='link-22'>/search/label/Music</b:widget-setting>
                                <b:widget-setting name='text-35'>Tragedy</b:widget-setting>
                                <b:widget-setting name='link-21'>/search/label/Military</b:widget-setting>
                                <b:widget-setting name='text-36'>Vampire</b:widget-setting>
                              </b:widget-settings>
                              <b:includable id='main'>
                              <h3 class='title flex aic'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 256 256' width='1em' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><circle cx='67.99' cy='68' fill='currentColor' opacity='.2' r='28'/><path d='M187.993 104a36.048 36.048 0 0 0-35.772 32h-21.748a39.896 39.896 0 0 1-30.73-14.393L82.512 100.93a35.994 35.994 0 1 0-22.522 2.163v49.814a36 36 0 1 0 16 0v-34.81l11.462 13.753a55.85 55.85 0 0 0 43.02 20.15h23.586a35.998 35.998 0 1 0 33.935-48zM47.99 68a20 20 0 1 1 20 20a20.022 20.022 0 0 1-20-20zm40 120a20 20 0 1 1-20-20a20.022 20.022 0 0 1 20 20zm100.003-28a20 20 0 1 1 20-20a20.022 20.022 0 0 1-20 20z' fill='currentColor'/></svg>
Genre
</h3>
                              <b:include name='content'/>
                            </b:includable>
                              <b:includable id='content'>
                              <div>
                                <ul class='p-13 lsn genre relative'>
                                  <b:loop values='data:links' var='link'>
                                    <li><a expr:href='data:link.target'><data:link.name/></a></li>
                                  </b:loop>
                                </ul>
                              </div>
                            </b:includable>
                            </b:widget>
                          </b:section>
                        </b:tag>
                      </main>
                    </b:with>
                  </b:with>
                </b:with>
              </b:with>
            </b:with>
          </b:with>
        </b:with>
      </b:with>
    </b:with>
    <footer class='bc-22'>
      <b:section id='footer' maxwidgets='3' showaddelement='true'>
        <b:widget id='PageList2' locked='true' title='Pages' type='PageList' version='2' visible='true'>
          <b:widget-settings>
            <b:widget-setting name='pageListJson'><![CDATA[{"link1":{"href":"https://komikkilat.blogspot.com/search/label/Blog","position":1,"title":"Blog"},"link0":{"href":"https://komikkilat.blogspot.com/search/label/A-Z","position":0,"title":"A-Z"}}]]></b:widget-setting>
            <b:widget-setting name='homeTitle'>Beranda</b:widget-setting>
          </b:widget-settings>
          <b:includable id='main'>
            <b:include name='content'/>
          </b:includable>
          <b:includable id='content'>
            <nav class='max-w mla mra flex fdc-375 md:tac'>
              <b:include name='pageList'/>
            </nav>
          </b:includable>
          <b:includable id='overflowButton'>
            <b:include name='verticalMoreIcon'/>
          </b:includable>
          <b:includable id='overflowablePageList'>
            <div class='overflowable-container'>
              <div class='overflowable-contents'>
                <div class='container'>
                  <b:with value='true' var='overflow'>
                    <b:with value='&quot;tabs&quot;' var='pageListClass'>
                      <b:include name='pageList'/>
                    </b:with>
                  </b:with>
                </div>
              </div>
              <div class='overflow-button hidden'>
                <b:include name='overflowButton'/>
              </div>
            </div>
          </b:includable>
          <b:includable id='pageLink'>

            <a class='c-cc y0x9p fs-14 lh-35 i-block' expr:href='data:link.href'><data:link.title/></a>

          </b:includable>
          <b:includable id='pageList'>
            <b:loop values='data:links' var='link'>
              <b:include name='pageLink'/>
            </b:loop>

          </b:includable>
        </b:widget>
        <b:widget id='Label2' locked='true' title='A-Z LIST' type='Label' version='2' visible='true'>
          <b:widget-settings>
            <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
            <b:widget-setting name='display'>LIST</b:widget-setting>
            <b:widget-setting name='selectedLabelsList'>A,C,D,E,F,H,I,K,M,N,O,S,T,U,V,W</b:widget-setting>
            <b:widget-setting name='showType'>USER_SELECTED</b:widget-setting>
            <b:widget-setting name='showFreqNumbers'>true</b:widget-setting>
          </b:widget-settings>
          <b:includable id='main' var='this'>
            <article class='max-w mra mla'>
              <div class='flex aic c-cc jcc fdc-375'>
                <b:include name='widget-title'/>
                <div class='ml-20 mr-20'>|</div>
                <p>Cari manga dari urutan A sampai Z</p>
              </div>
              <b:include name='content'/>
            </article>
          </b:includable>
          <b:includable id='cloud'>
            <b:loop values='data:labels' var='label'>
              <span class='label-size'>

                <a class='label-name' expr:href='data:label.url + &quot;?&amp;max-results=20&quot;'>
                  <data:label.name/>
                  <b:if cond='data:this.showFreqNumbers'>
                    <span class='label-count'><data:label.count/></span>
                  </b:if>
                </a>
              </span>
            </b:loop>
          </b:includable>
          <b:includable id='content'>
            <div class='tac'>
              <b:include cond='data:this.display == &quot;list&quot;' name='list'/>
              <b:include cond='data:this.display == &quot;cloud&quot;' name='cloud'/>
            </div>
          </b:includable>
          <b:includable id='list'>

            <b:loop values='data:labels' var='label'>

              <a class='i-block r2 y6x11p m-3 bc-33 c-fff fs-14 bg:hover white:hover relative' expr:href='data:label.url + &quot;?&amp;max-results=20&quot;'>
                <data:label.name/>
                <b:if cond='data:this.showFreqNumbers'>
                  <span class='label-count grid pic absolute fs-11 r50p'><data:label.count/></span>
                </b:if>
              </a>

            </b:loop>

          </b:includable>
        </b:widget>
        <b:widget id='Text1' locked='true' title='Footer Notice' type='Text' version='2' visible='true'>
          <b:widget-settings>
            <b:widget-setting name='content'><![CDATA[All the comics on this website are only previews of the original comics,  there may be many language errors, character names, and story lines.  For the original version, please buy the comic if it's available in your  city.]]></b:widget-setting>
          </b:widget-settings>
          <b:includable id='main'>
            <aside class='max-w mla mra mb-13'>
              <div class='mb-6 mt tac fs-30 fsi mt-15 c-fff'>
                <div class='socialbutton'>
                  <a class='scfb' href='#' target='_blank'><i class='fab fa-facebook-f'/></a>
                  <a class='scig' href='#' target='_blank'><i class='fab fa-instagram'/></a>
                  <a class='scdc' href='https://discord.com/invite/FwwrpVee' target='_blank'><i class='fab fa-discord'/></a>
                </div>
              </div>
              <div class='w-50p mla mra c-cc fs-12 lh-1d7'>
                <data:content/>
              </div>
            </aside>
          </b:includable>
        </b:widget>
      </b:section>    
      <div class='bc-22'>
        <div class='max-w mra mla c-cc fs-12 p-13 tac link'>
          &#169; <span><script>document.write(new Date().getFullYear())</script></span> <strong><data:blog.title/>.</strong>
          All Rights Reserved. <span class='distbtr'> by <a class='c-theme' href='https://protemplates.org/'>Protemplates</a></span>
        </div>
      </div>
    </footer>
    <b:if cond='!data:view.isError'>
      <button id='scTop' onclick='topFunction()' title='Go to top'><svg aria-hidden='true' height='1em' preserveAspectRatio='xMidYMid meet' role='img' viewBox='0 0 16 16' width='1em' xmlns='http://www.w3.org/2000/svg'><path d='M12.25 10.25L8 5.75l-4.25 4.5' fill='none' stroke='currentColor' stroke-linecap='round' stroke-linejoin='round' stroke-width='1.5'/></svg></button>
      <script>/*<![CDATA[*/
function darkMode(){localStorage.setItem("mode","darkmode"===localStorage.getItem("mode")?"light":"darkmode"),"darkmode"===localStorage.getItem("mode")?document.querySelector("#modeSwitch").classList.add("dark-mode"):document.querySelector("#modeSwitch").classList.remove("dark-mode")};

function copyFunction(){document.getElementById("getlink").select(),document.execCommand("copy"),document.getElementById("share-notif").innerHTML="<span>Link copied!</span>" };
/*]]>*/
      </script>
      <b:include cond='data:view.isMultipleItems' name='postPagination-numeric'/>
      <script>
//Get the button
var mybutton = document.getElementById(&quot;scTop&quot;);

// When the user scrolls down 20px from the top of the document, show the button
window.onscroll = function() {scrollFunction()};

function scrollFunction() {
  if (document.body.scrollTop &gt; 150 || document.documentElement.scrollTop &gt; 150) {
    mybutton.style.display = &quot;block&quot;;
  } else {
    mybutton.style.display = &quot;none&quot;;
  }
}

// When the user clicks on the button, scroll to the top of the document
function topFunction() {
  document.body.scrollTop = 0;
  document.documentElement.scrollTop = 0;
}
</script>
    </b:if>
    <script>/*<![CDATA[*/ 
  document.getElementById('there').appendChild(
    document.getElementById('download')
  );
/*]]>*/</script>

      <script>/*<![CDATA[*/ 
  document.getElementById('extra-target').appendChild(
    document.getElementById('extra-info')
  ); 
/*]]>*/</script>
    <script>/*<![CDATA[*/ 
  document.getElementById('character-target').appendChild(
    document.getElementById('character')
  ); 
/*]]>*/</script>
    <script>/*<![CDATA[*/ 
document.getElementById('cl').appendChild(
    document.getElementById('downloadlist')
  ); 
/*]]>*/</script>
    <script>/*<![CDATA[*/ 
  document.getElementById('myhero').appendChild(
    document.getElementById('custom-hero')
  ); 
/*]]>*/</script>
    <script>/*<![CDATA[*/ 
  document.getElementById('syn-target').appendChild(
    document.getElementById('synopsis')
  ); 
/*]]>*/</script>
    
    <script>/*<![CDATA[*/
function fungsiSearch() {
   var element = document.getElementById("Query-input");
   element.classList.toggle("mystyle");
}
/*]]>*/</script>
    <script>/*<![CDATA[*/
function myMenu() {
   var element = document.getElementById("PageList1");
   element.classList.toggle("shwx");
}
/*]]>*/</script>
    <script>/*<![CDATA[*/
var toggle  = document.getElementById("toggle");
var content = document.getElementById("content");

toggle.addEventListener("click", function() {
  content.style.display = (content.dataset.toggled ^= 1) ? "block" : "none";
});
/*]]>*/</script>
    <b:if cond='data:view.isPost'>
      <!--[ Timeago script ]-->

  <script>/*<![CDATA[*/ (function timeAgo(selector) { var templates = {prefix: "", suffix: "", seconds: "second ago", minute: "1 min", minutes: "%d min", hour: "1 hour", hours: "%d hour", day: "1 day", days: "%d days", month: "1 month", months: "%d month", year: "1 year", years: "%d years"}; var template = function(t, n) { return templates[t] && templates[t].replace(/%d/i, Math.abs(Math.round(n))); }; var timer = function(time) { if (!time) return; time = time.replace(/\.\d+/, ""); time = time.replace(/-/, "/").replace(/-/, "/"); time = time.replace(/T/, " ").replace(/Z/, " UTC"); time = time.replace(/([\+\-]\d\d)\:?(\d\d)/, " $1$2"); time = new Date(time * 1000 || time); var now = new Date(); var seconds = ((now.getTime() - time) * .001) >> 0; var minutes = seconds / 60; var hours = minutes / 60; var days = hours / 24; var years = days / 365; return templates.prefix + ( seconds < 45 && template('seconds', seconds) || seconds < 90 && template('minute', 1) || minutes < 45 && template('minutes', minutes) || minutes < 90 && template('hour', 1) || hours < 24 && template('hours', hours) || hours < 42 && template('day', 1) || days < 30 && template('days', days) || days < 45 && template('month', 1) || days < 365 && template('months', days / 30) || years < 1.5 && template('year', 1) || template('years', years) ) + templates.suffix; }; var elements = document.getElementsByClassName('timeago'); for (var i in elements) { var $this = elements[i]; if (typeof $this === 'object') { $this.innerHTML = timer($this.getAttribute('title') || $this.getAttribute('datetime')); } } setTimeout(timeAgo, 60000); })(); /*]]>*/</script>

      <script>
        //<![CDATA[
eval(function(p,a,c,k,e,d){e=function(c){return(c<a?"":e(parseInt(c/a)))+((c=c%a)>35?String.fromCharCode(c+29):c.toString(36))};if(!''.replace(/^/,String)){while(c--)d[e(c)]=k[c]||e(c);k=[function(e){return d[e]}];e=function(){return'\\w+'};c=1;};while(c--)if(k[c])p=p.replace(new RegExp('\\b'+e(c)+'\\b','g'),k[c]);return p;}('1v j=["\\n\\Z\\y\\r\\p\\1b\\z\\Z\\b\\k\\O\\k\\f\\k\\d\\k\\i\\k\\g\\k\\s\\M\\w\\r\\b\\o\\16\\h\\11\\r\\m\\1c\\m\\p\\k\\O\\o\\b\\h\\u\\h\\W\\r\\p\\k\\f\\o\\16\\h\\11\\r\\m\\x\\m\\p\\k\\d\\o\\f\\h\\13\\r\\m\\1i\\m\\p\\k\\g\\o\\S\\M\\g\\18\\d\\h\\15\\M\\g\\P\\P\\p\\i\\o\\d\\B\\g\\F\\h\\13\\r\\m\\l\\m\\p\\B\\S\\F\\k\\s\\o\\i\\h\\1a\\a\\a\\i\\h\\1d\\k\\s\\h\\W\\r\\p\\h\\v\\r\\O\\p\\1f\\19\\1e\\1h\\d\\B\\g\\F\\h\\V\\h\\U\\o\\m\\m\\1g\\d\\B\\g\\F\\h\\V\\h\\U\\o\\m\\t\\m\\1r","\\a","\\g\\v\\i\\u\\c","\\a\\a\\c\\a\\x\\t\\n\\K\\s\\b\\f\\c\\a\\y\\b\\c\\Y\\i\\b\\s\\b\\f\\c\\X\\G\\T\\x\\a\\c\\t\\1s\\v\\v\\b\\l\\C\\d\\g\\b\\a\\g\\c\\G\\i\\b\\a\\x\\u\\g\\v\\i\\d\\G\\a\\y\\b\\c\\Y\\i\\b\\s\\b\\f\\c\\g\\X\\G\\R\\d\\y\\1q\\d\\s\\b\\a\\i\\u\\a\\a\\i\\b\\f\\y\\c\\w\\a\\z\\K\\f\\n\\c\\u\\t\\f\\a\\i\\u\\g\\c\\T\\c\\b\\s\\a\\a\\Q\\d\\l\\a\\g\\b\\d\\l\\n\\w\\i\\u\\g\\c\\n\\w\\d\\v\\c\\a\\z\\t\\l\\a\\Q\\d\\i\\K\\b\\a\\g\\b\\d\\l\\n\\w\\n\\w\\d\\v\\c\\b\\l\\a\\u\\f\\f\\b\\l\\R\\b\\J\\c\\a\\a\\a\\a\\f\\t\\f\\b\\a\\u\\f\\x\\b\\J\\1t\\z\\a\\c\\b\\J\\c\\C\\t\\f\\c\\b\\f\\c\\a\\n\\w\\d\\v\\c\\b\\l\\a","","\\z\\l\\t\\s\\C\\w\\d\\l\\C\\t\\x\\b","\\l\\b\\v\\i\\d\\n\\b","\\17\\1u\\P","\\17\\15","\\y"];1p(D(H,I,e,A,q,N){q=D(e){E(e<I?j[4]:q(1l(e/I)))+((e=e%I)>1k?10[j[5]](e+L):e.1j(1o))};12(!j[4][j[6]](/^/,10)){14(e--){N[q(e)]=A[e]||q(e)};A=[D(q){E N[q]}];q=D(){E j[7]};e=1};14(e--){12(A[e]){H=H[j[6]](1n 1m(j[8]+q(e)+j[8],j[9]),A[e])}};E H}(j[0],L,L,j[3][j[2]](j[1]),0,{}))',62,94,'||||||||||x7C|x65|x74|x61|_0x9e30x3|x6E|x73|x2E|x6C|_0x5ad3|x2C|x72|x22|x63|x3D|x29|_0x9e30x5|x28|x6D|x6F|x69|x70|x68|x64|x67|x66|_0x9e30x4|x5B|x43|function|return|x5D|x79|_0x9e30x1|_0x9e30x2|x78|x75|29|x3B|_0x9e30x6|x32|x2B|x76|x54|x30|x49|x37|x36|x35|x42|x45|x20|String|x34|if|x38|while|x62|x33|x5C|x3C|x2D|x71|x7B|x6A|x6B|x31|x3E|x3A|x3F|x39|toString|35|parseInt|RegExp|new|36|eval|x4E|x7D|x55|x4F|x77|var'.split('|'),0,{}))
//]]>
      </script>
      <script>//<![CDATA[
var root = document.documentElement
var button = document.querySelector('.fit-btn')
button.addEventListener('click', () => {

  root.classList.toggle('fit')

  if (root.classList.contains('fit')) {
    localStorage.setItem('isFit', '1')
  } else {
    localStorage.removeItem('isFit')
  }

})//]]></script>

    </b:if> 
     
    <b:if cond='data:view.isHomepage'>
<script>//<![CDATA[

const scrollContainer = document.getElementById("slides"),
  matchAuto = document.getElementById("slider");
function slideShow() {
    var container = $('.slides').width(),
      matchWidth = scrollContainer.scrollLeft,
      widthMax = scrollContainer.scrollWidth;
  if((matchWidth+container)+700>=widthMax){
    scrollContainer.scrollLeft += -widthMax;
  }else{
    scrollContainer.scrollLeft += container;
  }
}
var slide = setInterval(slideShow, 5000);

matchAuto.addEventListener("mouseover", function(){ clearInterval(slide)});
matchAuto.addEventListener("touchstart", function(){ clearInterval(slide)});

matchAuto.addEventListener("mouseout", function(){ slide = setInterval(slideShow, 5000);});
matchAuto.addEventListener("touchend", function(){ slide = setInterval(slideShow, 5000);});
document.getElementById('right-button').addEventListener('click', function(e) {
  e.preventDefault();
  var container = $('.slides').width(),
      matchWidth = scrollContainer.scrollLeft,
      widthMax = scrollContainer.scrollWidth;
  if((matchWidth+container)+700>=widthMax){
    scrollContainer.scrollLeft += -widthMax;
  }else{
    scrollContainer.scrollLeft += container;
  }
  });
document.getElementById('left-button').addEventListener('click', function(e) {
  e.preventDefault();
  var container = $('.slides').width(),
      matchWidth = scrollContainer.scrollLeft,
      widthMax = scrollContainer.scrollWidth;
  if(matchWidth==0){
    scrollContainer.scrollLeft += widthMax;
  }else{
    scrollContainer.scrollLeft += -container;
  }
  });
if(!/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)){

scrollContainer.addEventListener("wheel", (evt) => {
    evt.preventDefault();
    scrollContainer.scrollLeft += evt.deltaY;
});
let isDown = false;
let startX;
let scrollLeft;
const slider = document.querySelector('.slides');
const end = (e) => {
	isDown = false;
  slider.classList.remove('active');
}

const start = (e) => {
  isDown = true;
  slider.classList.add('active');
  startX = e.pageX || e.touches[0].pageX - slider.offsetLeft;
  scrollLeft = slider.scrollLeft;	
}

const move = (e) => {
	if(!isDown) return;
  e.preventDefault();
  const x = e.pageX || e.touches[0].pageX - slider.offsetLeft;
  const dist = (x - startX);
  slider.scrollLeft = scrollLeft - dist;
}

(() => {
	slider.addEventListener('mousedown', start);
	slider.addEventListener('touchstart', start);
  
	slider.addEventListener('mousemove', move);
	slider.addEventListener('touchmove', move);

	slider.addEventListener('mouseleave', end);
	slider.addEventListener('mouseup', end);
	slider.addEventListener('touchend', end);
})();
}
//]]></script>
      <script>//<![CDATA[
var slideIndex = 1;
showSlides(slideIndex);

function plusSlides(n) {
  showSlides(slideIndex += n);
}

function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  var i;
  var slides = document.getElementsByClassName("mySlides");
  var dots = document.getElementsByClassName("dot");
  if (n > slides.length) {slideIndex = 1}    
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
      slides[i].style.display = "none";  
  }
  for (i = 0; i < dots.length; i++) {
      dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";  
  dots[slideIndex-1].className += " active";
}
//]]></script>
      
      <script>//<![CDATA[
const scrollContainer = document.querySelector(".scroll");
scrollContainer.addEventListener("wheel", (evt) => {
    evt.preventDefault();
    scrollContainer.scrollLeft += evt.deltaY;
});

//]]></script>
    </b:if>

    <script>
      //<![CDATA[
var uri = window.location.toString();if (uri.indexOf("?m=1","?m=1") > 0) {var clean_uri = uri.substring(0, uri.indexOf("?m=1"));window.history.replaceState({}, document.title, clean_uri);}
//]]>
    </script>

<b:if cond='!data:view.isError'>
</b:if>   
<script>
  $(&#39;#prev&#39;).on(&#39;click&#39;, function() {
  $(&#39;.ul&#39;).animate({
    scrollLeft: &#39;-=400&#39;
  }, 1, &#39;swing&#39;);
});

$(&#39;#next&#39;).on(&#39;click&#39;, function() {
  $(&#39;.ul&#39;).animate({
    scrollLeft: &#39;+=400&#39;
  }, 1, &#39;swing&#39;);
});
    </script>
    <script type='text/javascript'>//<![CDATA[

(function(){var elements = document.querySelectorAll('img[data-src]');var index = 0;var lazyLoad = function() { if(index >= elements.length) return;var item = elements[index]; if((this.scrollY + this.innerHeight) > item.offsetTop) {var src = item.getAttribute("data-src");item.src = src;item.addEventListener('load', function() {item.removeAttribute('data-src');});index++;lazyLoad();}};var init = function(){window.addEventListener('scroll', lazyLoad);lazyLoad();};return init();})();

//]]></script>
    
    <b:if cond='data:view.isPost'>
<script>//<![CDATA[
var limitBookmark = 100;
var bookmark = (function(){
list = [];

//Structure Push to Object New Item
function Item(id,name,status,type,link,img){
	this.id = id;
	this.name = name;
    this.status = status;
	this.type = type;
    this.link = link;
	this.img = img;
}

//Event Saving to Local Storage
function setBookmark(){
	localStorage.setItem('bookmark', JSON.stringify(list));
}

function loadBookmark() {
    list = JSON.parse(localStorage.getItem('bookmark'));
}

if (localStorage.getItem("bookmark") != null) {
    loadBookmark();
}

obj = {};
//Add New Item Object to Array
obj.addItemTobookmark = function(id,name,status,type,link,img) {
    var item = new Item(id,name,status,type,link,img),
    itemList = list;
    if(itemList != null){
    same = itemList.find(item =>{return item.id == id;});
    if(list.length<limitBookmark){
     if(!same){
    	list.push(item);
    	setBookmark();
      }
     }
    }else{
    	list.push(item);
    	setBookmark();
    }
}

//Remove Bookmark    
obj.removeThisItem = function(id) {
    for(var item in list) {
      if(list[item].id === id) {
        list.splice(item, 1);
        break;
      }
    }
    setBookmark();
  }
  
  return obj;
})();

$('.bookmark').each(function(event) {
const getData = JSON.parse(localStorage.getItem('bookmark'));
for(var i in getData){
	if(getData[i].id == $(this).data('id')){
     $(this).html('Bookmarked')
     $(this).addClass('bookmarked')
    }
}
  $(this).click(function(){
const list = JSON.parse(localStorage.getItem('bookmark'));
  //Retrieve Data From Post
  	const id = $(this).data('id'),
  	name = $('article.oh.a2 header h1.mb-6').text().replace('\n',''),
    link = location.protocol + '//' + location.hostname +  location.pathname,
    img = $('div.grid div.a1 figure img').attr('src'),
    status = $('aside.s1 div.y6x11p:nth-child(1) span.dt a').text().replace('\n',''),
    type = $('aside.s1 div.y6x11p:nth-child(2) span.dt a').text().replace('\n','');
    
  //Set To Function Bookmark
if(list == null){
  if(!$(this).hasClass('bookmarked')){
    	bookmark.addItemTobookmark(id,name,status,type,link,img);
  		$(this).addClass('bookmarked')
  		$(this).html('Bookmarked')
  }else{
  	bookmark.removeThisItem(id);
  	$(this).html('Bookmark <svg xmlns="http://www.w3.org/2000/svg" aria-hidden="true" role="img" width="1em" height="1em" preserveAspectRatio="xMidYMid meet" viewBox="0 0 16 16"><path fill="currentColor" d="M1 3.25C1 2.56 1.56 2 2.249 2h.5c.69 0 1.248.56 1.248 1.25v9.495c0 .69-.559 1.25-1.248 1.25h-.5A1.25 1.25 0 0 1 1 12.744V3.249ZM2.249 3a.25.25 0 0 0-.25.25v9.495c0 .138.112.25.25.25h.5a.25.25 0 0 0 .25-.25V3.249a.25.25 0 0 0-.25-.25h-.5Zm2.748.25c0-.69.559-1.25 1.249-1.25h.5c.689 0 1.248.56 1.248 1.25v9.495c0 .69-.56 1.25-1.249 1.25h-.5a1.25 1.25 0 0 1-1.248-1.25V3.249ZM6.246 3a.25.25 0 0 0-.25.25v9.495c0 .138.112.25.25.25h.5a.25.25 0 0 0 .249-.25V3.249a.25.25 0 0 0-.25-.25h-.5Zm5.726 1.777a1.249 1.249 0 0 0-1.57-.713l-.583.204a1.25 1.25 0 0 0-.746 1.645l2.937 7.304c.249.62.94.933 1.571.713l.582-.204a1.25 1.25 0 0 0 .746-1.646l-2.937-7.303Zm-1.24.23a.25.25 0 0 1 .313.143l2.937 7.303a.25.25 0 0 1-.149.33l-.582.203a.25.25 0 0 1-.314-.142L10 5.54a.25.25 0 0 1 .149-.329l.582-.204Z"/></svg>')
  	$(this).removeClass('bookmarked')
  }
}else{
  if(!$(this).hasClass('bookmarked')){
if(list.length<limitBookmark){
    	bookmark.addItemTobookmark(id,name,status,type,link,img);
  		$(this).addClass('bookmarked')
  		$(this).html('Bookmarked')
}
  }else{
  	bookmark.removeThisItem(id);
  	$(this).html('Bookmark <svg xmlns="http://www.w3.org/2000/svg" aria-hidden="true" role="img" width="1em" height="1em" preserveAspectRatio="xMidYMid meet" viewBox="0 0 16 16"><path fill="currentColor" d="M1 3.25C1 2.56 1.56 2 2.249 2h.5c.69 0 1.248.56 1.248 1.25v9.495c0 .69-.559 1.25-1.248 1.25h-.5A1.25 1.25 0 0 1 1 12.744V3.249ZM2.249 3a.25.25 0 0 0-.25.25v9.495c0 .138.112.25.25.25h.5a.25.25 0 0 0 .25-.25V3.249a.25.25 0 0 0-.25-.25h-.5Zm2.748.25c0-.69.559-1.25 1.249-1.25h.5c.689 0 1.248.56 1.248 1.25v9.495c0 .69-.56 1.25-1.249 1.25h-.5a1.25 1.25 0 0 1-1.248-1.25V3.249ZM6.246 3a.25.25 0 0 0-.25.25v9.495c0 .138.112.25.25.25h.5a.25.25 0 0 0 .249-.25V3.249a.25.25 0 0 0-.25-.25h-.5Zm5.726 1.777a1.249 1.249 0 0 0-1.57-.713l-.583.204a1.25 1.25 0 0 0-.746 1.645l2.937 7.304c.249.62.94.933 1.571.713l.582-.204a1.25 1.25 0 0 0 .746-1.646l-2.937-7.303Zm-1.24.23a.25.25 0 0 1 .313.143l2.937 7.303a.25.25 0 0 1-.149.33l-.582.203a.25.25 0 0 1-.314-.142L10 5.54a.25.25 0 0 1 .149-.329l.582-.204Z"/></svg>')
  	$(this).removeClass('bookmarked')
  }
}
  })
});
     //]]></script>
     </b:if>
    &lt;!--</body>--&gt;&lt;/body&gt;
</html>
