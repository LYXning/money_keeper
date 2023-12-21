<template>
  <div class="back">
    <img src="../assets/icon/back.png" height="16" width="16"/></div>
  <div class="top">
    <div class="title">
      <div style="text-align: center">2023年11账单</div>
    </div>
  </div>
  <div class="main" style="height: 844px">
    <div class="overview">
      <div class="bill">11月账单</div>
      <div class="surplus">
        <div class="surplus_this">本月结余</div>
        <div class="surplus_money" id="this">-100.00</div>
        <div class="surplus_last">上月结余</div>
        <div class="surplus_money" id="last">200.00</div>
      </div>
      <div class="output">
        <div class="output_name">支出</div>
        <div class="output_chart">
          <img src="../assets/icon/支出条形图.png" height="10" width="170"/></div>
        <div class="output_money">500.00</div>
      </div>
      <div class="input">
        <div class="input_name">收入</div>
        <div class="input_chart">
          <img src="../assets/icon/收入条形图.png" height="10" width="136"/></div>
        <div class="input_money">400.00</div>
      </div>
    </div>
    <div class="category" style="width: 390px; background-color: #ffffff; position:relative; top: 10px; height: 380px">
      <div class="output_category" style="position: relative; top: 15px; left: 16px">支出类别</div>
      <div class="output_category_chart" style="position: absolute; top: 70px; left: 16px">
        <img src="../assets/icon/支出饼状图.png" height="110" width="110"/></div>
      <div class="detail">
        <div class="kind" style="display: inline-block; position: absolute; top: 90px; left: 150px; font-size: 10px">
          <div style="">类别</div>
          <div class="mingxi" style="position: relative; top: 5px">
            <img src="../assets/icon/蓝色.png" height="12" width="12"/> 餐饮
          </div>
          <div class="mingxi" style="position: relative; top: 10px">
            <img src="../assets/icon/绿色.png" height="12" width="12"/> 购物
          </div>
        </div>
        <div class="proportion"
             style="display:inline-block; position: absolute; top: 90px; right: 115px; font-size: 10px; text-align: right">
          <div>占比</div>
          <div style="position: relative; top: 5px">63.6%</div>
          <div style="position: relative; top: 10px">36.4%</div>
        </div>
        <div class="amount"
             style="display: inline-block; position: absolute; top: 90px; right: 20px; font-size: 10px; text-align: right">
          <div>金额</div>
          <div style="position: relative; top: 5px">318</div>
          <div style="position: relative; top: 10px">182</div>
        </div>
      </div>
      <div class="output_rank" style="width: 390px; background-color: #ffffff; position:relative; top: 180px">
        <div style="position: relative; left: 15px; font-size: 12px">支出排行</div>
        <div class="rank" style="position: relative; top: 20px; left: 15px; font-size: 10px">
          <div class="line" style="display: flex; align-items: center; height: 45px">
            <div class="remark" style="width: 40px; line-height: 12px; font-size: 10px">1</div>
            <div class="remark" style="width: 60px"><img src="../assets/icon/food_.png" height="35" width="35"/></div>
            <div class="remark" style="width: 50px; line-height: 17px; font-size: 10px">餐饮<br/>11月17日</div>
            <div class="remark" style="width: 205px; line-height: 12px; font-size: 10px; text-align: right">-216</div>
          </div>
          <div class="line" style="display: flex; align-items: center; height: 45px">
            <div class="remark" style="width: 40px; line-height: 12px; font-size: 10px">2</div>
            <div class="remark" style="width: 60px"><img src="../assets/icon/shopping_.png" height="35" width="35"/></div>
            <div class="remark" style="width: 50px; line-height: 17px; font-size: 10px">购物<br/>11月17日</div>
            <div class="remark" style="width: 205px; line-height: 12px; font-size: 10px; text-align: right">-108</div>
          </div>
          <div class="line" style="display: flex; align-items: center; height: 45px">
            <div class="remark" style="width: 40px; line-height: 12px; font-size: 10px">3</div>
            <div class="remark" style="width: 60px"><img src="../assets/icon/shopping_.png" height="35" width="35"/></div>
            <div class="remark" style="width: 50px; line-height: 17px; font-size: 10px">餐饮<br/>11月17日</div>
            <div class="remark" style="width: 205px; line-height: 12px; font-size: 10px; text-align: right">-72</div>
          </div>
        </div>
      </div>
    </div>
    <div class="tendency" style="width: 390px; background-color: #ffffff; position:relative; top: 20px; height: 300px">
      <div class="output_category" style="position: relative; top: 15px; left: 16px">支出趋势</div>
      <div class="line" style="display: flex; align-items: center; height: 45px; position: relative; left: 15px; top: 10px">
        <div class="remark" style="width: 130px; line-height: 12px; font-size: 11px">单日支出最高</div>
        <div class="remark" style="width: 120px; line-height: 12px; font-size: 11px; color: #6f6f6f">日均支出</div>
        <div class="remark" style="width: 120px; line-height: 12px; font-size: 11px; color: #6f6f6f">本月支出</div>
      </div>
      <div class="line" style="display: flex; align-items: center; height: 20px; position: relative; left: 15px;">
        <div class="remark" style="width: 130px; line-height: 12px; font-size: 20px; font-weight: bold">246.00</div>
        <div class="remark" style="width: 120px; line-height: 12px; font-size: 20px; font-weight: bold; color: #6f6f6f">16.67</div>
        <div class="remark" style="width: 120px; line-height: 12px; font-size: 20px; font-weight: bold; color: #6f6f6f">500</div>
      </div>
      <div class="line" style="display: flex; align-items: center; height: 20px; position: relative; left: 15px; top: 10px">
        <div class="remark" style="width: 130px; line-height: 12px; font-size: 11px">11月17日</div>
      </div>
      <div><img src="../assets/icon/折线图.png" height="184" width="390"/></div>
    </div>
  </div>
</template>

<script>

</script>

<style>
body {
  background-color: #f5f6f8;
  padding: 0;
  margin: 0;
  border: 0;
  overflow: hidden;
}

html {
  padding: 0;
  margin: 0;
  border: 0;
}

div {
  padding: 0;
  margin: 0;
  border: 0;
}

.top {
  background-color: #feda46;
  width: 390px;
  height: 40px;

}

.title {
  width: 334px;
  height: 40px;
  line-height: 40px;
  text-align: center;
}

.back {
  float: left;
  margin-left: 18px;
  margin-top: 12px;
}
.main {
  overflow-y: scroll;
}
.overview {
  background-color: #ffffff;
  width: 390px;
  height: 180px;
}

.bill {
  position: relative;
  top: 20px;
  left: 15px;
  font-size: 14px;
  font-weight: bold;
}

.surplus {
  display: block;
}

.surplus_this {
  position: relative;
  top: 25px;
  left: 15px;
  font-size: 12px;
  display: inline-block;
}

.surplus_last {
  position: relative;
  top: 25px;
  left: 95px;
  font-size: 12px;
  color: #6f6f6f;
  display: inline-block;
}

.surplus_money {
  position: relative;
  top: 50px;
  font-size: 20px;
  font-weight: bold;
  display: inline-block;
}

#this {
  left: -32px;
}

#last {
    left: 48px;
  color: #6f6f6f;
}

.output div {
  display: inline-block;
  position: relative;
}

.output_name {
  top: 70px;
  left: 25px;
  font-size: 10px;
}

.output_chart {
  top: 70px;
  left: 35px;
}

.output_money {
  top: 70px;
  left: 40px;
  font-size: 12px;
}

.input div {
  display: inline-block;
  position: relative;
}

.input_name {
  top: 70px;
  left: 25px;
  font-size: 10px;
}

.input_chart {
  top: 70px;
  left: 35px;
}

.input_money {
  top: 70px;
  left: 40px;
  font-size: 12px;
}

.mingxi {
  font-size: 10px;
  line-height: 10px;
  height: 12px;
  display: flex;
  align-items: center;
}
</style>