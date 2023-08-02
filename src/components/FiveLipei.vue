<template>
<div>
    <div class="lipei">
        <h3>5理赔请求</h3>
        <div class="left">
            <form>
            <label>保单号：</label>
            <input v-model="id" placeholder="请输入">
            <br> <br>
            理赔人姓名：<input v-model="name" placeholder="请输入">
            <br> <br>
            理赔人联系方式：<input v-model="contact" placeholder="请输入">
            <br> <br>
            理赔原因：<input v-model="reason" placeholder="请输入">
            <br> <br>
            地市：<select v-model="city">
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
            <button @click="handleFive">提交</button>
        </form>

            <div class="result5" style="display: none">理赔中...</div>
        </div>
    </div>
    <div class="right">
        <div class="printresult">
			<div class="apply5">
				<div style="color: red; font-weight: bold;">请求报文：</div>
				<div class="content"><br><br><br><br></div>
			</div>
			<div class="return5">
				<div style="color: red; font-weight: bold;">响应报文：</div>
				<div class="content"><br><br><br><br></div>
			</div>
		</div>
    </div>
</div>
<!-- <hr class="clearfix"> -->
</template>

<script>

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
.printresult{
	border: 1px solid #000;
	height: 95%;
	width: 95%;
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
.result5{
	text-decoration: none;
	display: inline-block;
	text-align: center;
	width: 100px;
	height: 30px;
	line-height: 30px;
	border-radius: 4px;
	border: 0px solid #5077d8;
	color: #FF0000;
	background-color: #eee;
	margin-left: 100px;
	font-size: 20px;
	font-weight:bold;
}
</style>