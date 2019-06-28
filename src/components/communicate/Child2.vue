<template>
  <div>
      <h2>Child2</h2>
      <h3>{{msg}}</h3>
      <p>祖先元素提供的数据 : {{woniu}}</p>
  </div>
</template>
<script>
export default {
  name:'child2',
  inject:['woniu'],
  data() {
    return {
      msg:"",
    }
  },
}
</script>
