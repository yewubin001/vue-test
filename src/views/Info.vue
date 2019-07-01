<template>
  <div>
    hello info component
    <button type="button" @click="add()">添加</button>
  </div>
</template>

<script>
  import store from '@/store';
  export default {
    name: 'Info',
    store,
    data() {
      return {
        msg: 'hello vue'
      };
    },
    mounted() {
      window.vue = this;
    },
    methods: {
      add() {
        console.log('add Event from info!');
        // alert('alert from info')
        debugger;
        store.commit('increase');
      },
      output() {
        console.log('in output');
      }
    },
  };
</script>

<style scoped>

</style>
