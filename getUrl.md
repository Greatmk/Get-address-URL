
##今天11月1日，Great来总结一下获取url中参数方法，分享一下

##获取一个url地址中的参数值方法:



```
 function GetQueryString(name){
            var reg = new RegExp("(^|&)"+ name +"=([^&]*)(&|$)");
            var r = window.location.search.substr(1).match(reg);
            if(r!=null)return  unescape(r[2]); return null;
        }

```
       
        
### 举例：假如现在一个url地址为：www.baidu.com/id=234&abc=we432de3
###      那么用上面封装好的方法调用一下就好了，如果要id参数  就把id传进去
###      也就是GetQueryString（“id”）以此内推

