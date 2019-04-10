<template>
 <div class="page">
    hello info component
    <button type="button" @click="add()">添加</button>
 </div>
</template>

<script type="text/ecmascript-6">
//@符号代表src目录
import store from '@/store';
export default {
  name: 'Info',
  store,
  data() {
    return {

    }
  },
  //页面加载完成后执行
  mounted () {
    //绑定到 window 对象进行调试
    window.vue = this
  },
  methods: {
    add(){
      console.log("add Event from info!");
      store.commit('increase');
    }
  },
  components: {

  }
}
</script>

<style scoped lang="stylus">
</style>
