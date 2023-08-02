<template>
    <div class="zhifu">
        <h3>2支付通知</h3>
        <div class="left">
            投保单号：<input v-model="message" placeholder="请输入">
            <br> <br>地市：
            <select v-model="selected">
                <option disabled value="">请选择</option>
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
			<br> <br> <div class="attentionWord">注意：保函下载以及支付请切换外网</div>

			<div class="right"></div>
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
	<!-- <hr class="clearfix"> -->
    </div>
</template>

<script></script>

<style>
.zhifu {
    background-color: aquamarine;
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
.attentionWord {
	color: red;
	font-weight: bold;
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
</style>