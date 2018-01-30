---
layout: post
title: java判断访问来源是PC端还是移动端，并返回不同的URL
date: 2018-01-30 
tags: java  
---

&nbsp;&nbsp;&nbsp;&nbsp;在web开发做手机站的时候会遇到这个问题,就是如果判断用户的请求是来自手机端还是pc端。
<br>&nbsp;&nbsp;&nbsp;&nbsp;实现这个需求有两种方法，一种是在前端进行判断，但这种方法不好的地方在于用户体验上不是特别好。因此我的思路是在后端创建一个拦截器，对首页的URL进行拦截，即在拦截的过程中获取用户请求头中的User-Agent,这个User-Agent记录了用户访问的设备信息。
<br>&nbsp;&nbsp;&nbsp;&nbsp;具体步骤如下：
 >* 1、写一个工具类
 >* 2、拦截器 
 >* 3、SpringMVC-Servlet中的拦截配置    

&nbsp;&nbsp;&nbsp;&nbsp;代码：
```     
//1、工具类——判断访问是移动端还是PC端
public class CheckPcOrMobileUtil {
    //判断是否为手机浏览器
    public static boolean JudgeIsMoblie(HttpServletRequest request) {
        boolean isMoblie = false;
        String[] mobileAgents = { "iphone", "android","ipad", "phone", "mobile", "wap", "netfront", "java", "opera mobi",
                "opera mini", "ucweb", "windows ce", "symbian", "series", "webos", "sony", "blackberry", "dopod",
                "nokia", "samsung", "palmsource", "xda", "pieplus", "meizu", "midp", "cldc", "motorola", "foma",
                "docomo", "up.browser", "up.link", "blazer", "helio", "hosin", "huawei", "novarra", "coolpad", "webos",
                "techfaith", "palmsource", "alcatel", "amoi", "ktouch", "nexian", "ericsson", "philips", "sagem",
                "wellcom", "bunjalloo", "maui", "smartphone", "iemobile", "spice", "bird", "zte-", "longcos",
                "pantech", "gionee", "portalmmm", "jig browser", "hiptop", "benq", "haier", "^lct", "320x320",
                "240x320", "176x220", "w3c ", "acs-", "alav", "alca", "amoi", "audi", "avan", "benq", "bird", "blac",
                "blaz", "brew", "cell", "cldc", "cmd-", "dang", "doco", "eric", "hipt", "inno", "ipaq", "java", "jigs",
                "kddi", "keji", "leno", "lg-c", "lg-d", "lg-g", "lge-", "maui", "maxo", "midp", "mits", "mmef", "mobi",
                "mot-", "moto", "mwbp", "nec-", "newt", "noki", "oper", "palm", "pana", "pant", "phil", "play", "port",
                "prox", "qwap", "sage", "sams", "sany", "sch-", "sec-", "send", "seri", "sgh-", "shar", "sie-", "siem",
                "smal", "smar", "sony", "sph-", "symb", "t-mo", "teli", "tim-", "tosh", "tsm-", "upg1", "upsi", "vk-v",
                "voda", "wap-", "wapa", "wapi", "wapp", "wapr", "webc", "winw", "winw", "xda", "xda-",
                "Googlebot-Mobile" };
        if (request.getHeader("User-Agent") != null) {
            String agent=request.getHeader("User-Agent");
            for (String mobileAgent : mobileAgents) {
                if (agent.toLowerCase().indexOf(mobileAgent) >= 0 && agent.toLowerCase().indexOf("windows nt")<=0 &&agent.toLowerCase().indexOf("macintosh")<=0) {
                    isMoblie = true;
                    break;
                }
            }
        }
        return isMoblie;
    }
}
```     
&nbsp;&nbsp;&nbsp;&nbsp;写一个拦截器，如果是PC端访问，则放行，如果是移动端访问，则跳转到移动端的url:  
```  
//拦截器——检查是移动端还是PC端
public class CheckPcOrMobile extends HandlerInterceptorAdapter {

    public void afterCompletion(HttpServletRequest request, HttpServletResponse response,
                                Object handler, Exception ex) throws Exception{
        super.afterCompletion(request,response,handler,ex);
    }

    public void postHandle(HttpServletRequest request, HttpServletResponse response,
                           Object handler, ModelAndView modelAndView) throws Exception{
        super.postHandle(request, response, handler, modelAndView);
    }

    public boolean preHandle(HttpServletRequest request, HttpServletResponse response, Object handler) throws Exception{
        boolean judgeIsMobile = CheckPcOrMobileUtil.JudgeIsMoblie(request);
        if(judgeIsMobile == true){
            response.sendRedirect("移动端URL");
        }else{
            return true;
        }
        return true;
    }
}
```
&nbsp;&nbsp;&nbsp;&nbsp;最后在SpringMVC-Servlet中的拦截配置：
```
<!--如果是移动端访问，拦截并转到移动端页面-->
        <mvc:interceptor>
            <mvc:mapping path="/**"/>
            <bean class="com.dimeng.front.controller.easy.common.CheckPcOrMobile"/>
        </mvc:interceptor>
```
<br>

转载请注明：[CarsonW's Blog](http://www.carsonwong.top/) » [点击阅读原文](http://www.carsonwong.top/2018/01/checkPcOrMobile/) 

 



