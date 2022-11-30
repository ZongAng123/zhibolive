<template>
  <div class="hello">
    <div class="shipinone">
      <h1>点播演示</h1>
      <LivePlayer class="videostr1" :videoUrl="mp4URL"/>
   </div>
  </div>
</template>

<script>
import LivePlayer from '@liveqing/liveplayer'

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
     LivePlayer,   
  },
  computed:{
    mp4URL() {
        return "填写你们公司自己的业务的mp4地址"
    },
    flvURL() {     
        return "填写你们公司flv地址"
    },
  },
  methods: {
      snapOutside: function (snapData) {
         alert(snapData)
      },

  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello{
  display: align;
  background-color: blue;
}
.shipinone{
  display: flex;
  height: 400px;
}

.videostr1{
  margin-top: 80px;
  margin-left: 70px;
  width:500px;
  height:390px;
}

</style>
