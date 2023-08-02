<template>

<div class="hello">
  <div class="tableTitle" style="font-size: 20px"><span class="midText">电子保函测试系统</span></div>

  <div class = "toubao">
    <h3>1投保请求</h3>
    <div class="left">
      投保人统一社会信用代码：<input type="text" id="idNumber" name="idNumber" value="91430105MA4Q4UU10E"> &nbsp;&nbsp;
      投保人姓名：<input type="text" id="Name" name="Name" value="工保科技（浙江）有限公司"> 
		<br> <br> 招标人统一社会信用代码：<input type="text" id="TendereeCode" name="TendereeCode" value="siDnioaZJK9"> &nbsp;&nbsp;
      招标人名称：<input type="text" id="TendereeName" name="TendereeName" value="dv2rAgYOmLh"> 
      <br> <br> 项目标段编号：<input type="text" id="BidSectionCode" name="BidSectionCode" value="NGeaiVj5wol"> &nbsp;&nbsp;
      项目名称：<input type="text" id="ProjectName" name="ProjectName" value="y6Y10id9CaQ"> 
      <br> <br> 投保人手机号：<input type="text" id="Mobile" name="Mobile" value="17677179907"> &nbsp;&nbsp;地市：<select id="City" class="platform" name="City">
				<option selected="selected" value="341600">亳州</option>
				<option selected="selected" value="341700">池州</option>
				<option selected="selected" value="341800">宣城</option>
				<option selected="selected" value="341200">阜阳</option>
				<option selected="selected" value="630000">青海</option>
				<option selected="selected" value="141100">吕梁</option>
				<option selected="selected" value="650000">新疆</option>
				<option selected="selected" value="650100">新疆生产建设兵团</option>
				<option selected="selected" value="430100">长沙(见费)</option>
				<option selected="selected" value="430300">湘潭(见费)</option>
				<option selected="selected" value="430600">岳阳(见费)</option>
				<option selected="selected" value="620500">天水(见费)</option>
				<option selected="selected" value="620100">兰州</option>
				<option selected="selected" value="430800">张家界</option>
				<option selected="selected" value="653201">和田</option>
				<option selected="selected" value="340500">马鞍山(见费)</option>
				<option selected="selected" value="653101">喀什</option>
				<option selected="selected" value="120000">天津(见费)</option>
				<option selected="selected" value="610100">西安(见费)</option>
				<option selected="selected" value="650500">哈密</option>
				<option selected="selected" value="653000">克州</option>
				<option selected="selected" value="654023">伊犁</option>
				<option selected="selected" value="65100X">乌鲁木齐</option>
			</select><br> <br>
			<div id="a">

				保费：<input type="text" id="sumPremium" name="sumPremium" readonly="readonly" value="1.5"> &nbsp;&nbsp;
        保额：<input type="text" id="sumAmount" name="sumAmount" readonly="readonly" value="300">

			</div>
			<br> <br> <a id="toubaoapply">提交</a >

			<div class="result1" style="display: none">投保中...</div>
    </div>

    <div class="right">
		<div class="printresult">
			<div class="apply1">
				<div style="color: red; font-weight: bold;">请求报文：</div>
				<div class="content"></div>
			</div>
			<div class="return1">
				<div style="color: red; font-weight: bold;">响应报文：</div>
				<div class="content"></div>
			</div>
		</div>
	</div>
</div>
<hr class="clearfix">

<div>
		<h3 class="">2支付通知</h3>
		<div class="left">
			投保单号：<input type="text" id="proposalno1" name="proposalno1">
			<br> <br> 地市：<select id="City1" class="platform" name="City1">
				<option selected="selected" value="341600">亳州</option>
				<option selected="selected" value="341700">池州</option>
				<option selected="selected" value="341800">宣城</option>
				<option selected="selected" value="341200">阜阳</option>
				<option selected="selected" value="630000">青海</option>
				<option selected="selected" value="141100">吕梁</option>
				<option selected="selected" value="650000">新疆</option>
				<option selected="selected" value="650100">新疆生产建设兵团</option>
				<option selected="selected" value="430100">长沙(见费)</option>
				<option selected="selected" value="430300">湘潭(见费)</option>
				<option selected="selected" value="430600">岳阳(见费)</option>
				<option selected="selected" value="620500">天水(见费)</option>
				<option selected="selected" value="620100">兰州</option>
				<option selected="selected" value="430800">张家界</option>
				<option selected="selected" value="653201">和田</option>
				<option selected="selected" value="340500">马鞍山(见费)</option>
				<option selected="selected" value="653101">喀什</option>
				<option selected="selected" value="120000">天津(见费)</option>
				<option selected="selected" value="610100">西安(见费)</option>
				<option selected="selected" value="650500">哈密</option>
				<option selected="selected" value="653000">克州</option>
				<option selected="selected" value="654023">伊犁</option>
				<option selected="selected" value="65100X">乌鲁木齐</option>
			</select> <br> <br>
			<div style="color: red; font-weight: bold;">注意：保函下载以及支付请切换外网</div>
			<br> <a id="zhifuapply">提交</a > <a id="url" href=" "
				target="_blank">保函下载</a > <a id="url1" href=" " target="_blank">去支付</a >

			<div class="result2" style="display: none">支付中...</div>
		</div>
	</div>

	<div class="right">
		<div class="printresult">
			<div class="apply2">
				<div style="color: red; font-weight: bold;">请求报文：</div>
				<div class="content"></div>
			</div>
			<div class="return2">
				<div style="color: red; font-weight: bold;">响应报文：</div>
				<div class="content"></div>
			</div>
		</div>
	</div>
	<hr class="clearfix">

  <div class="">
		<h3 >3批改请求</h3>
		<div id="pigaiapply_from" class="left">
			被保人姓名：<input type="text" id="name" name="name" value="利辛县公路管理服务中心">
			&nbsp;&nbsp;被保人统一社会信用代码：<input type="text" id="idNumber1"
				name="idNumber1" value="12341623MB1H010947"><br> <br>
			招标项目名称：<input type="text" id="projectName" name="projectName"
				value="2021年度利辛县农村公路养护工程第二标段（中修）"> &nbsp;&nbsp;招标文件编号：<input
				type="text" id="projectNo" name="projectNo" value="BZLXGC2021044-02"><br>
			<br> 保单号：<input type="text" id="policyno3" name="policyno3">
			&nbsp;&nbsp;地市：<select id="City3" class="platform" name="City3"><option
					selected="selected" value="341600">亳州</option>
				<option selected="selected" value="341700">池州</option>
				<option selected="selected" value="341800">宣城</option>
				<option selected="selected" value="341200">阜阳</option>
				<option selected="selected" value="630000">青海</option>
				<option selected="selected" value="141100">吕梁</option>
				<option selected="selected" value="650000">新疆</option>
				<option selected="selected" value="650100">新疆生产建设兵团</option>
				<option selected="selected" value="430100">长沙(见费)</option>
				<option selected="selected" value="430300">湘潭(见费)</option>
				<option selected="selected" value="430600">岳阳(见费)</option>
				<option selected="selected" value="620500">天水(见费)</option>
				<option selected="selected" value="620100">兰州</option>
				<option selected="selected" value="430800">张家界</option>
				<option selected="selected" value="653201">和田</option>
				<option selected="selected" value="340500">马鞍山(见费)</option>
				<option selected="selected" value="653101">喀什</option>
				<option selected="selected" value="120000">天津(见费)</option>
				<option selected="selected" value="610100">西安(见费)</option>
				<option selected="selected" value="650500">哈密</option>
				<option selected="selected" value="653000">克州</option>
				<option selected="selected" value="654023">伊犁</option>
				<option selected="selected" value="65100X">乌鲁木齐</option>
			</select><br> <br>
			<div id="qhym" style="display: none">
				招标人电话：<input type="text" id="tenderMobile" name="tenderMobile">
				&nbsp;&nbsp;招标人地址：<input type="text" id="tendereeAddress"
					name="tendereeAddress">
			</div>
			<br>

			<div style="color: red; font-weight: bold;">注意：批改单下载请切换外网</div>
			<br> <a id="pigaiapply">提交</a> <a id="src" href=""
				target="_blank">批改单下载</a>

			<div class="result4" style="display: none">批改中...</div>

		</div>
	</div>
	<div class="right">
		<div class="printresult">
			<div class="apply4">
				<div style="color: red; font-weight: bold;">请求报文：</div>
				<div class="content"></div>
			</div>
			<div class="return4">
				<div style="color: red; font-weight: bold;">响应报文：</div>
				<div class="content"></div>
			</div>
		</div>
	</div>
	<hr class="clearfix">

	<div>
		<h3 class="">4发票申请</h3>
		<div id="fapiaoapply_from" class="left">
			保单号：<input type="text" id="policyno2" name="policyno2">
			&nbsp;&nbsp;发票类型：<select id="InvoiceType" class="platform"
				name="InvoiceType">
				<option selected="selected" value="3">纸质（专票）</option>
				<option selected="selected" value="2">纸质（普票）</option>
				<option selected="selected" value="1">电子（普票）</option>
			</select> <br> <br> 发票抬头：<input type="text" id="InvoiceHead"
				name="InvoiceHead" value="安徽凯辉建筑工程有限公司"> &nbsp;&nbsp;纳税人识别号：<input
				type="text" id="cuscCode" name="cuscCode" value="91341600093343749W">
			<br> <br>
			<div id="dzpp">
				电子邮箱：<input type="text" id="email" name="email"
					placeholder="电子（普票）用字段" value="18855995605@163.com">
			</div>
			<div id="zzpp" style="display: none;">
				收件人：<input type="text" id="addressee" name="addressee"
					placeholder="纸质（普票）用字段" value="刘虎"> &nbsp;&nbsp; 收件人手机号：<input
					type="text" id="addresseePhone" name="addresseePhone"
					placeholder="纸质（普票）用字段" value="19156965565"> <br> <br>收件地址：<input
					type="text" id="address" name="address" placeholder="纸质（普票）用字段"
					value="安徽省亳州市谯城区中央公园3栋702室">
			</div>
			<div id="zzzp" style="display: none;">
				注册地址：<input type="text" id="addInfo" name="addInfo"
					placeholder="纸质（专票）用字段" value="中国建设银行股份有限公司亳州市分行">
				&nbsp;&nbsp;开户行：<input type="text" id="bankInfo" name="bankInfo"
					placeholder="纸质（专票）用字段" value="亳州市谯城区徽商银行西侧金品名门世家A区室"> <br>
				<br> 开户帐号：<input type="text" id="bankAcc" name="bankAcc"
					placeholder="纸质（专票）用字段" value="34050188860800000826">
				&nbsp;&nbsp;联系电话：<input type="text" id="phoneNo" name="phoneNo"
					placeholder="纸质（专票）用字段" value="0558-5958989">
			</div>
			<br> 地市：<select id="City2" class="platform" name="City2">
				<option selected="selected" value="341600">亳州</option>
				<option selected="selected" value="341700">池州</option>
				<option selected="selected" value="341800">宣城</option>
				<option selected="selected" value="341200">阜阳</option>
				<option selected="selected" value="630000">青海</option>
				<option selected="selected" value="141100">吕梁</option>
				<option selected="selected" value="650000">新疆</option>
				<option selected="selected" value="650100">新疆生产建设兵团</option>
				<option selected="selected" value="430100">长沙(见费)</option>
				<option selected="selected" value="430300">湘潭(见费)</option>
				<option selected="selected" value="430600">岳阳(见费)</option>
				<option selected="selected" value="620500">天水(见费)</option>
				<option selected="selected" value="620100">兰州</option>
				<option selected="selected" value="430800">张家界</option>
				<option selected="selected" value="653201">和田</option>
				<option selected="selected" value="340500">马鞍山(见费)</option>
				<option selected="selected" value="653101">喀什</option>
				<option selected="selected" value="120000">天津(见费)</option>
				<option selected="selected" value="610100">西安(见费)</option>
				<option selected="selected" value="650500">哈密</option>
				<option selected="selected" value="653000">克州</option>
				<option selected="selected" value="654023">伊犁</option>
				<option selected="selected" value="65100X">乌鲁木齐</option>
			</select> <br> <br> <a id="fapiaoapply">提交</a>
			<div class="result3" style="display: none">发票申请中...</div>

		</div>
	</div>
	<div class="right">
		<div class="printresult">
			<div class="apply3">
				<div style="color: red; font-weight: bold;">请求报文：</div>
				<div class="content"></div>
			</div>
			<div class="return3">
				<div style="color: red; font-weight: bold;">响应报文：</div>
				<div class="content"></div>
			</div>
		</div>
	</div>
	<hr class="clearfix">


	<div>
		<h3 class="">5理赔请求</h3>
		<div id="lipeiapply_from" class="left">
			保单号：<input type="text" id="policyno4" name="policyno4"> <br>
			<br> 理赔人姓名：<input type="text" id="claimName" name="claimName"
				value="公共资源交易中心"> <br> <br> 理赔人联系方式：<input
				type="text" id="claimPhone" name="claimPhone" value="17677179907">
			<br> <br> 理赔原因：<input type="text" id="cliaimReason"
				name="cliaimReason" value="后台发起理赔"> <br> <br> 地市：<select
				id="City4" class="platform" name="City4">
				<option selected="selected" value="341600">亳州</option>
				<option selected="selected" value="341700">池州</option>
				<option selected="selected" value="341800">宣城</option>
				<option selected="selected" value="341200">阜阳</option>
				<option selected="selected" value="630000">青海</option>
				<option selected="selected" value="141100">吕梁</option>
				<option selected="selected" value="650000">新疆</option>
				<option selected="selected" value="650100">新疆生产建设兵团</option>
				<option selected="selected" value="430100">长沙(见费)</option>
				<option selected="selected" value="430300">湘潭(见费)</option>
				<option selected="selected" value="430600">岳阳(见费)</option>
				<option selected="selected" value="620500">天水(见费)</option>
				<option selected="selected" value="620100">兰州</option>
				<option selected="selected" value="430800">张家界</option>
				<option selected="selected" value="653201">和田</option>
				<option selected="selected" value="340500">马鞍山(见费)</option>
				<option selected="selected" value="653101">喀什</option>
				<option selected="selected" value="120000">天津(见费)</option>
				<option selected="selected" value="610100">西安(见费)</option>
				<option selected="selected" value="650500">哈密</option>
				<option selected="selected" value="653000">克州</option>
				<option selected="selected" value="654023">伊犁</option>
				<option selected="selected" value="65100X">乌鲁木齐</option>
			</select> <br> <br> <a id="lipeiapply">提交</a>

			<div class="result5" style="display: none">理赔中...</div>

		</div>
	</div>
	<div class="right">
		<div class="printresult">
			<div class="apply5">
				<div style="color: red; font-weight: bold;">请求报文：</div>
				<div class="content"></div>
			</div>
			<div class="return5">
				<div style="color: red; font-weight: bold;">响应报文：</div>
				<div class="content"></div>
			</div>
		</div>
	</div>
	<hr class="clearfix">


	<div>
		<h3 class="">6退保请求</h3>
		<div id="tuibaoapply_from" class="left">
			退保保单号：<input type="text" id="policyno5" name="policyno5"> <br>
			<br> 退保原因：<input type="text" id="policyReason"
				name="policyReason" value="投标人自行申请退保"> <br> <br>
			账户名：<input type="text" id="accountNo" name="accountNo" value="张丽君">
			<br> <br> 退款账号开户行：<input type="text" id="bankName"
				name="bankName" value="招商银行"> <br> <br> 退款账号：<input
				type="text" id="bankNo" name="bankNo" value="62148312139010">
			<br> <br> 地市：<select id="City5" class="platform"
				name="City5">
				<option selected="selected" value="341600">亳州</option>
				<option selected="selected" value="341700">池州</option>
				<option selected="selected" value="341800">宣城</option>
				<option selected="selected" value="341200">阜阳</option>
				<option selected="selected" value="630000">青海</option>
				<option selected="selected" value="141100">吕梁</option>
				<option selected="selected" value="650000">新疆</option>
				<option selected="selected" value="650100">新疆生产建设兵团</option>
				<option selected="selected" value="430100">长沙(见费)</option>
				<option selected="selected" value="430300">湘潭(见费)</option>
				<option selected="selected" value="430600">岳阳(见费)</option>
				<option selected="selected" value="620500">天水(见费)</option>
				<option selected="selected" value="620100">兰州</option>
				<option selected="selected" value="430800">张家界</option>
				<option selected="selected" value="653201">和田</option>
				<option selected="selected" value="340500">马鞍山(见费)</option>
				<option selected="selected" value="653101">喀什</option>
				<option selected="selected" value="120000">天津(见费)</option>
				<option selected="selected" value="610100">西安(见费)</option>
				<option selected="selected" value="650500">哈密</option>
				<option selected="selected" value="653000">克州</option>
				<option selected="selected" value="654023">伊犁</option>
				<option selected="selected" value="65100X">乌鲁木齐</option>
			</select> <br> <br> <a id="tuibaoapply">提交</a>

			<div class="result6" style="display: none">退保中...</div>

		</div>
	</div>
	<div class="right">
		<div class="printresult">
			<div class="apply6">
				<div style="color: red; font-weight: bold;">请求报文：</div>
				<div class="content"></div>
			</div>
			<div class="return6">
				<div style="color: red; font-weight: bold;">响应报文：</div>
				<div class="content"></div>
			</div>
		</div>
	</div>
	<hr class="clearfix">



</div>




</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}

{/* <script type="text/javascript"> */}
$(function() {
    $("#lipeiapply").click(
            function() {
                var policyno4 = $("#policyno4").val();
                var claimName = $("#claimName").val();
                var claimPhone = $("#claimPhone").val();
                var cliaimReason = $("#cliaimReason").val();
                var City4 = $("#City4").val();
                if (!policyno4) {
                    alert('请输入保单号');
                    $("#policyno4").focus();
                    return;
                }

                if (!claimName) {
                    alert('请输入理赔人姓名');
                    $("#claimName").focus();
                    return;
                }

                if (!claimPhone) {
                    alert('请输入理赔人联系方式');
                    $("#claimPhone").focus();
                    return;
                }
                if (!claimPhone.match(/^1(3|4|5|6|7|8|9)\d{9}$/)) {
                    alert("手机号码格式不正确！");
                    $("#claimPhone").focus();
                    return;
                }

                if (!cliaimReason) {
                    alert('请输入理赔原因');
                    $("#cliaimReason").focus();
                    return;
                }
                $(".result5").show();

                $.ajax({
                    type : 'post',
                    url : 'PpeiPort',
                    data : JSON.stringify({
                        'policyno4' : policyno4,
                        'claimName' : claimName,
                        'claimPhone' : claimPhone,
                        'cliaimReason' : cliaimReason,
                        'City4' : City4
                    }),
                    datatType : 'json',
                    contentType : 'application/json;charset=UTF-8',
                    success : function(data) {
                        var requestXml = data.requestXML;
                        $(".apply5 .content").text(requestXml);

                        var responseXml = data.resposeXML;
                        $(".return5 .content").text(responseXml);
                        if (data.status == "true"
                                || data.status == "00000000") {
                            $(".result5").text("理赔成功");
                        } else {
                            $(".result5").text(data.msg);
                        }
                    },
                    error : function(data) {
                        alert('系统异常')
                    }
                })
            })
})

</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  color: rgb(16, 3, 3);
  font-size: 24px;
  text-align: center;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #000704;
}

.tableTitle {
  position: relative;
  margin: 0 auto;
  width: 900px;
  height: 1px;
  background-color: #d4d4d4;
  text-align: center;
  font-size: 16px;
  color: rgba(101, 101, 101, 1);
}
.midText {
  position: absolute;
  left: 50%;
  background-color: #ffffff;
  padding: 0 15px;
  transform: translateX(-50%) translateY(-50%);
}
.hello {
  position: inherit;
}
.toubao {
  background-color: antiquewhite;
}
.printresult{
	border: 1px solid #000;
	height: 95%;
	width: 95%;
	background-color: #fff;
	overflow: auto;
}
.clearfix {
  clear: both;
  margin: 25px 0px;
}
.left {
  width: 50%;
  height: 100%;
  float: left;
}
.right {
    width: 50%;
  height: 100%;
  float: right;
}
.apply1{
	border: 1px solid #000;
	height: 50%;
	width: 100%;
	background-color: #fff;
	overflow: auto;
}
.return1{
	border: 1px solid #000;
	height: 50%;
	width: 100%;
	background-color: #fff;
	overflow: auto;
}
.apply2{
	border: 1px solid #000;
	height: 50%;
	width: 100%;
	background-color: #fff;
	overflow: auto;
}
.return2{
	border: 1px solid #000;
	height: 50%;
	width: 100%;
	background-color: #fff;
	overflow: auto;
}
.apply3{
	border: 1px solid #000;
	height: 50%;
	width: 100%;
	background-color: #fff;
	overflow: auto;
}
.return3{
	border: 1px solid #000;
	height: 50%;
	width: 100%;
	background-color: #fff;
	overflow: auto;
}
.apply4{
	border: 1px solid #000;
	height: 50%;
	width: 100%;
	background-color: #fff;
	overflow: auto;
}
.return4{
	border: 1px solid #000;
	height: 50%;
	width: 100%;
	background-color: #fff;
	overflow: auto;
}
.apply5{
	border: 1px solid #000;
	height: 50%;
	width: 100%;
	background-color: #fff;
	overflow: auto;
}
.return5{
	border: 1px solid #000;
	height: 50%;
	width: 100%;
	background-color: #fff;
	overflow: auto;
}
.apply6{
	border: 1px solid #000;
	height: 50%;
	width: 100%;
	background-color: #fff;
	overflow: auto;
}
.return6{
	border: 1px solid #000;
	height: 50%;
	width: 100%;
	background-color: #fff;
	overflow: auto;
}
</style>
