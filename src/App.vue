<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link :to="{ name: 'About', params: { msg1 } }">About</router-link>
  </div>
  <router-view/>
</template>

<script>

export default ({
 data(){
   return{
     msg:Array,
     msg1:String
   }
 },
 mounted() {
   this.msg = new Array(3);
   this.msg[0] = {};
    this.msg[1] = {};
    this.msg[2] = {};

   this.msg[0]['test'] = '1';
   this.msg[0]['id'] = '1234';
   this.msg[1]['test'] = '1';
   this.msg[1]['id'] = '1234';
   this.msg[2]['test'] = '1';
   this.msg[2]['id'] = '1234';
   this.msg1 = JSON.stringify(this.msg);
 },
})
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
