# JRT-discuss
### 欢迎大家来讨论，JRT灌水，扯淡，意见专用仓库


---
>## 好无聊好像被强奸

>#### 为什么呢没人来强奸我

>#### 后面也可以
> <div align = right>1楼</div>

>---
</code>
<h2>AJAX</h2>
<button class="btn btn-sm BtnGroup-item" type="button" v-on:click="messageaa">请求数据</button>
<div id="myDiv"></div>


<script src="./public/vue.js"></script>
<script>
var example2 = new Vue({
el: '#discuss',
data: {
  parentMessage: 'Parent',
  items: [
    { message: 'Foo' },
    { message: 'Bar' }
  ]
},

methods: {
messageaa: function () {
  //window.alert(5 + 6)
  xmlhttp=new XMLHttpRequest()
  xmlhttp.onreadystatechange=function()
  {
    if (xmlhttp.readyState==4 && xmlhttp.status==200)
    {
      a=JSON.parse(xmlhttp.responseText)
      document.getElementById("myDiv").innerHTML=a[0].body
    }
  }
  xmlhttp.open("GET","https://api.github.com/repos/JRT-FOREVER/JRT-discuss/issues/comments",true)
  //var a=1
  xmlhttp.send()

}}
})


function loadXMLDoc()
{
  var xmlhttp;
  if (window.XMLHttpRequest)
  {
    // IE7+, Firefox, Chrome, Opera, Safari 浏览器执行代码
    xmlhttp=new XMLHttpRequest();
  }
  else
  {
    // IE6, IE5 浏览器执行代码
    xmlhttp=new ActiveXObject("Microsoft.XMLHTTP");
  }
  xmlhttp.onreadystatechange=function()
  {
    if (xmlhttp.readyState==4 && xmlhttp.status==200)
    {
      document.getElementById("myDiv").innerHTML=xmlhttp.responseText;
    }
  }
  xmlhttp.open("GET","https://api.github.com/repos/JRT-FOREVER/JRT-discuss/issues/comments",true);
  //xmlhttp.send();
}
</script>
<code>
