
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head> 
 	<script type="text/javascript">
	//底部路径
	var basePath=footerPath="http://www.365bangnichou.com/";
	var  currUser_id="";//当前登录人ID
	var codeStatus = "false";
	</script>
	<meta http-equiv="Pragma" content="no-cache"/>
	<meta http-equiv="Cache-Control" content="no-cache, must-revalidate">
	<meta http-equiv="Expires" content="0">
	<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
	<meta name="renderer" content="webkit"  />
	<meta http-equiv="X-UA-Compatible" content="IE=Edge,chrome=1"  /> 
	<meta name="renderer" content="webkit">
	<meta name="keywords" content="帮你筹，公益众筹"  />
	<meta name="description" content="帮你筹"  />
	<meta property="wb:webmaster" content="3e7a490b04ffe9d8" />
	<link rel="icon" href="http://www.365bangnichou.com/easy/images/favicon.ico" type="image/x-icon" />

	<link rel="stylesheet" type="text/css" href="http://www.365bangnichou.com/easy/css/newsinformation.css">

	<link rel="stylesheet" type="text/css" href="http://www.365bangnichou.com/easy/css/base.css" />
	<link rel="stylesheet" type="text/css" href="http://www.365bangnichou.com/easy/css/common.css" />
	<link rel="stylesheet" type="text/css" href="http://www.365bangnichou.com/easy/css/index.css" />
	<link rel="stylesheet" type="text/css" href="http://www.365bangnichou.com/easy/css/front.css" />
	<link rel="stylesheet" type="text/css" href="http://www.365bangnichou.com/easy/css/user.css" />


	
	<!-- 公用js -->
	<script type="text/javascript" src="http://www.365bangnichou.com/js/common/jquery-1.8.3.min.js"></script>
	<script type="text/javascript" src="http://www.365bangnichou.com/js/common/jquery.form.min.js"></script>
	<script type="text/javascript" src="http://www.365bangnichou.com/js/core/jquery.spine.js"></script>
	<script type="text/javascript" src="http://www.365bangnichou.com/js/core/jquery.spine.framework.js"></script>
	<script type="text/javascript" src="http://www.365bangnichou.com/js/framework/DM.js?v=2015"></script>
	<script type="text/javascript" src="http://www.365bangnichou.com/js/framework/DM.Util.js"></script>




	<script type="text/javascript" src="http://www.365bangnichou.com/easy/js/home/Dialog.js"></script>
	<script type="text/javascript" src="http://www.365bangnichou.com/easy/js/home/common.js"></script>
	<script type="text/javascript" src="http://www.365bangnichou.com/easy/js/home/front.js"></script>
    <title>帮你筹</title> 
 </head> 
 <body> 
	 <div> 
	         <div id="layout_header"><script type="text/javascript">
    //自适应宽度
    function winWrap() {
        var width = $(window).width();
        if (width > 1300) {
            $("body").attr("class", "wrap-1220");
        } else {
            $("body").attr("class", "wrap-1002");
        }
    };
    $(window).resize(function () {
        winWrap();
    });
    winWrap();
</script>
<!--底部-->
<link rel="stylesheet" type="text/css" href="http://www.365bangnichou.com/easy/css/public.css">
<!--头部-->
<header>
    <div class='header'>
        <a href="http://www.365bangnichou.com/home/index.do" class='fl logo'><img src="http://www.365bangnichou.com/easy/images/logo2.png"></a>
        <ul class='fl head-n' id="HEADER_MENUS">
            <li class=""><a href="http://www.365bangnichou.com/home/index.do">首页</a></li>
            <li><a href="http://www.365bangnichou.com/project/projectList.do">项目</a></li>
            <li><a href="http://www.365bangnichou.com/hospital/hospitalList.do">医院</a></li>
            <li><a href="http://www.365bangnichou.com/foundation/foundationDetails.do?foundationId=100">基金会</a></li>
            <li><a href="http://www.365bangnichou.com/home/aboutUs.do">关于我们</a></li>
            <li><a href="http://www.365bangnichou.com/frontHome/newsInfos.do">新闻资讯</a></li>
            <div class='clear'></div>
        </ul>
        <div class='fr loin'>
            <!-- 登录前 -->
            <a href="http://www.365bangnichou.com/home/login.do" class="ina">我要注册</a>
                <a href="http://www.365bangnichou.com/home/login.do" class="inb">登录</a>
            <!-- 登录前 end-->
            <!--已登录-->
            <!-- 登录后 end-->
        </div>
    </div>
</header>
<script type="text/javascript" src="http://www.365bangnichou.com/easy/js/home/header.js"></script>
<script>
    var hrefs = window.location.href;
    $("#HEADER_MENUS").find("li").removeClass("actiog");
    if (hrefs.indexOf("/home/index") > 0) {
        $("#HEADER_MENUS").find("li:eq(0)").addClass("actiog");
    } else if (hrefs.indexOf("/project/") > 0) {
        $("#HEADER_MENUS").find("li:eq(1)").addClass("actiog");
    } else if (hrefs.indexOf("/hospital/") > 0) {
        $("#HEADER_MENUS").find("li:eq(2)").addClass("actiog");
    } else if (hrefs.indexOf("/home/aboutUs") > 0) {
        $("#HEADER_MENUS").find("li:eq(4)").addClass("actiog");
    } else if (hrefs.indexOf("/frontHome/") > 0) {
        $("#HEADER_MENUS").find("li:eq(5)").addClass("actiog");
    }else if (hrefs.indexOf("/foundation/") > 0) {
        $("#HEADER_MENUS").find("li:eq(3)").addClass("actiog");
    }
</script></div>
	         <div id="layout_body"><link rel="stylesheet" type="text/css" href="http://www.365bangnichou.com/easy/css/public.css">
<!-- 头部菜单栏  菜单索引   begin -->
<input type="hidden" id="head_menus_index" value="H_SY"/>
<!-- 头部菜单栏  菜单索引   end -->
<!--首页客服浮层-->
<div class="floating_layer">
	<ul>
    	<li class="item">
            <div class="block weixin code">
                <div class="con"><div class="border"><img style="width: 140px;height: 140px" src="/fileStore/2017/12/18/11/jpeg/1513566234501.jpeg"><p>微信公众号</p><i class="arrow"></i></div></div>
            </div>
        </li>
      <li class="item">
        	<div class="block service">
                <div class="con">
                	<div class="border">
                    	<i class="arrow"></i>
                        <ul>
                          <li><a href="tencent://message/?uin=2194770137&Site=&Menu=yes" >在线客服</a></li>
		                  </ul>
                    </div>
                </div>
            </div>
        </li>
    	<li class="item" id="returnTop"><a class="block back" onclick="javascript:void(0)"></a></li>
	</ul>
    
</div>  
<!--浮层-->

<div id="homeContent">


</div>
<link rel="stylesheet" type="text/css" href="http://www.365bangnichou.com/easy/css/expend.css">
<!-- 模板 -->
<script id="homeContentTmpl" type="text/x-jquery-tmpl">
	<link rel="stylesheet" type="text/css" href="http://www.365bangnichou.com/easy/css/index_new.css">

<!--banner 首页滚动广告图片-->
{{if advertise!=null && advertise.length>0}}
<div class="banner clearfix">
    <ul class="rslides">
        {{each(sta, obj) advertise}}
        <li style="background:url({{= obj.adImageUrl }}) center 0 no-repeat;">
            <a href="{{if obj.adPartnerUrl.length > 7 }}{{= obj.adPartnerUrl}}{{/if}}{{if obj.adPartnerUrl.length <= 7 }}javascript:void(0){{/if}}"
               {{if obj.openType== 1 }}target="_blank" {{/if}}{{if obj.openType == 2 }}target="_self"{{/if}}
            title=""></a>
        </li>
        {{/each}}
    </ul>
</div>
{{/if}}
<!--banner-->

<div class='txt-yo'>
    <div>
        <p>“帮你筹”平台致力于重大疾病救助信息发布及网络建设、整合社会爱心资源，缓解病患个人及家庭困境；帮你筹平台致力于重大疾病的
            防治工作以及优质医疗资源的整合，提高贫困病患救治率。“帮你筹”平台将积极整合爱心企业（个人）、慈善机构、医疗机构等慈善
            资源，通过移动互联网技术打通慈善筹款与医疗救助的爱心 通路。
        </p>
        <ul class='liu-cfr'>
            <li><img src="http://www.365bangnichou.com/easy/images/cn07.png">
                <p>多家全国性公益机构<br>百家行业媒体群</p></li>
            <li><img src="http://www.365bangnichou.com/easy/images/cn09.png">
                <p>全国医务救助组织</br>百家省级三甲医院</p></li>
            <li><img src="http://www.365bangnichou.com/easy/images/cn06.png">
                <p>多家国家指定互联网筹款平台</br>真实的患者数据</p></li>
            <li><img src="http://www.365bangnichou.com/easy/images/cn08.png">
                <p>多个全国性用户数据接口</br>开放性的数据平台</p></li>
            <div class='clear'></div>
        </ul>
    </div>
</div>
<!-- 推荐项目 -->
<div class='tui-ja'>
    <div class='cyio'>
        <div class='ph'>
            <h1>推荐项目</h1>
            <span>recommendable projects</span></br>
            <i></i>
        </div>
        <ul class='im-tx'>
            {{each(staInfo, objInfo) hotProject}}
            <li>
                <img src="{{= objInfo.projectImg}}"
                     onclick="location.href='http://www.365bangnichou.com/project/projectDetails.do?projectId={{= objInfo.projectId}}'">
                <div class='detailed'>
                    <p class='ti-m'>
                        <a href="http://www.365bangnichou.com/project/projectDetails.do?projectId={{= objInfo.projectId}}">慈善募捐&nbsp;|&nbsp;{{=
                            objInfo.projectName}}&nbsp;|&nbsp;帮你筹</a>
                    </p>

                    <p class='yi-b' style="width:330px;white-space: nowrap; overflow: hidden; text-overflow: ellipsis">
                        <b></b><span>{{= objInfo.hospitalName}}</span><i></i> <span>{{= objInfo.foundationName}}</span>
                    </p>
                    <div class='dao-t' id='dao-t'>
                        <p><span id="progress">{{= objInfo.rate*100}}%</span></p>
                    </div>
                    <ul class='ul-num'>
                        <li>目标金额（元）</br> <span>{{= objInfo.targetAmount}}</span></li>
                        <li>已筹金额（元）</br> <span>{{= objInfo.raiseTotal}}</span></li>
                        <li>捐助人次（次）</br> <span>{{= objInfo.supportCount}}</span></li>
                        <div class='clear'></div>
                    </ul>
                    <p class='but-a'><a
                            href="http://www.365bangnichou.com/project/projectDetails.do?projectId={{= objInfo.projectId}}">我要捐款</a>
                    </p>
                </div>
            </li>
            {{/each}}
            <div class='clear'></div>
        </ul>
        </div>
</div>
<!-- 合作医院 -->
<div class='he-hospital'>
    <div class='hos-hz'>
        <div class='ph'>
            <h1>合作医院</h1>
            <span>cooperative hospital</span></br>
            <i></i>
        </div>
        <div class='add-eas'>
            <p class='fl'><img src="http://www.365bangnichou.com/easy/images/WechatIMG59.png"></p>
            <div class='fr wid-ad'>

                <p>百家医院、国家指定互联网筹款平台、行业媒体、公益机构
                    </br>医务救助机构、爱心企业（个人）全面参与
                </p>
                <ul class='hospital-name'>
                    {{each(sta, obj) homeHosList}}
                    <li><a href="http://www.365bangnichou.com/hospital/hospitalDetails.do?hospitalId={{= obj.hospitalId}}">{{=
                        obj.hospitalName}}</a></li>
                    {{/each}}
                    <li><a href="http://www.365bangnichou.com/hospital/hospitalList.do">查看更多医院>></a></li>
                    <div class='clear'></div>
                </ul>
            </div>
            <div class='clear'></div>
        </div>
    </div>
</div>
<!-- 网站公告 -->
<div class='announ'>
    <div class='acement'>
        <div class='fl'>
            <div class='hl'>
                <h1>新闻动态</h1>
                <span>news</span></br>
                <i></i>
            </div>
            <ul class='xiw-k'>
                {{each(sta, obj) InvestmentDynamicInfo}}
                <li>
                    <a href="http://www.365bangnichou.com/frontHome/newsInfosDetails.do?id={{= obj.id}}">
                        <p class='fl dats'>
                            <b>{{= obj.dateCreateDay}}</b></br>
                            <span>{{= obj.dateCreate}}</span>
                        </p>
                        <div class='fl di-w'>
                            <h1>{{= obj.infoTitle}}</h1>
                            <p>{{= obj.infoContent}}</p>
                        </div>
                        <div class='clear'></div>
                    </a>
                </li>
                {{/each}}
                </ul>
            <a href="http://www.365bangnichou.com/frontHome/toNewsInfos.do?investmentInfoType=2" target="_blank" class='fr gd-n'></a>
        </div>
        <div class='fr'>
            <div class='hl'>
                <h1>网站公告</h1>
                <span>Website announcement</span></br>
                <i></i>
            </div>
            <ul class='xiw-k'>
                {{each(sta, obj) InvestmentInfo}}
                <li>
                    <a href="http://www.365bangnichou.com/frontHome/newsInfosDetails.do?id={{= obj.id}}">
                        <p class='fl dats'>
                            <b>{{= obj.dateCreateDay}}</b></br>
                            <span>{{= obj.dateCreate}}</span>
                        </p>
                        <div class='fl di-w'>
                            <h1>{{= obj.infoTitle}}</h1>
                            <p>{{= obj.infoContent}}</p>
                        </div>
                        <div class='clear'></div>
                    </a>
                </li>
                {{/each}}
                </ul>
            <a href="http://www.365bangnichou.com/frontHome/toNewsInfos.do?investmentInfoType=1" target="_blank" class='fr gd-n'></a>
        </div>
        <div class='clear'></div>
    </div>
</div>

<div class='plat'>
    <div class='palt-cen'>
        {{each(sta, obj) partnersList}}
        <p><span>{{= obj.partnerType}}：<span></span></span><span>{{= obj.partnerName}}</span>
        <div class='clear'></div>
        </p>
        {{/each}}
    </div>
</div>

</script>
 
<form id="homeForm" method="post" action="http://www.365bangnichou.com/home/projectDetail.html" target="_blank">
  <input type="hidden" name="projectId" id="hidden_projectId"/>
</form>

<script type="text/javascript">
var  currUserId="";//当前登录人ID
//自适应宽度
$(window).resize(function() {
    var width = $(this).width();		
    if(width > 1300){
	$("body").attr("class","wrap-1220");
    
    }else{
	$("body").attr("class","wrap-1002");
    }
});

$(function(){
	//自适应宽度
	var width = $(window).width();		
	if(width > 1300){
	$("body").attr("class","wrap-1220");
    
	}else{
	$("body").attr("class","wrap-1002");
    }
});

$("#returnTop a").click(function(){
	$("html,body").animate({scrollTop:0},1000);
	
});

if (!!window.chrome)$('.palt-cen>p').addClass('spa');
$(function(){
    $('.dao-t>p>span').each(function(){
        var withs=$(this).html();
        $(this).parents('p').css('width',withs)
        if(parseInt(withs)<10){
            $(this).css('left',0)
        }
    })
})

</script>
<!-- add by wsh *******************-->
<script type="text/javascript" src="http://www.365bangnichou.com/js/common/percentage.js"></script>
<script type="text/javascript"  src="http://www.365bangnichou.com/js/common/jquery.tmpl.min.js"></script>
<!-- add by wsh end  -->
<script type="text/javascript" src="http://www.365bangnichou.com/easy/js/home/homePage.js"></script> 
</div> 
	        <div id="layout_footer"><!--底部-->
<link rel="stylesheet" type="text/css" href="http://www.365bangnichou.com/easy/css/public.css">
<link rel="stylesheet" type="text/css" href="http://www.365bangnichou.com/easy/css/index_new.css">

<footer>
	<div class='foot-a'>
		<div class='fot-ou'>
			<div class='fl tite'>
				<p>
					客服电话(09:00-20:00)</br>
					<span>400-969-9266</span>
				</p>
				<b></b>
			</div>
			<div class='fl mapt'>
				<p><a href="http://www.365bangnichou.com/home/aboutUs.do">关于我们</a><i></i><a href="http://www.365bangnichou.com/frontHome/helpCenter.do">帮助中心</a></p>
				<p><span>公司名称：</span>北京帮你筹科技有限公司</p>
				<p><span>公司地址：</span>北京市朝阳区白家庄路甲6号</p>
				<p><span>公司邮箱：</span>bangnichou@126.com</p>
			</div>
			<div class='fl wxin'>
				<!-- 微信公众号 -->
					<a href=""><img src="/fileStore/2017/12/18/11/jpeg/1513566234501.jpeg"></br><span>微信公众号</span></a>
					<!-- app客户端 -->
					<a href=""><img src="/fileStore/2017/12/18/11/png/1513566244974.png"></br><span>新浪微博</span></a>
					<div class='clear'></div>
			</div>
		</div>
	</div>
	<div class='foot-c'><p>个人求助、网络互助不属于慈善捐div实性由信息提供方负责</p></div>
	<div class='foot-b'>北京帮你筹科技有限公司©2017|备案号:京ICP备17056947号</div>
</footer>




</div> 
	        <iframe name="hframe" id="hframe" style="display:none"></iframe>
	 </div> 
 <script type="text/javascript" src="http://www.365bangnichou.com/easy/js/home/index.js"></script>
 <script type="text/javascript">
DM.Event.menuMonitor();//菜单监听
DM.Event.menuCss();
document.onkeydown = function () {
    if (window.event && window.event.keyCode == 13) {
        window.event.returnValue = false;
    }
}
</script>	
</body> 
</html> 

