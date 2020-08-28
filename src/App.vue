<template>
  <div id="app">
    <caijian ref='caijian' :isShow='isShow'></caijian>
    <!-- 演示 -->
    <button @click='chose'>选择图片</button>
     <button  @click='show'>展示图片</button>
     <button @click='down'>下载图片</button>
     <button>上传图片</button>
     <div>
        <img :src="img" alt="">
     </div>
  </div>
</template>

<script>
import caijian from './components/caijian.vue'

export default {
  name: 'App',
  components: {
    caijian
  },
  data(){
    return{
        isShow:false,
    img:''
    }
  },
  methods:{
    chose(){
      this.$refs.caijian.iptClick()
      this.isShow=true
    },
    show(){
       this.img=this.$refs.caijian. localhostShow()
    },
    down(){
      this.$refs.caijian.localhostDown()
    }
  }
}
</script>

<style>
#app{
  margin-top:200px;
  margin-left:200px;
}
</style>
