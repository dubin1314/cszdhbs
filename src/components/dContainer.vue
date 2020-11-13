<template>
  <div class="dontainer">
    <div class="title">
      <span></span>
      <b>项目内容</b>
      <span></span>
    </div>
    <div>
     <el-row :gutter="40">
      <el-col :span="6" v-for="(item,num) in list" :key="num" class="ProjectDescription">
        <el-image style="width:226px" :src="$baseUrl+item.url"></el-image>
          <div class="marginTop_30">
<b >{{item.title}}</b>
          </div>
          <div class="marginTop_20">
            <div v-for="(items,n) in item.desc" :key="n+num" class="is-flex is-flex-justify-content-center">
              <div v-for="i in items" :key="i" class="projectDesc">
                <span>{{i}}</span>
              </div>
            </div>
          </div>
      </el-col>
</el-row>
    </div>
  </div>
</template>
<script>
export default {
  name: 'dContainer',
  props: {
    msg: String
  },
  data(){
    return{
      list:[
        {url:'g1.png',title:'美容',desc:[['深层清洁','祛斑祛痘'],['修复抗敏','补水保湿'],['美白亮肤','抗衰提升']]},
        {url:'g2.png',title:'养生',desc:[['肩颈保养','乳腺疏通'],['暖宫护巢','腰肾保养'],['骨盆修复','全身经络']]},
        {url:'g3.png',title:'美体',desc:[['专注易瘦体质调理'],['不吃药不打针不节食'],['签约减重','无效退款']]},
        {url:'g4.png',title:'其他',desc:[['美甲美睫'],['激光无痛脱毛'],['半永久丝雾仿生眉']]},
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
 @media only screen and (min-width: 1700px){
.dontainer{
  margin-top: 130px;
}
  }
    @media only screen and (min-width: 768px) and  (max-width: 1700px){
  .dontainer{
  margin-top: 80px;
}}
@media only screen and (max-width: 768px) {
   .ProjectDescription {
      width: 100%;
    }
 .ProjectDescription +.ProjectDescription{
      margin-top: 20px;
    }
  }
  .title{
    display: flex;
    justify-content: center;
    margin-bottom: 40px;
    align-items:center;
    span{
      display: inline-block;
      width: 40px;
      height: 2px;
      background: #333333;
      border-radius: 2px;
      margin:0 10px;
    }
    b{
      font-size: 24px;
      font-weight: 500;
      text-align: center;
      color: #333333;
      line-height: 40px;
    }
  }
  .ProjectDescription{
      display: flex;
      flex-direction: column;
      align-items: center;
      b{
        font-size: 22px;
        font-weight: 500;
        text-align: center;
        color: #333333;
        line-height: 30px;
        border-bottom: 4px solid #5ccdaf;
      }
      span{
        font-size: 18px;
        font-weight: 400;
        text-align: center;
        color: #666666;
        line-height: 30px;
      }
      .projectDesc{
        margin-top: 12px;
      }
      .projectDesc+.projectDesc{
        margin-left: 40px;
      }
  }
</style>
  

