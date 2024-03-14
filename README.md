# 书源日记

#### 介绍

★活力宝的书源日记-仅作学习交流之用.

<h2>此文仅用于学习交流，严禁用做它用，造成什么后果请自负.</h2>

### ☆非得到本人同意，禁止转载，违者必究.毕竟是零零散散的东西.

### ☆书源写法之个人见解

参考文档:[Html结构解析](https://www.cnblogs.com/iamspecialone/p/11139491.html)

参考文档:[HTML 标签参考手册](https://www.w3school.com.cn/tags/index.asp)

参考文档: [CSS 选择器参考手册](https://www.w3school.com.cn/cssref/css_selectors.asp)

(这个CSS 选择器参考手册有助于了解选择器的意思,实际做源的时候阅读APP使用的有它自己的一套更简单的写法)

参考文档:[阅读APP书源制作帮助文档](https://alanskycn.gitee.io/teachme/Rule/source.html)

参考文档:[正则表达式教程](https://www.runoob.com/regexp/regexp-tutorial.html)

参考视频:[HMLT5+CSS3制作前端网页](https://www.bilibili.com/video/BV1wS4y1G72k)

参考视频:[关耳大佬的【阅读3.0】书源制作过程(基础语法)](https://www.bilibili.com/video/BV1py4y1J73u)


简单说句废话,想学怎么写源想少走弯路建议在写之前打下HTML与CSS的基础,不求你都看懂,只要知道它网站的源码是怎么一个套一个的,他的属性我们怎么能取的到.

简单介绍Html与CSS样式的关系
html呢,相当于一个国家,一个大容器.里面有很多省市县乡村户等等.
就是它的框架结构是有层级关系的.大概理解成祖宗,爷爷,父亲,兄弟,儿子,子孙等等层级也可以.

CSS样式呢,相当于人身上的服饰之类的.就是原本大家都一样的.加上CSS样式之后可以让网站变的更丰富多彩,比如文字大小呀,文字颜色呀,鼠标放到字上面它变颜色呀等等..

```
<!DOCTYPE html>//声明这是个HTML5的文档,写源的时候不用在意它
<html>//html主框架相当于地球,    一般大部分标签都是有结束标签的,一个<html>开始对应着</html>为结尾,这样叫成套出现,只有少部分的标签是单独出现的.
    <head>//head隐藏加载框架相当于国家.    这个是网站预加载的内容,对于用户隐藏进行的,就是它不是展现给普通大众看的,它是给网站制作者们看的.它同样是有</head>为结尾.
        <meta charset="UTF-8" />//这个相当于省份.    这个是给出网站的语言解码信息.UTF-8是国际通用的码,码库相对于gbk***的要大一些.
        <link rel="stylesheet" href="/static/css/style.css"/>//这个也是省份.    这个是外部加载网站的CSS样式.
    </head>
    <body>//国,这里开始往后面到</body>里出现的东西都是面向普通网友的,就是大家能正常看到的东西都在下面这里面.
       <div class="g-plate">//省
            <p class="hd"> 重磅推荐 </p>//市   
            <ul class="list-3">//市
                <li>//县
                </li>
            </ul>
        </div>
    </body>
</html>//html主框架结束
```
大概意思呢,就是他们有层级关系的.


简单解释下标签的意思,拿这个```<div class="g-plate">```来说吧


这里的div是标签名,在阅读里面选它的时候用tag.标签名来选择,或者直接标签名前面啥也不加也可以.


class="g-plate" 这个是说刚这个div标签的class属性它的值等于g-plate. 这个g-plate不用管他啥意思,简单点就把它想成是它的名字就可以了,一般我们都是想要他们的值定位的东西.


它的名字还可以有多个.多个名字中间以空格隔开.


比如```<ul class="list-3 list-2">``` 这样它的名字可以叫list-3 list-2也可以单独叫list-3或者单独叫list-2


那么问题来了,名字会不会重名.重复的名字的话,可以通过定位它是谁家的,或者定位它名字中与别人不一样的.或者第几排第几个的小明同学.这样也可以.


class.祖级名字@class.父级名字@class.自己名字(或者自己的那个标签名tag.自己标签名)@最后找自己身上的衣服呀还是帽子呀还是鞋子.


class.zujimz@clas.fujimz@tag.a@text


阅读里的class可以用英文句号点来代替比如: .zujimz  这个跟class.zujimz用途一样,[.]就是个简写class方法


阅读里的id可以用#来代替比如:#xxx   这个跟id.xxx用途一样,[#]就是个简写id的方法


阅读里的tag有时候图省事也可以省略不写


阅读里的@ 可以用空格代替


.zujimz .fujimz a@text



特别说明一下,class属性的名字可能会出现多处.id属性它的名字大部分情况下都是独立唯一的.因为它不但有普通的显示作用还具备定位的作用,所以一般都是唯一的.


所以在取属性的时候自己考虑怎么选择,我建议有id取id,没有的话取class或者别的. 它又不限制你取哪个属性,能得到自己想要的信息就可以.



在阅读里写源也就是通过这些已知条件来挑选自己想要的东西.



### 关于[property$=book_name]@content这个写法的找法公布.


首先感谢酷安大佬:糖果超甜哒


这个怎么找的方法我是从她那里学的,可能现在没有原文了,以前在她的动态里面翻到的一个教程.


1.这个一般用于做书源的详情页.随便找本小说进入详情页后,在网站源码里面翻翻看head这个区域里面有没有相关的标签.


比如这一条:

```<meta property="og:novel:book_name" content="活力宝祝大家开心每一天!">```



meta是它的标签名,property是它的属性名,og:novel:book_name是它的属性名. 它的content的值就是我们要找的东西.


就是找有property属性名字末尾($的意思代表末尾是啥啥啥,^代表开始是啥啥啥)为book_name的,它的content的值或者名字文字之类的..大概就那个意思吧.


它其实还有个傻瓜写法:[property="og:novel:book_name"]@content


这样写也可以.  他们后面一样可以用##来挑选自己想要的内容或者剔除自己不想要的内容.具体的看阅读帮助文档.



学会灵活利用做书源的时候那个问号,里面可以自己添加快捷词条啥的.比如把这详情页几大简便写法给加进去,下次遇到类似的,就直接去点就可以了,比复制粘贴都快.


简单点的学习方法就是拿别人做好的源,去复刻一下,看看自己能不能理解别人怎么写的源,自己能不能按他已经给的方法去找到相对应的东西.


其它的去瞅关耳大佬的视频教学吧. 遇到不懂可以回来翻翻笔记哦.

### 日记第三版,自己折腾自己用
```
------书源里的选择器方法简写-----
案例一
class.名字1@text
简写为
.名字1@text

案例二
class.名字1 名字2 名字3@text
简写为
.名字1.名字2.名字3@text

如果这三个名字中哪个是唯一出现的话也可以单独拿出来用比如:  .名字3@text
也可以: .名字1.名字2@text 
自己灵活搭配使用

案例三
(当遇到id与class在同一标签里的时候优选id属性,因为id的优先权比class高,主要它具有唯一性,不容易像class那样出现多个一样的class.)
id.最优选哦@text
简写为
#最优选哦@text 

案例四
(有时候@连接上下层符号可以用一个空格来代替,除非标签的class属性有很多个属性名(比如案例二那个)要特别处理一下开始的class怎么写)
class.xxx@li@a@text
简写为
.xxx li a@text
---------------------------------------------
基本页请求头
在里面加referer信息破网站防盗链，比如在A网站里面的B链接地址，要是正常访问B链接它会自动跳回到A网站，那么在请求头里面带上'referer':A网站,有可能可以破除它的防盗链
{
'referer':'https://official.bkvvvvv.com/'
}
或者
{"referer":"https://mjjxs.net"}
或者
{"headers":{"Referer":baseUrl}};
或者
书源基本页面，请求头，@js:JSON.stringify({"referer":baseUrl})

"headers":{"Referer": "{{baseUrl}}"}

{
	"User-Agent":"Mozilla/5.0 (Linux; Android 9) Mobile Safari/537.36","referer":"{{baseUrl}}"
	}

{ "User-Agent": "Mozilla/5.0 (Linux; Android 11) Mobile Safari/537.36"}

{'User-Agent':'Mozilla/5.0 (Linux; Android 11; PCAM10 Build/RP1A.200720.011; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/83.0.4103.106 Mobile Safari/537.36'}

{"User-Agent":"Mozilla/5.0 (Linux; Android 11; PCAM10 Build/RP1A.200720.011; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/100.0.4103.106 Mobile Safari/537.36"}

小米浏览器UA，使用百度流畅，此UA不要全局使用，盗版网站会给大厂浏览器UA加上专属网页广告
{'User-Agent':'Mozilla/5.0 (Linux; Android 12) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/109.0.5414.86 Mobile Safari/537.36 XiaoMi/MiuiBrowser/17.2.79 swan-mibrowser'}
苹果手机请求头
{"User-Agent": "Mozilla/5.0 (iPhone; CPU iPhone OS 13_2_3 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/13.0.3 Mobile/15E148 Safari/604.1"}

请求头
{'User-Agent':'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/534.24 (KHTML, like Gecko) Chrome/71.0.3578.141 Safari/534.24 XiaoMi/MiuiBrowser/12.4.14'}

或者
{
  "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/58.0.3029.110 Safari/537.36"
}

或者
{
 'User-Agent': 'Mozilla/5.0 (Linux; Android 11; Pixel 3 XL Build/RQ3A.211001.001; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/102.0.4988.0 Mobile Safari/537.36 SearchCraft/3.9.2 (Baidu; P1 11) '
}

或者
{"User-Agent": "Mozilla/5.0 (Linux; Android 12; M2011K2C Build/SKQ1.211006.001; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/102.0.5005.99 Mobile Safari/537.36 T7/12.16 SearchCraft/3.9.1 (Baidu; P1 11)"}

或者
{'User-Agent':'Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/86.0.4240.198 Mobile Safari/537.36',
"Referer":"http://m.b777777.com/"}

或者
{
	"User-Agent":"Mozilla/5.0 (Linux; Android 12; Nexus 5X Build/NRD90M); wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/96.0.4664.104 Mobile Safari/537.36"
}

或者请求头2
{
  "User-Agent": "Mozilla/5.0 (Windows; U; Windows NT 5.2;. en-US) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/78.0.3904.108 Safari/537.36 Quark/4.6.2.161"
}

或者手机百度ua
{"User-Agent": "Mozilla/5.0 (Linux; Android 11; PCAM10 Build/RP1A.200720.011; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/97.0.4692.98 Mobile Safari/537.36 T7/13.32 SP-engine/2.70.0 baiduboxapp/13.32.5.10 (Baidu; P1 11) NABar/1.0"}

或者
{'webView': true,"header":{"referer":"https://mjjxs.net"}}

URL规则后面加上Java.log查看获取页面调试结果用的
tag.a@href<js>java.log(result)</js>
或者这样写
tag.a@href@js:java.log(result)
或者这样写
@js:java.log(src)

跨栏目存取数据
比如在搜索栏的书名里面存了个id这里的@put:{id:$.Id}就是存储数据，括号里的id是名字，:后面的是它要存的内容公式字符等等
Name@put:{id:$.Id}
然后到目录页里面的章节url里面调用它，这里的@get:{id}就是调用前面存储的数据
https://conhhs.pggfggi.com/BookFiles/Html/@get:{cid}/@get:{id}/{{$.id}}.html

搜索规则重定向处理案列
@js:
url="https://m.fushutxt.cc/e/search/index.php";
body="show=title&keyboard="+key;
$=java.post(url,body,{}).header("Location");
java.log("https://m.fushutxt.cc/e/search/"+$);
或者
{{java.post('https://m.siyixs.com/search/','keyword='+key+'&submit=',{}).header("Location")}}
或者
<js>
url="https://m.siyixs.com";
head={"User-Agent": "Mozilla/5.0 (Windows NT 10.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko, By Black Prism) Chrome/99.0 Safari/537.36","content-type":"application/x-www-form-urlencoded","Cookie":"5ydev_t=15; 5ydev_cdn=https%3A%2F%2Ffastly.jsdelivr.net%2Fgh%2Fiquns%2Fxs%40289%2Fstatic%2F","Referer":"https://m.siyixs.com/"};
body="submit=&keyword="+key;
op={
"method": "get",
"body": body,
        "charset": "UTF-8",
        "headers": JSON.stringify(head)
};
myurl=url+"/search/";
path=java.post(myurl,body,head).header("Location");
java.log(path);
url+path+","+JSON.stringify(op);
</js>

台湾小说网繁体字搜索时编码问题
搜索地址：
<js>
url="https://m.xsw.tw/modules/article/wap_search.php,";
key=java.s2t(key);
option={
  "body":`searchkey=${key}`,
  "charset":"big5",
  "method":"POST"
}
url+JSON.stringify(option)
</js>
新版阅读适用
---------------------------------
解决搜索30秒的办法，在基本页里登录检查Js里填上
cookie.removeCookie(source.getKey())
result
或者在搜索地址栏清空cookie写法如下
{{cookie.removeCookie(source.getKey())}}
/search0f.html?searchkey={{key}}
---------------------------------
搜索地址经常变动的解决办法
感谢 虚空大梦 大佬提供的方法
//通过ajax加载基本页的网址,然后提取form标签里的action的值,然后后面再跟着?searchkey={{key}}参数
{{java.ajax(source.getKey()).match(/action="(.*?)"/)[1]}}?searchkey={{key}}
或者用这个来获取搜索地址会变动的
案例网址:http://www.iqb8.cc
@js:
var url=source.getKey();
var html = java.ajax(url);
so = org.jsoup.Jsoup.parse(html).select('form[name=t_frmsearch]').attr('action');
url+so+","+JSON.stringify({
  "body": "searchkey={{key}}",
  "method": "post"
})
…………………………
搜索规则下的搜索链接第一页和第二页的网址不同可以这样写:
以下是非js正则的发现规则列表第二页和第一页格式不同的写法
①第一页https://qdjjj9.net/gudai/
②第二页https://qdjjj9.net/gudai/index_2.html
可写成
/{{page==1?"":page+".html"}}

https://qdjjj9.net/gudai/{{page==1?'':'index_'+page+'.html'}}
具体看阅读帮助文档page相关的:
<,{{page}}>
还有种第一页是这样的
https://11111.com/搜索/关键字
第二页是这样的
https://11111.com/搜索/关键字/2.html
这个情况可以这样写
https://11111.com/搜索/关键字<,/{{page}}.html>

发现页第一页和第二页网址不同案例
http://dmxs.org/book/index_{{page}}.html
或
http://dmxs.org/book/<,index_{{page}}.html>
--------------------------------
搜索栏下目录列表多个的处理方法
案例一:https://m.bookb.net/
它的搜索列表有两个
<div class="recommend mybook">
//目录1
<div class="hot_sale ">...</div>
//目录2
<div class="hot_sale hot_saleEm">...</div>
</div>
处理办法用div.hot_sale取它的class名字的共通处

案例二:http://www.bookshuku.info/
这是个电脑端的网站,它的搜索页也是两个列表,一个是书籍名字,一个是书籍分类想都取到可以这样傻瓜式写法
//解释一下,就是取id是searchmain的下面的所有的div标签,然后not(@class="searchResult")就是排除不要这个class是searchResult的标签然后用and连接多个排除条件剩下的就是我们想要的
//div[@id="searchmain"]//div[not(@class="searchResult") and not(@class="mainNextPage") and not(@class="searchIntro")]
--------------------------------

作者规则写法
###在这里的作用是只保留###前面的内容,全部写法为##要替换提取的内容或者正则##从前面内容中提取并仅保留的内容或者正则其他内容都抛弃###
tag.a@text##作者：([^"]+)"##$1###
或者
.info@text##作者：(.*?) ##$1###
或者
##作者[:：]([^<]+)<##$1###
或者
##作者：([^<]+)<##$1###

书籍详情页规则URL
tag.a.1@href@js:'https://www.x7773xs.com'+result
或者
tag.a@href@js:"https://www.wan888ntxt.com/"+result+"/"
或者
tag.a@href##$##,{"headers":{
	"Referer":"https://bo454lf.html5.qq.com/kdread/adread/chapter"
	}}
或者
//意思就是在这个a的href属性获得的地址前面加上这##后面的内容
tag.a@href##^##https://whts.com
或者
tag.a@href@js:"https://xxx.com"+result
或者
//意思就是在这个a的href属性获得的地址后面加上这##后面的内容
tag.a@href##$##/sadly_1.html
或者
//前面这段一直到href是获取详情页地址，后面一段的js的具体作用是把获取到的详情页地址里面的www……替换成后面的k……
tag.a.0@href@js:result.replace('www.yexia77ge','k.yexia77ge')
或者
//当前页的url
{{baseUrl}}

详情页或者搜索页分类规则写法
在正文里面找到相关内容然后用双大括号加上双@来写内容,这里的双@有时候也可能是$..比如说json的文件的写法
{{@@.info@text##类型：(.*?) ##$1###}},{{@@.status@text}}

……………………………………
详情页的书名规则写法
[property$=book_name]@content

详情页的作者规则写法
[property$=author]@content

详情页的分类规则写法
~符号在这里的作用是一次性获取property的category|status|update_time三个属性.功能有点类似&&
[property~=category|status|update_time]@content##\s.*
或者
[property~=category|status|update_time]@content##\s\d.*

详情页字数拼接的写法
{{@@#csount span.1@text}}字
或者
class.xxx@tag.a@text##$##万字
或者
.book_box@html##字数[：:](.+?)\<##$1###
或者
{{@@text.字数@text##字数：}}##W##万字

详情页最新章节写法
[property$=latest_chapter_name]@content##正文卷.|正文.|VIP章节.|免费章节.|VIP卷.|默认卷.|章节目录.|最新章节.|[\(（【].*?[求更票谢乐发订合补加].*?[】）\)]

或者
.book_update:contains(最新章节：) > a@text
##[\(（【].*?[求更谢乐发订合补加].*?[】）\)]|^章节目录\s*

或者
//前后文字段拼接中间以▪️符号隔开，这个符号也可以用其他任意内容代替
{{@@li.1@text}}▪️{{@@li.3@text}}

或者
.block_txt2@p.6:5@text##最新：(.*)\s更新：20(.*)##$1▪️$2

或者
a.0@href<js>java.ajax('http://www.fenghuaju.com'+result)</js>
class.diswap@p.-1@text&&class.diswap@p.-2@text##最后更新：|最新章节：|直达底部
<js>result.replace(/(.*)\s/,'$1 • ')</js>
<js>result.replace(/\s\d+:\d+:\d+/,'')</js>
<js>result.replace(/^(正文|VIP章节|最新章节)?(\s+|_)|[\(\{（｛【].*[求更谢乐发推票盟补加字Kk\/].*[\)\}）｝】]/g,'')</js>

或者
{{@@[property$=chapter_name]@content}} • {{@@[property$=update_time]@content##\s.*}}

详情页的简介规则写法
[property$=description]@content##(^|[。！？]+[”」）】]?)##$1<br>

或者
.book_intro:contains(简介：)@textNodes
##(^|[。！？]+[”」）】]?)##$1<br>
<js>result</js>##\s*（[^）]*本书网址[^）]*）\s*

详情页的封面规则写法
[property$=image]@content

详情页的目录URL规则写法
//这个比较特殊，有的网站的目录跟详情页是在一起的，但是排序可能是反的,这与某些网站用 text.阅读@href 来得到正确的目录页作用一样，能更简单的把目录列表显示出来为最佳选择
text.[正序]@href
或者
text.阅读@href

搜索栏目下的封面规则:
tag.a.1@href##.*/(\d+)(\d{3})/##https://www.rouziwu.info/files/article/image/$1/$1$2/$1$2s.jpg

或者
a@href##.*/book/(\d+)/##https://imghhhxiaoshuocom.cdn.bcebos.com/img/$1.jpg

搜索栏下的封面规则通过jax跨页面加载写法
a.0@href<js>java.ajax("补全缺失的网址"+result)</js>class.pic@img@src

搜索栏下的图片破防盗链
img@data-src@js:
headers={"headers":{"Referer":baseUrl}}
result+','+JSON.stringify(headers)

搜索栏下的章节规则拼接并净化垃圾话
.tabcontent@class.tabvalue.1@tag.td.2@text&&
.tabcontent@class.tabvalue.1@tag.td.1@text&&
.tabcontent@class.tabvalue.1@tag.td.0@text##最后更新：|连载状态：|作品分类：


封面图的另一种写法
class.zp@tag.a@href<js>
var id = result.match(/(\d+)\/?$/)[1];
var iid = parseInt(id/1000);
'https://www.qljgh5.tw/files/article/image/'+iid+'/'+id+'/'+id+'s.jpg';
</js>

或者
tag.a@href<js>
var id = result.match(/(\d+)\/?$/)[1];
var iid = parseInt(id/1000);
'https://www.bequgexs.com/files/article/image/'+iid+'/'+id+'/'+id+'s.jpg';
</js>

或者
a.0@href##.*/(\d+)/##$1
@js:
n=result
m=parseInt(result/1000)
"https://fm.pomoxs.com/"+m+"/"+n+"/"+n+"s.jpg"

文字内容不需要左右的[]括号可以这样写:
tag.a.0@text##\[|\]

目录页的章节名去垃圾话
text##正文\s|[\(（【].*?[求更票谢乐发订合补加].*?[】）\)]

章节名称通用替换规则:
dd@text##[\(（【].*?[求更谢乐发订合补加].*?[】）\)]

或者
tag.a@text@js:result.replace(/[（［【\{\(].*?[更合求票赏鲜盟修推歉谢祝节年].*?[）］】\}\)]/,"")
或者
//去除双第N章的章字样，2留1
tag.a@text##第.*?章\s?(第.*?章)(.*$)##$1 $2
…………………………
章节URL特殊情况onclick="window.open处理
onclick##'([^']+)##$1###<js>
unescape(result.replace(/\\u/g,'%u'));
</js>
应对的情况
<ul>
<li>
<el-tag onclick="window.open('/chapter/235/235310/86363147.\u0068\u0074\u006d\u006c','_self')">503、王传贞（2/2）
</el-tag>
</li>

或者用这个
#next_url@onclick##.*?'([^']+\.).*##$1html

或者用这个
table[onclick~=bookinfo]@onclick
##'([^']+)'##$1###
应对的情况如下：
<table onclick="window.location.href='http://wap.bookshuku.info/bookinfo/95807.html">

章节目录另一个写法
书名所在的a标签，也可以这样写范围，a[href^=/move/]，这说的是以href中/move/开头的a标签，^是开头的意思，$是结尾的意思，~是当中有的意思

…………………………

章节URL规则适用于动态加载的网页:
tag.a@href@js:result+',{webView:“true”}'
或者
tag.a@href##$##,{'webView':true}

章节URL取到地址进行拼接的
tag.a@href##/(.*?)/(.*?).html##https://www.wanben8888txt.net/api/api.php,{
  "charset": "gbk",
  "method": "POST",  "body":"action=read&id=$1&cid=$2&token="
}
或者
tag.a@href@js:'https://www.8k55ana.com/book/'+result+'.html'
或者
用这个方法取当前详情页的URL来做拆分拼接
//取当前链接里的数字，然后带入新的链接里面去
@js:var bid = baseUrl.match(/\d+/);
java.put('bid', bid);
'https://uk.reade5455r.qq.com/book-read/'+bid+'/{{$.seq}}'

详情页目录地址加请求头案例
/b/{{baseUrl.match(/(\d+)/)[1]}}/more,{"headers":{"x-requested-with":"XMLHttpRequest"}}
——————
详情页的目录URL规则(目录和详情页不在一页可以这么写)
这里的{{$.}}代表的是详情页当前的地址,后面的list.html是目录的地址比详情页多出来的一段地址
{{$.}}list.html
﹉﹉﹉﹉
★详情页+目录页+正文第一章显示在一页的时候的处理方法:
章节名写法
//具体到它的分页显示比如:首页 2/22 下一页 尾页
a.0@text##(\d+)\/\d+##第$1页
其他地方获取内容正常获取，就是在目录页里面的章节URL规则里面这样写:
//意思是跟目录页共用一页作为第一章的网址
{{baseUrl}}

或者
就不填目录链接，目录列表可以填tag.html或tag.body等，章节名称tag.title@text，章节链接填href（获取不到链接，正文就会直接用详情页链接）或者章节链接留空
反正就是要有一个列表能获取到章节名称就行
﹉﹉﹉﹉﹉

简介通用替换规则:
class.intro_info@textNodes##(^|[。！？]+[”」）】]?)##$1<br>
或者
[property$=description]@content##(^|[。！？]+[”」）】]?)##$1<br>


目录下一页规则
//适用于目录列表在详情页属于隐藏标签的
option@value
或者并发加载，多个隐藏按钮一起打开 [name=pageselect] > option!0@value


………………
目录下一页拼接写法(第1/30页)当前20条/页,第一页网址https://www.yipinxia.co/43/43579/
第二页网址https://www.yipinxia.co/43/43579_2/

##\(第1\/(\d+)页\)当前##$1###
<js>
n=result;
base=String(baseUrl).replace(/\/$/,'');
for(i=2,list=[];i<=n;i++){list.push(base+"_"+i+"/")}
list
</js>
………………
目录列表规则写法
从id.list开始一直找到tag.dd标签然后把tag.dd的最上面9个排除，因为！号后面的0代表数字1后面的每个数字都是同理加上1算实际对的第几个章节目录
id.list@tag.dl@tag.dd[!0:8]
//排除第1个到第9个,因为默认从0开始计算
或者
id.list@tag.dl@tag.dd[0:8]
//只要第1个到第9个,因为默认从0开始计算
或者
id.list@tag.dl@tag.dd!0:1:2:3:4:5:6:7:8



目录标签下的目录列表规则
//找div标签里面id是lbks的底下的dl标签下的最后一个dt标签后面的与dt标签同级标签里面找dd标签下的a标签
//#lbks > dl > dt:nth-of-type(2) ~ dd > a
//div[@id="lbks"]/dl/dt[last()]/following-sibling::dd/a
案列:
<div id="lbks"><dl><dt>最新8章节(倒叙)，如果喜欢可以把穿越万界：神功自动满级放到书架里面随时观看</dt><dd><a href="/shoujixs_167907_44533846.html">第996章 古之名将</a></dd><dd><a href="/shoujixs_167907_44533845.html">第995章 包拯</a></dd><dd><a href="/shoujixs_167907_44533844.html">第994章 丢了一魄的宁采臣</a></dd><dd><a href="/shoujixs_167907_44533843.html">第993章 移山术满级</a></dd><dd><a href="/shoujixs_167907_44533624.html">第992章 踏足枉死城</a></dd><dd><a href="/shoujixs_167907_44532919.html">第991章 玩家的求助帖</a></dd><dd><a href="/shoujixs_167907_44531951.html">第990章 一计不成又生一计</a></dd><dd><a href="/shoujixs_167907_44524032.html">第989章 损耗</a></dd><dt>正文</dt><dd><a href="/shoujixs_167907_41554242.html">第1章 全能王者！瞬间满级</a></dd><dd><a href="/shoujixs_167907_41554243.html">第2章 玩家广场热议综合排名第一人</a></dd><dd><a href="/shoujixs_167907_41554244.html">第3章 东汉末年冀州阵营</a></dd><dd><a href="/shoujixs_167907_41554245.html">第4章 成就勋章</a></dd><dd><a href="/shoujixs_167907_41555507.html">第5章 高览</a></dd><dd><a href="/shoujixs_167907_41569074.html">第6章 高阶刀法</a></dd><dd><a href="/shoujixs_167907_41569076.html">第7章 沙场刀诀</a></dd>


听书源的正文写法
正文规则
<js>result</js>
资源正则
.*\.(mp3|m4a).*

正文去两段中文中间的空格
##([\u4e00-\u9fa5])[ ]+([\u4e00-\u9fa5])##$1$2

正文去重复章节名
id.contents@html
<js>
a=title.replace(/第.*章\s*/,'第.*章')
b=new RegExp(a,'g')
result.replace(b,'')
</js>

或者
书源正文规则后面添加 ##{{chapter.title}}
可去除章节名称
或者
##\s*{{chapter.title}}(\s)?\(第\d\/\d页\)\s*
用于去除:章节名 (第1/3页)
或者
<js>
rep='\\s*'+String(book.durChapterTitle.replace(/[^\\u4e00-\\u9fa5\d]/g,'')).split('').toArray().join('[^\\u4e00-\\u9fa5]{0,2}?')+'\\s*';
reg=new RegExp(rep,'gi');
result.replace(reg,'');
</js>

或者
<js>
rep='\\s*'+book.durChapterTitle.replace(/[^\\u4e00-\\u9fa5\d]/g,'').replace(/\u3002|\uff1f|\uff01|\uff0c|\u3001|\uff1b|\uff1a|\u201c|\u201d|\u2018|\u2019|\uff08|\uff09|\u300a|\u300b|\u3010|\u3011|\u007e
/g,'').split('').join('[\s\S]{0,2}?')+'\\s*';
reg=new RegExp(rep,'gi');
result.replace(reg,'');
</js>

或者
<js>
rep='\\s*'+book.durChapterTitle.replace(/((?=[\x21-\x7e]+)[^A-Za-z0-9])|[\u3002\uff1b\uff0c\uff1a\u201c\u201d\uff08\uff09\u3001\uff1f\u300a\u300b’]/g,'').split('').join('[\\s\\S]{0,2}?')+'\\s*';
reg=new RegExp(rep,'gi');
result.replace(reg,'');
</js>

正文去章节名2
##{{chapter.title}}
或者
##{{book.durChapterTitle}}


目录下一页以文字拆链接拼接网址
#pagestats@textNodes
@js:var go = result[0];
var page = go.match(/(\d+)/) [1];
var list = [];
for (var i = 2; i <= page; i++) {
  list.push(baseUrl.replace(/1\/asc/, i + '/asc'));
}
list;

正文下一页写法1
if (result.indexOf("next.png") > -1) {
mat = baseUrl.match(/\/\d+(_(\d+))?\.html/);
page = Number(mat[2]||1)+1;
baseUrl.replace(/\/(\d+)(_(\d+))?.html/,'/$1_'+page+'.html');
}

正文下一页写法2
:contains(下一章)@href##(^.*_\d+.*$|^)##$1###

正文下一页写法3
text.【.*】@href
//它用于正文下一页是这样的:【1】【2】【3】【4】……等等之类以中文括号括起来的下一页

正文下一页写法(拼接网址)
<js>
var list=[];
if(n=result.match(/\/(\d+)页/)){
for(var i=2;i<=n[1];i++){list.push(baseUrl.replace(/\/$/,"_"+i+"/"))
}}list</js>

或者
text.尾页@href
@js:
{n=parseInt(result[0].match(/\/(\d+)\.html/)[1]);
list=[];
for(i=2;i<=n;i++)
{list.push(i+".html");}
list}
或者
text.尾页@href
@js:
n=parseInt(result[0].match(/\/(\d+)\.html/)[1]);
list=[];
for(i=2;i<=n;i++)
list.push(i+".html");
list
或者
text.尾页@href
@js:
{var n=parseInt(result[0].match(/\/(\d+)\.html/)[1]);
var list=[];
for(var i=2;i<=n;i++)
{list.push(i+".html");}
list}
或者
text.尾页@href
@js:
n=parseInt(result[0].match(/\/(\d+)\.html/)[1]);
list=[];
for(i=2;i<=n;i++)
list.push(baseUrl+i+".html");
list
或者
text.尾页@href
@js:
var n=parseInt(result[0].match(/\/(\d+)\.html/)[1]);
var list=[];
for(var i=2;i<=n;i++)
{list.push(baseUrl+i+".html");}
list
或者
@js:
{var n=parseInt(java.ajax(baseUrl).match(/\>(\d+)\<\/span\>页\)当前/)[1]);
var list=[];
for(var i=2;i<=n;i++)
{list.push(i+".html");}
list}
或者
@js:
var n=parseInt(java.ajax(baseUrl).match(/\>(\d+)\<\/span\>页\)当前/)[1]);
var list=[];
for(var i=2;i<=n;i++)
list.push(i+".html");
list
或者
@js:
n=parseInt(java.ajax(baseUrl).match(/\>(\d+)\<\/span\>页\)当前/)[1]);
list=[];
for(i=2;i<=n;i++)
{list.push(baseUrl+i+".html");}
list
或者
@js:
{var n=parseInt(java.ajax(baseUrl).match(/\>(\d+)\<\/span\>页\)当前/)[1]);
var list=[];
for(var i=2;i<=n;i++)
{list.push(baseUrl+i+".html");}
list}
或者
@js:if(result.match(/\>\d+\<\/span\>页\)当前/))
{var n=parseInt(result.match(/\>(\d+)\<\/span\>页\)当前/)[1]);
var list=[];
for(var i=2;i<=n;i++)
{list.push(i+".html");}
list}
或者
@js:if(result.match(/\>\d+\<\/span\>页\)当前/))
{var n=parseInt(result.match(/\>(\d+)\<\/span\>页\)当前/)[1]);
var list=[];
var url=baseUrl;
for(var i=2;i<=n;i++)
{list.push(url+i+".html");}
list}
或者
@js:if(result.match(/\>\d+\<\/span\>页\)当前/))
{var n=parseInt(result.match(/\>(\d+)\<\/span\>页\)当前/)[1]);
var list=[];
for(var i=2;i<=n;i++)
{list.push(baseUrl+i+".html");}
list}
或者
text.下一页@href||text.下一頁@href
或者
@js:
if (result.indexOf("nextpage.png") > -1) {
  var code = result.match(/eval\(function(.*)\);/)[0];
  code = code.replace(/u[0-9a-f]+/, 'uData')
  eval(code);
  if(!uData.match('_')) {
	next = java.getElement("@@#pt_next@a")
	uData = next.attr("href")
	}
  uData;
}

或者
##和@js不能同时用，正文规则
要么加上##$##下一页
要么加上@js:result+'下一页'
……………………
正文规则去垃圾话
(?s)\n+[^\n]+下载爱阅小说.+
或者
段落开头几个字加(.|\n)*$或者[\s\S]*
……………………
JSON写法
$.book_author@put{自定义变量：当前页面获取的值}
$.book_author@put:{bid:book_id}

调用的格式是固定的 一定@get:{自定义变量}
这里调用本页的json信息可以用双大括号括起来{{$.book_id}} 里面的book_id就是要取的内容
http://123456.com/{{$.book_id}}_@get:{bid}/1.html
要是通过java打印台打印get数据的时候可以这样写,括号里加引号是针对属于字符串类型,其它类型可不加引号,比如数字类型的
{{java.get("id")}}
或者
@js:
java.get("bid")

正文图片修改headers
let options = {
"headers": {"User-Agent": "xxxx","Referrer":baseUrl,"Cookie":"aaa=vbbb;"}
};
'<img src="'+src+","+JSON.stringify(options)+'">'

漫画源正文
#cp_img@html##src.*\"
@js:result.replace(/data-original/g,"src")
漫画源正文的图片样式
FULL

正文内容多页拼接断句处理办法
可以在替换规则里面这样写
##\s{0,100}\n{0,2}.*(第.*页).*\n{0,2}\s{0,100}

………………
正文匹配重复段落处理办法
//([^\n]+)的意思是匹配任意自然段落的内容.
//  \s*\n\s*的意思是匹配段前段尾出现的空格和换行
// \1的意思是对前面的第一个括号里面匹配的内容进行引用,即与前面括号内匹配到的内容相同.这样就能匹配到所有的连续的重复段落.
正则表达式如下:
([^\n]+)\s*\n\s*\1
替换为
$1
连起来写就是:
xxxx@html##([^\n]+)\s*\n\s*\1##$1
……………………

正文js写法替换广告或者字体
//有多个内容要有替换可以在后面用【.replace(/正则表达式/g,'替换成的内容,想替换为空就留空不填')】
id.ak@html
@js:result
.replace(/<span.class=\"Y_1\"><\/span>/g,'男')
.replace(/<span.class=\"Y_2\"><\/span>/g,'人')

正文末尾去广告
正则：广告XX后面加(.|\n)*$可以屏蔽XX后面的内容
或者开头去广告
正则：^(.|\n)*?广告

正文段落末尾不是符号并下一段落首字是汉字则自动拼接(简单应对翻页段落被拆分)
(?<=[\u4e00-\u9fa5])\n(?=[\u4e00-\u9fa5])

----------------------------
订阅源内容页去除某些不想要的标签
//选择需要删除的标签，以,来分隔.最后一个标签末尾不用填逗号,class用点开头,id用#开头

items = document.querySelectorAll(` 	.post-info-box, 	.navbar-header `) 
//把选择的html值改成空
Array.from(items,(item)=>{ 	item.innerHTML = `` 	item.style.display = `none` })
----------------------------


发现页发现的写法:
[{"title":"❀榜单❀","url":"","style":{"layout_flexBasisPercent":1,"layout_flexGrow":1}}, {"title":"总点击榜","url":"/top_allvisit/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"月点击榜","url":"/top_monthvisit/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"总推荐榜","url":"/top_allvote/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"月推荐榜","url":"/top_monthvote/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"总月票榜","url":"/top_allvipvote/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"总鲜花榜","url":"/top_allflower/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"月勤更榜","url":"/top_monthwords/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"最近更新","url":"/top_lastupdate/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"最新入库","url":"/top_postdate/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"收藏榜","url":"/top_goodnum/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"字数榜","url":"/top_words/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"新书榜","url":"/top_newhot/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"❀分类❀","url":"","style":{"layout_flexBasisPercent":1,"layout_flexGrow":1}}, {"title":"玄幻奇幻","url":"/xuanhuan/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"武侠仙侠","url":"/xianxia/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"都市言情","url":"/dushi/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"穿越架空","url":"/chuanyue/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"女生视觉","url":"/nvsheng/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"精品辣文","url":"/lawen/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}]

```




### 日记第二版,自己折腾自己用
```
阅读书源写法
解决搜索30秒的办法，在基本页里登录检查Js里填上
cookie.removeCookie(source.getKey())
result
或者在搜索地址栏清空cookie写法如下
{{cookie.removeCookie(source.getKey())}}
/search0f.html?searchkey={{key}}

基本页请求头
在里面加referer信息破网站防盗链，比如在A网站里面的B链接地址，要是正常访问B链接它会自动跳回到A网站，那么在请求头里面带上'referer':A网站,有可能可以破除它的防盗链
{
'referer':'https://official.bkvvvvv.com/'
}
或者
{"referer":"https://mjjxs.net"}
或者
书源基本页面，请求头，@js:JSON.stringify({"referer":baseUrl})



{'User-Agent':'Mozilla/5.0 (Linux; Android 11; PCAM10 Build/RP1A.200720.011; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/83.0.4103.106 Mobile Safari/537.36'}

请求头
{'User-Agent':'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/534.24 (KHTML, like Gecko) Chrome/71.0.3578.141 Safari/534.24 XiaoMi/MiuiBrowser/12.4.14'}

或者
{
  "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/58.0.3029.110 Safari/537.36"
}

或者
{
 'User-Agent': 'Mozilla/5.0 (Linux; Android 11; Pixel 3 XL Build/RQ3A.211001.001; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/102.0.4988.0 Mobile Safari/537.36 SearchCraft/3.9.2 (Baidu; P1 11) '
}

或者
{"User-Agent": "Mozilla/5.0 (Linux; Android 12; M2011K2C Build/SKQ1.211006.001; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/102.0.5005.99 Mobile Safari/537.36 T7/12.16 SearchCraft/3.9.1 (Baidu; P1 11)"}

或者
{'User-Agent':'Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/86.0.4240.198 Mobile Safari/537.36',
"Referer":"http://m.b777777.com/"}

或者
{
	"User-Agent":"Mozilla/5.0 (Linux; Android 12; Nexus 5X Build/NRD90M); wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/96.0.4664.104 Mobile Safari/537.36"
}

或者请求头
{
  "User-Agent": "Mozilla/5.0 (Windows; U; Windows NT 5.2;. en-US) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/78.0.3904.108 Safari/537.36 Quark/4.6.2.161"
}


或者
{"User-Agent": "Mozilla/5.0 (Linux; Android 11) Mobile Safari/537.36"}

或者
{'webView': true,"header":{"referer":"https://mjjxs.net"}}

URL规则后面加上Java.log查看获取页面调试结果用的
tag.a@href<js>java.log(result)</js>
或者这样写
tag.a@href@js:java.log(result)

跨栏目存取数据
比如在搜索栏的书名里面存了个id这里的@put:{id:$.Id}就是存储数据，括号里的id是名字，:后面的是它要存的内容公式字符等等
Name@put:{id:$.Id}
然后到目录页里面的章节url里面调用它，这里的@get:{id}就是调用前面存储的数据
https://conhhs.pggfggi.com/BookFiles/Html/@get:{cid}/@get:{id}/{{$.id}}.html


搜索规则下的搜索链接第一页和第二页的网址不同可以这样写:
以下是非js正则的发现规则列表第二页和第一页格式不同的写法
①第一页https://qdjjj9.net/gudai/
②第二页https://qdjjj9.net/gudai/index_2.html
可写成
https://qdjjj9.net/gudai/{{page==1?'':'index_'+page+'.html'}}
具体看阅读帮助文档page相关的:
<,{{page}}>
还有种第一页是这样的
https://11111.com/搜索/关键字
第二页是这样的
https://11111.com/搜索/关键字/2.html
这个情况可以这样写
https://11111.com/搜索/关键字<,/{{page}}.html>

作者规则写法
###在这里的作用是只保留###前面的内容,全部写法为##要替换提取的内容或者正则##从前面内容中提取并仅保留的内容或者正则其他内容都抛弃###
tag.a@text##作者：([^"]+)"##$1###
或者
.info@text##作者：(.*?) ##$1###
或者
##作者[:：]([^<]+)<##$1###

书籍详情页规则URL
tag.a.1@href@js:'https://www.x7773xs.com'+result
或者
tag.a@href@js:"https://www.wan888ntxt.com/"+result+"/"
或者
tag.a@href##$##,{"headers":{
	"Referer":"https://bo454lf.html5.qq.com/kdread/adread/chapter"
	}}
或者
//意思就是在这个a的href属性获得的地址前面加上这##后面的内容
tag.a@href##^##https://whts.com
或者
//意思就是在这个a的href属性获得的地址后面加上这##后面的内容
tag.a@href##$##/sadly_1.html
或者
//前面这段一直到href是获取详情页地址，后面一段的js的具体作用是把获取到的详情页地址里面的www……替换成后面的k……
tag.a.0@href@js:result.replace('www.yexia77ge','k.yexia77ge')
或者
//当前页的url
{{baseUrl}}

详情页或者搜索页分类规则写法
在正文里面找到相关内容然后用双大括号加上双@来写内容,这里的双@有时候也可能是$..比如说json的文件的写法
{{@@.info@text##类型：(.*?) ##$1###}},{{@@.status@text}}

……………………………………
详情页的书名规则写法
[property$=book_name]@content

详情页的作者规则写法
[property$=author]@content

详情页的分类规则写法
~符号在这里的作用是一次性获取property的category|status|update_time三个属性.功能有点类似&&
[property~=category|status|update_time]@content##\s.*
或者
[property~=category|status|update_time]@content##\s\d.*

详情页字数拼接的写法
{{@@#csount span.1@text}}字
或者
class.xxx@tag.a@text##$##万字

详情页最新章节写法
[property$=latest_chapter_name]@content##正文卷.|正文.|VIP章节.|免费章节.|VIP卷.|默认卷.|章节目录.|最新章节.|[\(（【].*?[求更票谢乐发订合补加].*?[】）\)]

或者
.book_update:contains(最新章节：) > a@text
##[\(（【].*?[求更谢乐发订合补加].*?[】）\)]|^章节目录\s*

或者
//前后文字段拼接中间以▪️符号隔开，这个符号也可以用其他任意内容代替
{{@@li.1@text}}▪️{{@@li.3@text}}

或者
.block_txt2@p.6:5@text##最新：(.*)\s更新：20(.*)##$1▪️$2

或者
a.0@href<js>java.ajax('http://www.fenghuaju.com'+result)</js>
class.diswap@p.-1@text&&class.diswap@p.-2@text##最后更新：|最新章节：|直达底部
<js>result.replace(/(.*)\s/,'$1 • ')</js>
<js>result.replace(/\s\d+:\d+:\d+/,'')</js>
<js>result.replace(/^(正文|VIP章节|最新章节)?(\s+|_)|[\(\{（｛【].*[求更谢乐发推票盟补加字Kk\/].*[\)\}）｝】]/g,'')</js>

或者
{{@@[property$=chapter_name]@content}} • {{@@[property$=update_time]@content##\s.*}}

详情页的简介规则写法
[property$=description]@content##(^|[。！？]+[”」）】]?)##$1<br>

或者
.book_intro:contains(简介：)@textNodes
##(^|[。！？]+[”」）】]?)##$1<br>
<js>result</js>##\s*（[^）]*本书网址[^）]*）\s*

详情页的封面规则写法
[property$=image]@content

详情页的目录URL规则写法
//这个比较特殊，有的网站的目录跟详情页是在一起的，但是排序可能是反的,这与某些网站用 text.阅读@href 来得到正确的目录页作用一样，能更简单的把目录列表显示出来为最佳选择
text.[正序]@href
或者
text.阅读@href

搜索栏目下的封面规则:
tag.a.1@href##.*/(\d+)(\d{3})/##https://www.rouziwu.info/files/article/image/$1/$1$2/$1$2s.jpg

或者
a@href##.*/book/(\d+)/##https://imghhhxiaoshuocom.cdn.bcebos.com/img/$1.jpg

搜索栏下的封面规则通过jax跨页面加载写法
a.0@href<js>java.ajax("补全缺失的网址"+result)</js>class.pic@img@src

搜索栏下的章节规则拼接并净化垃圾话
.tabcontent@class.tabvalue.1@tag.td.2@text&&
.tabcontent@class.tabvalue.1@tag.td.1@text&&
.tabcontent@class.tabvalue.1@tag.td.0@text##最后更新：|连载状态：|作品分类：


封面图的另一种写法
class.zp@tag.a@href<js>
var id = result.match(/(\d+)\/?$/)[1];
var iid = parseInt(id/1000);
'https://www.qljgh5.tw/files/article/image/'+iid+'/'+id+'/'+id+'s.jpg';
</js>

或者
tag.a@href<js>
var id = result.match(/(\d+)\/?$/)[1];
var iid = parseInt(id/1000);
'https://www.bequgexs.com/files/article/image/'+iid+'/'+id+'/'+id+'s.jpg';
</js>

文字内容不需要左右的[]括号可以这样写:
tag.a.0@text##\[|\]

目录页的章节名去垃圾话
text##正文\s|[\(（【].*?[求更票谢乐发订合补加].*?[】）\)]

章节名称通用替换规则:
dd@text##[\(（【].*?[求更谢乐发订合补加].*?[】）\)]

或者
tag.a@text@js:result.replace(/[（［【\{\(].*?[更合求票赏鲜盟修推歉谢祝节年].*?[）］】\}\)]/,"")
或者
//去除双第N章的章字样，2留1
tag.a@text##第.*?章\s?(第.*?章)(.*$)##$1 $2
…………………………
章节URL特殊情况onclick="window.open处理
onclick##'([^']+)##$1###<js>
unescape(result.replace(/\\u/g,'%u'));
</js>
应对的情况
<ul>
<li>
<el-tag onclick="window.open('/chapter/235/235310/86363147.\u0068\u0074\u006d\u006c','_self')">503、王传贞（2/2）
</el-tag>
</li>

或者用这个
#next_url@onclick##.*?'([^']+\.).*##$1html
…………………………

章节URL规则适用于动态加载的网页:
tag.a@href@js:result+',{webView:“true”}'
或者
tag.a@href##$##,{'webView':true}

章节URL取到地址进行拼接的
tag.a@href##/(.*?)/(.*?).html##https://www.wanben8888txt.net/api/api.php,{
  "charset": "gbk",
  "method": "POST",  "body":"action=read&id=$1&cid=$2&token="
}
或者
tag.a@href@js:'https://www.8k55ana.com/book/'+result+'.html'
或者
用这个方法取当前详情页的URL来做拆分拼接
//取当前链接里的数字，然后带入新的链接里面去
@js:var bid = baseUrl.match(/\d+/);
java.put('bid', bid);
'https://uk.reade5455r.qq.com/book-read/'+bid+'/{{$.seq}}'

详情页目录地址加请求头案例
/b/{{baseUrl.match(/(\d+)/)[1]}}/more,{"headers":{"x-requested-with":"XMLHttpRequest"}}

﹉﹉﹉﹉
★详情页+目录页+正文第一章显示在一页的时候的处理方法:
章节名写法
//具体到它的分页显示比如:首页 2/22 下一页 尾页
a.0@text##(\d+)\/\d+##第$1页
其他地方获取内容正常获取，就是在目录页里面的章节URL规则里面这样写:
//意思是跟目录页共用一页作为第一章的网址
{{baseUrl}}

或者
就不填目录链接，目录列表可以填tag.html或tag.body等，章节名称tag.title@text，章节链接填href（获取不到链接，正文就会直接用详情页链接）或者章节链接留空
反正就是要有一个列表能获取到章节名称就行
﹉﹉﹉﹉﹉

简介通用替换规则:
class.intro_info@textNodes##(^|[。！？]+[”」）】]?)##$1<br>
或者
[property$=description]@content##(^|[。！？]+[”」）】]?)##$1<br>


目录下一页规则
//适用于目录列表在详情页属于隐藏标签的
option@value
或者并发加载，多个隐藏按钮一起打开 [name=pageselect] > option!0@value

目录列表规则写法
从id.list开始一直找到tag.dd标签然后把tag.dd的最上面9个排除，因为！号后面的0代表数字1后面的每个数字都是同理加上1算实际对的第几个章节目录
id.list@tag.dl@tag.dd[!0:8]
或者
id.list@tag.dl@tag.dd!0:1:2:3:4:5:6:7:8

目录标签下的目录列表规则
//找div标签里面id是lbks的底下的dl标签下的最后一个dt标签后面的与dt标签同级标签里面找dd标签下的a标签
//div[@id="lbks"]/dl/dt[last()]/following-sibling::dd/a
案列:
<div id="lbks"><dl><dt>最新8章节(倒叙)，如果喜欢可以把穿越万界：神功自动满级放到书架里面随时观看</dt><dd><a href="/shoujixs_167907_44533846.html">第996章 古之名将</a></dd><dd><a href="/shoujixs_167907_44533845.html">第995章 包拯</a></dd><dd><a href="/shoujixs_167907_44533844.html">第994章 丢了一魄的宁采臣</a></dd><dd><a href="/shoujixs_167907_44533843.html">第993章 移山术满级</a></dd><dd><a href="/shoujixs_167907_44533624.html">第992章 踏足枉死城</a></dd><dd><a href="/shoujixs_167907_44532919.html">第991章 玩家的求助帖</a></dd><dd><a href="/shoujixs_167907_44531951.html">第990章 一计不成又生一计</a></dd><dd><a href="/shoujixs_167907_44524032.html">第989章 损耗</a></dd><dt>正文</dt><dd><a href="/shoujixs_167907_41554242.html">第1章 全能王者！瞬间满级</a></dd><dd><a href="/shoujixs_167907_41554243.html">第2章 玩家广场热议综合排名第一人</a></dd><dd><a href="/shoujixs_167907_41554244.html">第3章 东汉末年冀州阵营</a></dd><dd><a href="/shoujixs_167907_41554245.html">第4章 成就勋章</a></dd><dd><a href="/shoujixs_167907_41555507.html">第5章 高览</a></dd><dd><a href="/shoujixs_167907_41569074.html">第6章 高阶刀法</a></dd><dd><a href="/shoujixs_167907_41569076.html">第7章 沙场刀诀</a></dd>


听书源的正文写法
正文规则
<js>result</js>
资源正则
.*\.(mp3|m4a).*


正文去重复章节名
id.contents@html
<js>
a=title.replace(/第.*章\s*/,'第.*章')
b=new RegExp(a,'g')
result.replace(b,'')
</js>

或者
书源正文规则后面添加 ##{{chapter.title}}
可去除章节名称

或者
<js>
rep='\\s*'+String(book.durChapterTitle.replace(/[^\\u4e00-\\u9fa5\d]/g,'')).split('').toArray().join('[^\\u4e00-\\u9fa5]{0,2}?')+'\\s*';
reg=new RegExp(rep,'gi');
result.replace(reg,'');
</js>

或者
<js>
rep='\\s*'+book.durChapterTitle.replace(/[^\\u4e00-\\u9fa5\d]/g,'').replace(/\u3002|\uff1f|\uff01|\uff0c|\u3001|\uff1b|\uff1a|\u201c|\u201d|\u2018|\u2019|\uff08|\uff09|\u300a|\u300b|\u3010|\u3011|\u007e
/g,'').split('').join('[\s\S]{0,2}?')+'\\s*';
reg=new RegExp(rep,'gi');
result.replace(reg,'');
</js>

或者
<js>
rep='\\s*'+book.durChapterTitle.replace(/((?=[\x21-\x7e]+)[^A-Za-z0-9])|[\u3002\uff1b\uff0c\uff1a\u201c\u201d\uff08\uff09\u3001\uff1f\u300a\u300b’]/g,'').split('').join('[\\s\\S]{0,2}?')+'\\s*';
reg=new RegExp(rep,'gi');
result.replace(reg,'');
</js>

正文下一页写法1
if (result.indexOf("next.png") > -1) {
mat = baseUrl.match(/\/\d+(_(\d+))?\.html/);
page = Number(mat[2]||1)+1;
baseUrl.replace(/\/(\d+)(_(\d+))?.html/,'/$1_'+page+'.html');
}

正文下一页写法2
:contains(下一章)@href##(^.*_\d+.*$|^)##$1###

正文下一页写法(拼接网址)
<js>
var list=[];
if(n=result.match(/\/(\d+)页/)){
for(var i=2;i<=n[1];i++){list.push(baseUrl.replace(/\/$/,"_"+i+"/"))
}}list</js>

或者
text.尾页@href
@js:
{n=parseInt(result[0].match(/\/(\d+)\.html/)[1]);
list=[];
for(i=2;i<=n;i++)
{list.push(i+".html");}
list}
或者
text.尾页@href
@js:
n=parseInt(result[0].match(/\/(\d+)\.html/)[1]);
list=[];
for(i=2;i<=n;i++)
list.push(i+".html");
list
或者
text.尾页@href
@js:
{var n=parseInt(result[0].match(/\/(\d+)\.html/)[1]);
var list=[];
for(var i=2;i<=n;i++)
{list.push(i+".html");}
list}
或者
text.尾页@href
@js:
n=parseInt(result[0].match(/\/(\d+)\.html/)[1]);
list=[];
for(i=2;i<=n;i++)
list.push(baseUrl+i+".html");
list
或者
text.尾页@href
@js:
var n=parseInt(result[0].match(/\/(\d+)\.html/)[1]);
var list=[];
for(var i=2;i<=n;i++)
{list.push(baseUrl+i+".html");}
list
或者
@js:
{var n=parseInt(java.ajax(baseUrl).match(/\>(\d+)\<\/span\>页\)当前/)[1]);
var list=[];
for(var i=2;i<=n;i++)
{list.push(i+".html");}
list}
或者
@js:
var n=parseInt(java.ajax(baseUrl).match(/\>(\d+)\<\/span\>页\)当前/)[1]);
var list=[];
for(var i=2;i<=n;i++)
list.push(i+".html");
list
或者
@js:
n=parseInt(java.ajax(baseUrl).match(/\>(\d+)\<\/span\>页\)当前/)[1]);
list=[];
for(i=2;i<=n;i++)
{list.push(baseUrl+i+".html");}
list
或者
@js:
{var n=parseInt(java.ajax(baseUrl).match(/\>(\d+)\<\/span\>页\)当前/)[1]);
var list=[];
for(var i=2;i<=n;i++)
{list.push(baseUrl+i+".html");}
list}
或者
@js:if(result.match(/\>\d+\<\/span\>页\)当前/))
{var n=parseInt(result.match(/\>(\d+)\<\/span\>页\)当前/)[1]);
var list=[];
for(var i=2;i<=n;i++)
{list.push(i+".html");}
list}
或者
@js:if(result.match(/\>\d+\<\/span\>页\)当前/))
{var n=parseInt(result.match(/\>(\d+)\<\/span\>页\)当前/)[1]);
var list=[];
var url=baseUrl;
for(var i=2;i<=n;i++)
{list.push(url+i+".html");}
list}
或者
@js:if(result.match(/\>\d+\<\/span\>页\)当前/))
{var n=parseInt(result.match(/\>(\d+)\<\/span\>页\)当前/)[1]);
var list=[];
for(var i=2;i<=n;i++)
{list.push(baseUrl+i+".html");}
list}
或者
text.下一页@href||text.下一頁@href

或者
##和@js不能同时用，正文规则
要么加上##$##下一页
要么加上@js:result+'下一页'
……………………
正文规则去垃圾话
(?s)\n+[^\n]+下载爱阅小说.+

……………………
JSON写法
$.book_author@put{自定义变量：当前页面获取的值}
$.book_author@put:{bid:book_id}

调用的格式是固定的 一定@get:{自定义变量}
这里调用本页的json信息可以用双大括号括起来{{$.book_id}} 里面的book_id就是要取的内容
http://123456.com/{{$.book_id}}_@get:{bid}/1.html
要是通过java打印台打印get数据的时候可以这样写,括号里加引号是针对属于字符串类型,其它类型可不加引号,比如数字类型的
{{java.get("id")}}
或者
@js:
java.get("bid")

漫画源正文
#cp_img@html##src.*\"
@js:result.replace(/data-original/g,"src")
漫画源正文的图片样式
FULL

正文内容多页拼接断句处理办法
可以在替换规则里面这样写
##\s{0,100}\n{0,2}.*(第.*页).*\n{0,2}\s{0,100}

正文末尾去广告
正则：广告XX后面加(.|\n)*$可以屏蔽XX后面的内容
或者开头去广告
正则：^(.|\n)*?广告

发现页发现的写法:
[{"title":"❀榜单❀","url":"","style":{"layout_flexBasisPercent":1,"layout_flexGrow":1}}, {"title":"总点击榜","url":"/top_allvisit/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"月点击榜","url":"/top_monthvisit/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"总推荐榜","url":"/top_allvote/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"月推荐榜","url":"/top_monthvote/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"总月票榜","url":"/top_allvipvote/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"总鲜花榜","url":"/top_allflower/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"月勤更榜","url":"/top_monthwords/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"最近更新","url":"/top_lastupdate/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"最新入库","url":"/top_postdate/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"收藏榜","url":"/top_goodnum/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"字数榜","url":"/top_words/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"新书榜","url":"/top_newhot/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"❀分类❀","url":"","style":{"layout_flexBasisPercent":1,"layout_flexGrow":1}}, {"title":"玄幻奇幻","url":"/xuanhuan/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"武侠仙侠","url":"/xianxia/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"都市言情","url":"/dushi/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"穿越架空","url":"/chuanyue/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"女生视觉","url":"/nvsheng/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}, {"title":"精品辣文","url":"/lawen/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}]
```



### 书源日记第一版
```
阅读书源写法
解决搜索30秒的办法，在基本页里登录检查Js里填上
cookie.removeCookie(source.getKey())
result
或者在搜索地址栏清空cookie写法如下
{{cookie.removeCookie(source.getKey())}}
/search0f.html?searchkey={{key}}

基本页请求头
在里面加referer信息破网站防盗链，比如在A网站里面的B链接地址，要是正常访问B链接它会自动跳回到A网站，那么在请求头里面带上'referer':A网站,有可能可以破除它的防盗链
{
'referer':'https://official.bkvvvvv.com/'
}

请求头
{'User-Agent':'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/534.24 (KHTML, like Gecko) Chrome/71.0.3578.141 Safari/534.24 XiaoMi/MiuiBrowser/12.4.14'}

或者
{
 'User-Agent': 'Mozilla/5.0 (Linux; Android 11; Pixel 3 XL Build/RQ3A.211001.001; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/102.0.4988.0 Mobile Safari/537.36 SearchCraft/3.9.2 (Baidu; P1 11) '
}

或者
{"User-Agent": "Mozilla/5.0 (Linux; Android 12; M2011K2C Build/SKQ1.211006.001; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/102.0.5005.99 Mobile Safari/537.36 T7/12.16 SearchCraft/3.9.1 (Baidu; P1 11)"}

或者
{'User-Agent':'Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/86.0.4240.198 Mobile Safari/537.36',
"Referer":"http://m.b777777.com/"}

或者
{
	"User-Agent":"Mozilla/5.0 (Linux; Android 12; Nexus 5X Build/NRD90M); wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/96.0.4664.104 Mobile Safari/537.36"
}

或者请求头2
{
  "User-Agent": "Mozilla/5.0 (Windows; U; Windows NT 5.2;. en-US) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/78.0.3904.108 Safari/537.36 Quark/4.6.2.161"
}

URL规则后面加上Java.log查看获取页面调试结果用的
tag.a@href<js>java.log(result)</js>
或者这样写
tag.a@href@js:java.log(result)

跨栏目存取数据
比如在搜索栏的书名里面存了个id这里的@put:{id:$.Id}就是存储数据，括号里的id是名字，:后面的是它要存的内容公式字符等等
Name@put:{id:$.Id}
然后到目录页里面的章节url里面调用它，这里的@get:{id}就是调用前面存储的数据
https://xonhhs.pggfggi.com/BookFiles/Html/@get:{cid}/@get:{id}/{{$.id}}.html


搜索规则下的搜索链接第一页和第二页的网址不同可以这样写:
以下是非js正则的发现规则列表第二页和第一页格式不同的写法
①第一页https://qdjjj9999.net/gudai/
②第二页https://qdjjj9999.net/gudai/index_2.html
可写成
https://qdjjj9.net/gudai/{{page==1?'':'index_'+page+'.html'}}
具体看阅读帮助文档page相关的:
<,{{page}}>
还有种第一页是这样的
https://11111.com/搜索/关键字
第二页是这样的
https://11111.com/搜索/关键字/2.html
这个情况可以这样写
https://11111.com/搜索/关键字<,/{{page}}.html>

作者规则写法
###在这里的作用是只保留###前面的内容,全部写法为##要替换提取的内容或者正则##从前面内容中提取并仅保留的内容或者正则其他内容都抛弃###
tag.a@text##作者：([^"]+)"##$1###
或者
.info@text##作者：(.*?) ##$1###

书籍详情页规则URL
tag.a.1@href@js:'https://www.x777888883xs.com'+result
或者
tag.a@href@js:"https://www.wan8886688ntxt.com/"+result+"/"
或者
tag.a@href##$##,{"headers":{
	"Referer":"https://bo885454lf.html5.com/kdread/adread/chapter"
	}}
或者
//意思就是在这个a的href属性获得的地址前面加上这##后面的内容
tag.a@href##^##https://whts.com
或者
//意思就是在这个a的href属性获得的地址后面加上这##后面的内容
tag.a@href##$##/sadly_1.html
或者
//前面这段一直到href是获取详情页地址，后面一段的js的具体作用是把获取到的详情页地址里面的www……替换成后面的k……
tag.a.0@href@js:result.replace('www.yea77ge','k.yea77ge')

详情页的分类规则写法
~符号在这里的作用是一次性获取property的category|status|update_time三个属性.功能有点类似&&
[property~=category|status|update_time]@content##\s.*

分类规则写法
在正文里面找到相关内容然后用双大括号加上双@来写内容,这里的双@有时候也可能是$..比如说json的文件的写法
{{@@.info@text##类型：(.*?) ##$1###}},{{@@.status@text}}

详情页的书名规则写法
[property$=book_name]@content

详情页的作者规则写法
[property$=author]@content

详情页最新章节写法
[property$=latest_chapter_name]@content##正文卷.|正文.|VIP章节.|免费章节.|VIP卷.|默认卷.|章节目录.|最新章节.|[\(（【].*?[求更票谢乐发订合补加].*?[】）\)]

或者
//前后文字段拼接中间以▪️符号隔开，这个符号也可以用其他任意内容代替
{{@@li.1@text}}▪️{{@@li.3@text}}

或者
.block_txt2@p.6:5@text##最新：(.*)\s更新：20(.*)##$1▪️$2


详情页的简介规则写法
[property$=description]@content##(^|[。！？]+[”」）】]?)##$1<br>

详情页分类的写法
[property~=category|status|update_time]@content##\s\d.*

详情页字数的写法
{{@@#count span.1@text}}字

详情页最新章节的写法
{{@@[property$=chapter_name]@content}} • {{@@[property$=update_time]@content##\s.*}}

详情页的封面规则写法
[property$=image]@content

详情页的目录URL规则写法
//这个比较特殊，有的网站的目录跟详情页是在一起的，但是排序可能是反的,这与某些网站用 text.阅读@href 来得到正确的目录页作用一样，能更简单的把目录列表显示出来为最佳选择
text.[正序]@href
或者
text.阅读@href

搜索栏目下的封面规则:
tag.a.1@href##.*/(\d+)(\d{3})/##https://www.rouziwu.info/files/article/image/$1/$1$2/$1$2s.jpg

或者
a@href##.*/book/(\d+)/##https://imghhhxiaoshuocom.cdn.bcebos.com/img/$1.jpg

搜索栏下的封面规则通过jax跨页面加载写法
a.0@href<js>java.ajax("补全缺失的网址"+result)</js>class.pic@img@src

搜索栏下的章节规则拼接并净化垃圾话
.tabcontent@class.tabvalue.1@tag.td.2@text&&
.tabcontent@class.tabvalue.1@tag.td.1@text&&
.tabcontent@class.tabvalue.1@tag.td.0@text##最后更新：|连载状态：|作品分类：


封面图的另一种写法
class.zp@tag.a@href<js>
var id = result.match(/(\d+)\/?$/)[1];
var iid = parseInt(id/1000);
'https://www.qljgh5.tw/files/article/image/'+iid+'/'+id+'/'+id+'s.jpg';
</js>

文字内容不需要左右的[]括号可以这样写:
tag.a.0@text##\[|\]

目录页的章节名去垃圾话
text##正文\s|[\(（【].*?[求更票谢乐发订合补加].*?[】）\)]

章节名称通用替换规则:
dd@text##[\(（【].*?[求更谢乐发订合补加].*?[】）\)]

或者
tag.a@text@js:result.replace(/[（［【\{\(].*?[更合求票赏鲜盟修推歉谢祝节年].*?[）］】\}\)]/,"")
或者
//去除双第N章的章字样，2留1
tag.a@text##第.*?章\s?(第.*?章)(.*$)##$1 $2

章节URL规则适用于动态加载的网页:
tag.a@href@js:result+',{webView:“true”}'
或者
tag.a@href##$##,{'webView':true}

章节URL取到地址进行拼接的
tag.a@href##/(.*?)/(.*?).html##https://www.wanben8888txt.net/api/api.php,{
  "charset": "gbk",
  "method": "POST",  "body":"action=read&id=$1&cid=$2&token="
}
或者
tag.a@href@js:'https://www.8k55ana.com/book/'+result+'.html'
或者
用这个方法取当前详情页的URL来做拆分拼接
//取当前链接里的数字，然后带入新的链接里面去
@js:var bid = baseUrl.match(/\d+/);
java.put('bid', bid);
'https://uk.reade5455r.com/book-read/'+bid+'/{{$.seq}}'

﹉﹉﹉﹉
★详情页+目录页+正文第一章显示在一页的时候的处理方法:
章节名写法
//具体到它的分页显示比如:首页 2/22 下一页 尾页
a.0@text##(\d+)\/\d+##第$1页
其他地方获取内容正常获取，就是在目录页里面的章节URL规则里面这样写:
//意思是跟目录页共用一页作为第一章的网址
{{baseUrl}}

或者
就不填目录链接，目录列表可以填tag.html或tag.body等，章节名称tag.title@text，章节链接填href（获取不到链接，正文就会直接用详情页链接）或者章节链接留空
反正就是要有一个列表能获取到章节名称就行
﹉﹉﹉﹉﹉

简介通用替换规则:
class.intro_info@textNodes##(^|[。！？]+[”」）】]?)##$1<br>
或者
[property$=description]@content##(^|[。！？]+[”」）】]?)##$1<br>


目录下一页规则
//适用于目录列表在详情页属于隐藏标签的
option@value
或者并发加载，多个隐藏按钮一起打开
[name=pageselect] > option!0@value

目录列表规则写法
从id.list开始一直找到tag.dd标签然后把tag.dd的最上面9个排除，因为！号后面的0代表数字1后面的每个数字都是同理加上1算实际对的第几个章节目录
id.list@tag.dl@tag.dd[!0:8]
或者
id.list@tag.dl@tag.dd!0:1:2:3:4:5:6:7:8

目录标签下的目录列表规则
//找div标签里面id是lbks的底下的dl标签下的最后一个dt标签后面的与dt标签同级标签里面找dd标签下的a标签
//div[@id="lbks"]/dl/dt[last()]/following-sibling::dd/a
案列:
<div id="lbks"><dl><dt>最新8章节，如果喜欢可以把级放到书架里面随时观看</dt><dd><a href="/shoujixs_167907_44533846.html">第996章 古之名将</a></dd><dd><a href="/shoujixs_167907_44533845.html">第995章 包拯来啦</a></dd><dd><a href="/shoujixs_167907_44533844.html">第994章 丢了一魄嗯宁采臣</a></dd><dd><a href="/shoujixs_167907_44533843.html">第993章 移山术满级</a></dd><dd><a href="/shoujixs_167907_44533624.html">第992章 踏足枉死城</a></dd><dd><a href="/shoujixs_167907_44532919.html">第991章 玩家的求助帖</a></dd><dd><a href="/shoujixs_167907_44531951.html">第990章 一计不成又生一计</a></dd><dd><a href="/shoujixs_167907_44524032.html">第989章 损耗</a></dd><dt>正文</dt><dd><a href="/shoujixs_167907_41554242.html">第1章 全能王者！瞬间满级</a></dd><dd><a href="/shoujixs_167907_41554243.html">第2章 玩家广场热议综合排名第一人</a></dd><dd><a href="/shoujixs_167907_41554244.html">第3章 东汉末年冀州阵营</a></dd><dd><a href="/shoujixs_167907_41554245.html">第4章 成就勋章</a></dd><dd><a href="/shoujixs_167907_41555507.html">第5章 高览</a></dd><dd><a href="/shoujixs_167907_41569074.html">第6章 高阶刀法</a></dd><dd><a href="/shoujixs_167907_41569076.html">第7章 沙场刀诀</a></dd>


听书源的正文写法
正文规则
<js>result</js>
资源正则
.*\.(mp3|m4a).*


正文去重复章节名
id.contents@html
<js>
a=title.replace(/第.*章\s*/,'第.*章')
b=new RegExp(a,'g')
result.replace(b,'')
</js>

或者
书源正文规则后面添加 ##{{chapter.title}}
可去除章节名称

正文下一页写法(拼接网址)
<js>
var list=[];
if(n=result.match(/\/(\d+)页/)){
for(var i=2;i<=n[1];i++){list.push(baseUrl.replace(/\/$/,"_"+i+"/"))
}}list</js>


正文多个正则拼接
##正则1
<js>result</js>
##正则2

延时执行内容的方法，sleep的值是毫秒，1000等于1秒
<js>
Packages.java.lang.Thread.sleep(1000);
result
</js>
等待1s之后执行
……………………
JSON隔栏取值写法
$.book_author@put{自定义变量：当前页面获取的值}
$.book_author@put:{bid:book_id}

跨栏调用的格式是固定的 是这样的@get:{自定义变量}，参考下面链接
这里调用本页的json信息可以用双大括号括起来{{$.book_id}} 里面的book_id就是要取的内容，参考下面链接
http://123456.com/{{$.book_id}}_@get:{bid}/1.html
……………………

漫画源正文
#cp_img@html##src.*\"
@js:result.replace(/data-original/g,"src")
漫画源正文的图片样式
FULL


发现页发现地址规则案列:

[{"title":"❀榜单❀","url":"","style":{"layout_flexBasisPercent":1,"layout_flexGrow":1}},
{"title":"总点击榜","url":"/top_allvisit/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"月点击榜","url":"/top_monthvisit/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"总推荐榜","url":"/top_allvote/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"月推荐榜","url":"/top_monthvote/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"总月票榜","url":"/top_allvipvote/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"总鲜花榜","url":"/top_allflower/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"月勤更榜","url":"/top_monthwords/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"最近更新","url":"/top_lastupdate/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"最新入库","url":"/top_postdate/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"收藏榜","url":"/top_goodnum/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"字数榜","url":"/top_words/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"新书榜","url":"/top_newhot/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"❀分类❀","url":"","style":{"layout_flexBasisPercent":1,"layout_flexGrow":1}},
{"title":"玄幻奇幻","url":"/xuanhuan/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"武侠仙侠","url":"/xianxia/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"都市言情","url":"/dushi/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"穿越架空","url":"/chuanyue/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"女生视觉","url":"/nvsheng/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}},
{"title":"精品辣文","url":"/lawen/{{page}}.html","style":{"layout_flexBasisPercent":0.25,"layout_flexGrow":1}}]

```



祝大家生活愉快！
