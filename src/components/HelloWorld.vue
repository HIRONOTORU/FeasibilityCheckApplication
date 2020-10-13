<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button v-on:click="msg += 'kick!'">kick me!</button>
    <p>
      <inut type="text" v-model="name" /><br />
      {{name}}
    <p/>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return{
      name:""
    }
  },
  props: {
    msg: String
  },
  methods:{
    kick:function (event){
      this.msg+="kick!";
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
