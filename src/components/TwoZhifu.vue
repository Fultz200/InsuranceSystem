<template>
	<!-- Consolas, 'Courier New', monospace -->
<form id="TwoZhifu">
    <div id="lipei">
        <h3>2支付通知</h3>
        <div class="triple" @submit.prevent="handleFive" @submit='handleThree'>
            <form>
            投保单号：<input v-model="proposalno1" placeholder="请输入">
            <br> <br>
            地市：<select v-model="city1">
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
			</select> 
            <br> <br> 
            <div style="color:red; font-weight: bold;">注意：保函下载以及支付请切换外网</div>
			<button type="submit" class="button">提交</button>
            <button type="download" class="button">保函下载</button>
			<button type="download" class="button">去支付</button>

				<!-- <button type="submit">submit</button> -->
        </form>

            <!-- <div class="result5" style="display: none">理赔中...</div> -->
        </div>

		<div class="triple">
			<span style="color:red">请求报文</span>
			<p style="white-space: pre-line;">{{ message }}</p>
        <!-- <div class="printresult">
			<div class="apply5">
				<div style="color: red; font-weight: bold;">请求报文：</div>
				<div class="content"><br><br><br><br></div>
			</div>
			<div class="return5">
				<div style="color: red; font-weight: bold;">响应报文：</div>
				<div class="content"><br><br><br><br></div>
			</div>
		</div> -->
    </div>

		<div class="triple">
			<span style="color:red">响应报文</span>
			<p style="white-space: pre-line;">{{ message }}</p>
	</div>
    </div>

</form>
<!-- <form @submit.prevent="myMethod" @submit="alert">
  <button type="submit">submit</button>
</form> -->
<!-- <hr class="clearfix"> -->
</template>

<script>
export default {
	name:"TwoZhifu",
	data() {
		return {
			message :'<?xml version="1.0" encoding="utf-8"?><claimRequest><requestHead> <sign>1F1F4DEA13B5856A077D364B1BDC6835</sign> <requestUUID>65100X-1691047044383</requestUUID> </requestHead> <requestBody> <policyno>111</policyno> <claimName>公共资源交易中心</claimName> <claimPhone>17677179907</claimPhone> <cliaimReason>后台发起理赔</cliaimReason> </requestBody></claimRequest>',
			policyno4 : '', claimName : '', claimPhone : '', claimReason : ''
		}
	},
	methods: {
		handleThree() {

		},
		alert() {
			alert('理赔请求已提交')
		}
	}
}
</script>

<style>
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
.triple {
	box-sizing: border-box;  /*border计算在width中*/
	-moz-box-sizing:border-box; /* Firefox */
	-webkit-box-sizing:border-box; /* Safari */
	width: 33.33%;
	height: 300px;
	border: 0;
	float:left;
}
.autoChange {
	height: 600px;
	overflow:auto;
}

.printresult {
	border: 1px solid #000;
	height: 95%;
	width: 95%;
	background-color: #fff;
	overflow: auto;
}
.input {
	display: block;
	padding: 10px, 6px;
	width: 100%;
	box-sizing: border-box;
	border: none;
	border-bottom: 1px solid #ddd;
	color: #555;
}
.button {
	background: #1c8e23;
	border: 0;
	padding: 10px 20px;
	margin-top: 20px;
	color: white;
	border-radius: 20px;
}
.submit {
	text-align: center;
}

.apply5 {
	border: 1px solid #000;
	height: 50%;
	width: 100%;
	background-color: #fff;
	overflow: auto;
}
.return5 {
	border: 1px solid #000;
	height: 50%;
	width: 100%;
	background-color: #fff;
	overflow: auto;
}
.result5 {
	text-decoration: none;
	display: inline-block;
	text-align: center;
	width: 100px;
	height: 30px;
	line-height: 30px;
	border-radius: 4px;
	border: 0px solid #0c100b;
	color: #FF0000;
	background-color: #eee;
	margin-left: 100px;
	font-size: 20px;
	font-weight:bold;
}
</style>