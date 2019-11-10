<template>
<!-- template 에선 최상위 div 한개만 -->
  <div>
    <app-header
      v-bind:propsdata="str"
      v-on:renew="renewStr"></app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'

export default {
  data: function() {
    return {
      str: 'Header'
    }
  },
  components: {
    'app-header': AppHeader
  },
  methods:{
    renewStr: function() {
      this.str = 'hi'
    }
  }
}
</script>

<style>

</style>