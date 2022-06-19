<template>
  <div>
    <app-header 
      v-bind:propsdata="str" 
      v-on:renew="renewStr"
    ></app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
/*
  const AppHeader = {
    template: '<header><h1>Header</h1></header>'
  }
*/

/* 
  new Vue({
    data: {
      str: 'hi',
    }
  })
*/

export default {
  // 객체가 아닌 function을 사용
  data: function() {
    return {
      str: 'Header'
    }
  },
  components: {
    'app-header': AppHeader
  },
  methods: {
    renewStr: function() {
      this.str = 'hi';
    }
  }
}
</script>

<style>

</style>