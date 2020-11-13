<template>
  <div class="dfooter">
      <div>
        <p v-for="(item,n) in list" :key="n">{{item}}</p>
        <p><a href="https://beian.miit.gov.cn/" target="_blank">晋ICP备2020011025号-1</a></p>
      </div>
      <div>
          <el-image :preview-src-list="srcList" style="width:114px;" :src="erweima"></el-image>
      </div>
  </div>
  
</template>

<script>
export default {
  name: 'dFooter',
  props: {
    msg: String
  },
  data(){
    return{
      srcList:[this.$baseUrl+'erweima.png'],
      list:['联系电话：0351-5268277',
      '企业名称：太原玖美荟美容养生有限公司',
      '门店地址：太原市新屯巷大唐惠泽园16号楼8号商铺2楼玖美荟大唐店',
      '商务合作：17703518277'],
      erweima:this.$baseUrl+'erweima.png'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.dfooter{
  height: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  p{
    font-size: 14px;
    font-weight: 400;
    text-align: left;
    color: #f0f0f0;
    margin-top: 12px;
    a{
       color: #f0f0f0;
    }
  }
}
@media only screen and (max-width: 768px) {

  }
</style>
<style>
.el-image-viewer__close{
  color:#fff;
}
</style>
  

