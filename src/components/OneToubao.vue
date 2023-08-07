<template>
	<!-- Consolas, 'Courier New', monospace -->
<div id="OneToubao" class="autoChange">
    <div id="toubao">
        <h3>1投保请求</h3>
        <div class="triple" @submit.prevent="" @submit='handleOne'>
            <form>
            投保人统一社会信用代码：<input v-model="idNumber" placeholder="请输入">
            <br> <br>
            投保人姓名：<input v-model="Name" placeholder="请输入">
            <br> <br>
            招标人统一社会信用代码：<input v-model="TendereeCode" placeholder="请输入">
            <br> <br>
            招标人名称：<input v-model="TendereeName" placeholder="请输入">
            <br> <br>
            项目标段编号：<input v-model="BidSectionCode" placeholder="请输入">
            <br> <br>
            项目名称：<input v-model="ProjectName" placeholder="请输入">
            <br> <br>
            投保人手机号：<input v-model="Mobile" placeholder="请输入">
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
            保费：<input v-model="sumPremium" placeholder="请输入">
            <br> <br>
            保额：<input v-model="sumAmount" placeholder="请输入">
            <br> <br>
				<button type="submit" class="button">提交</button>
				<!-- <button type="submit">submit</button> -->
        </form>

            <!-- <div class="result5" style="display: none">理赔中...</div> -->
        </div>

		<div class="triple">
			<span style="color:red">请求报文</span>
			<p style="white-space: pre-line;">{{ requestXML }}</p>
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
			<p style="white-space: pre-line;">{{ responseXML }}</p>
	</div>
    </div>

</div>
<!-- <form @submit.prevent="myMethod" @submit="alert">
  <button type="submit">submit</button>
</form> -->
<!-- <hr class="clearfix"> -->
</template>

<script>
import axios from 'axios';
export default {
	name:"OneToubao",
	data() {
		return {
			message:'',
			message1:'<?xml version="1.0" encoding="utf-8"?><claimRequest><requestHead> <sign>1F1F4DEA13B5856A077D364B1BDC6835</sign> <requestUUID>65100X-1691047044383</requestUUID> </requestHead> <requestBody> <policyno>111</policyno> <claimName>公共资源交易中心</claimName> <claimPhone>17677179907</claimPhone> <cliaimReason>后台发起理赔</cliaimReason> </requestBody></claimRequest>',
            requestUUID:'1111111',
			idNumber:'',Name:'',TendereeCode:'',TendereeName:'',BidSectionCode:'',ProjectName:'',Mobile:'',city:'',sumPremium:'',sumAmount:'',
			requestXML: '',
			responseXML: '',
			time:'',
			resultFlag:true,
			resultMessage:'投保成功',
			proposalNo:'投保单号',
		}
	},
	methods: {
		alert() {
			alert('理赔请求已提交')
		},
		loadData() {
			axios.post('http://localhost:3000/posts', {
            title: "POST请求",
            author: "小M."
        }).then((result) => {
            console.log(result);
        }).catch((err) => {
            console.log(err);
        });
		},
		handleOne() {
			var request = "<?xml version=\"1.0\" encoding=\"utf-8\"?>" 
			+ " <insureRequest>" 
			+ "       <requestHead>"
			+ "            <requestUUID>"        + this.requestUUID      +     "</requestUUID>" 
			+ "            <sign>"               + "     "          +     "</sign>"
			+ "       </requestHead>" 
			+ "       <requestBody>"   
			+ "         <applicantInfo>" 
			+ "             <name>"              + this.Name             +    "</name>"
			+ "             <mobile>"            + this.Mobile           +    "</mobile>"
			+ "             <idNumber>"          + this.idNumber         +    "</idNumber>"
			+ "             <ProjectName>"       + this.ProjectName      +    "</ProjectName>" 
			+ "             <BidSectionCode>"    + this.BidSectionCode   +    "</BidSectionCode>" 
			+ "             <TendereeName>"      + this.TendereeName     +    "</TendereeName>"
			+ "             <TendereeCode>"      + this.TendereeCode     +    "</TendereeCode>" 
			+ "        </applicantInfo>"
			+ "        <policyInfo>" 
			+ "           <sumPremium>"          + this.sumPremium       +    "</sumPremium>"
			+ "           <sumAmount>"           + this.sumAmount        +    "</sumAmount>"
			+ "<endorseText>一、本特别约定，作为投标保证保险保单的有效组成部分，与保险合同、保单或其它保险凭证具有同等法律效力。二、保险单生效时间为投保项目投标截止时间，保险期间为投保项目《招标文件》中载明的投标有效期。三、投保人违反所投项目《招标文件》规定要求导致投标保证金不予退还或罚没情形的均属于本保单保险责任。四、退保处理1.开标前投保人自愿放弃投保或项目发生中止、暂停的，可进行退保；2.开标前项目发生流标、终止的，可进行退保；3.开标后项目发生流标的，可进行退保；4.除上述 3 种情形外均不予退保。5.投保人办理退保事宜，满足退保条件的，保险费全额退还。五、线下理赔材料提供如下：1.索赔申请书；2.招标文件和投标文件；3.投保人违约证明材料。六、保险公司应在收到索赔申请书和相关材料后 10 个工作日内完成理赔。七、保险人向被保险人赔偿后，保险人享有向投保人追偿的权利。</endorseText>"
			+ "       </policyInfo>" 
			+ "       </requestBody>"
			+ " </insureRequest>";

			this.requestXML = request;

			this.getTime()
			var response = "<?xml version=\"1.0\" encoding=\"utf-8\"?>" 
			+ " <insureRequest>" 
			+ "       <requestHead>"
			+ "            <requestUUID>"        + this.requestUUID      +     "</requestUUID>" 
			+ "            <sign>"               + "     "          +     "</sign>"
			+ "       </requestHead>" 
			+ "       <requestBody>"
			+ "             <responseTime>"      + this.time             +    "</responseTime>"
			+ "             <resultFlag>"        + this.resultFlag       +    "</resultFlag>"
			+ "             <resultMessage>"     + this.resultMessage    +    "</resultMessage>"
			+ "             <proposalNo>"        + this.proposalNo       +    "</proposalNo>" 
			+ "       </requestBody>"
			+ " </insureRequest>";

			this.responseXML = response;
		},
		getTime() {
			var date = new Date();
			//年
			var year = date.getFullYear();
			//月
			var month = date.getMonth() + 1;
			//日
			var strDate = date.getDate();
			//时
			var hour = date.getHours();
			//分
			var minute = date.getMinutes();
			//秒
			var second = date.getSeconds();
			month = month > 9 ? month : '0' + month
			strDate = strDate > 9 ? strDate : '0' + strDate
			hour = hour > 9 ? hour : '0' + hour
			minute = minute > 9 ? minute : '0' + minute
			second = second > 9 ? second : '0' + second
			var newdata = year + '-' + month + '-' + strDate + ' ' + hour + ':' + minute + ':' + second
			this.time = newdata;
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
	min-height: 600px;
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