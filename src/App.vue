<template>
  <div id="app">
      <h1> Awesome Blogs </h1>
      <button @click="toggle">Click for Awesome</button>
      <section v-if='showForm'>
        <h3>Add new blog post:</h3>
      </section>
      <section v-else>
        <h3>All posts:</h3>
      </section>
      
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {  //don't use arrow functions in vue, but you can use ES6 method syntax.
    return {
      showForm:true
    }
  },
  methods:{
    toggle: function() {
      this.showForm = !this.showForm
    }
  }
}
</script>

<style >
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
