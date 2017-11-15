# HTML 练习 - 试卷
## 说明:

## 实现两个页面：index.html&result.html

## 学习资源:

1. [W3School HTML教程](http://www.w3school.com.cn/html/index.asp)
2. 考试倒计时功能：http://www.jb51.net/article/99915.htm
3. 分析一个正则表达式函数GetQueryString

                   functionGetQueryString(name){

                             var reg = new RegExp("(^|&)"+name +"=([^&]*)(&|$)");

                             var r =window.location.search.substr(1).match(reg);

                             if(r!=null)return  decodeURI(r[2]); return null;

                   }

  a) 函数名为：GetQueryString()，需要传一个参数name，这是一个js写法

  b) var reg = new RegExp("(^|&)"+ name+"=([^&]*)(&|$)");

   RegExp 的构造函数创建了一个正则表达式对象，用模式来匹配文本。

--------------------------------续
(^|&)"+ name+"=([^&]*)(&|$)

这个正则表达式的意思是:以&号或其他开头，中间传过来一个变量name，后面

(^|&)   ：^匹配字符串开头,&就是&字符，(^|&)匹配字符串开头或者&字符，如果其后还有正则，那么必须出现在字符串开始或&字符之后

name   ：变量

([^&]*)  ：[^&]表示匹配不包含&的内容 *表示可以重复0或N次     PS.(^在[]才表示取反)

(&|$)   ：表示&结束(匹配多个参数)或直到结尾($表示结尾)

 c) var r = window.location.search.substr(1).match(reg);

window.location.search方法是截取当前url中“?”后面的字符串

比方说：https://www.xq.com:9001/?room_id=333将输出：?room_id=333;
substr(1):是截取字符串，从第1个输出（字符串从0开始记）



d) if(r!=null)return decodeURI(r[2]);
return null;
这两句话的意思是：如果r不是空的话，就返回解码后的r[2](room_id=333,就返回333)，否则，就返回空。
decodeURI() 函数可对 encodeURI() 函数编码过的 URI 进行解码。



---------------------------------------------------------------------------------------------------------
**/

