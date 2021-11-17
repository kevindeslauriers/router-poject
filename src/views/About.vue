<template>
  <div class="about">
    <h1 @click="test">This is an about page</h1>
    {{info}}
  </div>
</template>

<script>

export default {
  name: 'About',
  methods: {
    test(){
     this.$router.push({path : '/'})
    }
  },
  data() {
    return {
      info : Array
    }
  },
  props:['msg1'],
  mounted() {
    if (this.msg1){
      this.info = JSON.parse(this.msg1);
      console.log(this.info);
    }
  }
}
</script>
