<template>
  <div class="is-flex ">
    <div class="textAlign-left leftStyle">
      <el-image style="width:138px" :src="bgurl"></el-image>
      <div class="componeyDesc">
        <h3>专注美容养生二十年</h3>
        <h3 class="marginTop_20">让你美得更久</h3>
        <p>
          汇集知名美业厂家的产品和项目,以匠人精神认真做好每一次服务,以放心品质满足你每一个对美的期望~
        </p>
      </div>
      <div class="desc">
        <span>我们坚信好的产品+好的服务=好的效果</span>
      </div>
    </div>
    <div class="flex-1">
      <div class="imageContainer">
        <el-image class="imagezsy" :src="rightUrl"></el-image>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'dHeader',
  props: {
    msg: String,
  },
  data() {
    return {
      bgurl: this.$baseUrl+'bjlog.png',
      rightUrl: this.$baseUrl+'rightBg.png'
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.leftStyle {
  width: 493px;
}
.componeyDesc {
  width: 100%;
  margin-top: 168px;
  h3 {
    height: 56px;
    font-size: 40px;
    font-weight: 600;
    text-align: left;
    color: #333333;
    line-height: 56px;
  }
  p {
    margin-top: 38px;
    font-size: 18px;
    font-weight: 400;
    text-align: justify;
    color: #666666;
    line-height: 28px;
  }
}
.imageContainer {
  position: absolute;
  right: 0;
  top: 0;
}
@media only screen and (min-width: 1700px) {
  .desc {
    margin-top: 168px;
  }
  .imagezsy {
    width: 978px;
  }
}
@media only screen and (min-width: 1300px) and (max-width: 1700px) {
  .desc {
    margin-top: 50px;
  }
  .imagezsy {
    width: 700px;
  }
}
@media only screen and (min-width: 1024px) and (max-width: 1300px) {
  .desc {
    margin-top: 50px;
  }
  .imagezsy {
    width: 650px;
  }
  .leftStyle {
    width: 360px;
  }
}
@media only screen and (max-width: 768px) {
  .imagezsy {
   display: none;
  }
   .leftStyle {
    width: 100%;
  }
}
.desc {
  height: 28px;
  font-size: 18px;
  font-weight: 500;
  text-align: left;
  color: #333333;
  line-height: 28px;
  span {
    border-bottom: 4px solid #5ccdaf;
  }
}
</style>
