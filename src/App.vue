<template>
  <h2>Add method - {{ add() }}</h2>
  <h2>Multiply method - {{ multiply(3) }}</h2>
  <h2>{{ name }}</h2>
  <button @click=changeName()>Change Name</button>
  <h2>Count - {{ count }}</h2>
  <div>
    <button @click=increment()>Increment</button>
    <button @click=decrement()>Decrement</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      baseMultiplier : 5,
      name : 'Zayarwin',
      count:1
    }
  },
  methods : {
    add(){
      return 2 + 3 + 5
    },
    multiply(num){
      return num * this.baseMultiplier
    },
    changeName(){
      return this.name = 'Batman'
    },
    increment(){
      this.count += 1;
    },
    decrement(){
      this.count -=1;
    }
  }
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px; 
}
</style>
