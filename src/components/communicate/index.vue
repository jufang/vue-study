<template>
  <div class="communicate">
    <h2>Parent</h2>
    <h3>{{msg}}</h3>
    <child1 :title="title1" @getmsg="getmsg"></child1>
    <!-- <child2></child2> -->
  </div>
</template>
<script >
import Child1 from "@/components/communicate/Child1";
import Child2 from "@/components/communicate/Child2";

export default {
  name:'communicate',
  provide: {      //选项允许我们指定我们想要提供给后代组件的数据/方法
    woniu: "我是你的老师",
    hhh: (msg)=>{
      this.msg = msg;
    }
  },
  data() {
    return {
      msg:"",
      titleParent:'index.vue 父元素'
    }
  },
  components: {
    Child1,
    Child2
  },
  methods:{
    getmsg(msg){
      this.msg = msg;
    }
  }
}
</script>
<style scoped>
div {
  border: 3px blue solid;
  padding: 10px;
  display: inline-block;
  vertical-align: top;
  /* width:50%; */
}
h1,
h2 {
  font-size: 18px;
  margin: 5px 0;
}
h3 {
  color: red;
  font-size: 14px;
}
</style>