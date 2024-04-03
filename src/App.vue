<template>
  <div id="app">
    <h1>Computed Properties in VueJS</h1>
    <h2>Full Name is  {{ firstName }} {{ lastName }}</h2>
    <h2>Computed Full Name is  {{ fullName }}</h2>
    <h2>Total Price is  {{ total }}</h2>
    
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      firstName:'Ashok',
      lastName:'Amara',
      items:[
        {
          id:1,
          title:'Tv',
          price:100
        },
        {
          id:2,
          title:'Phone',
          price:200
        },
        {
          id:3,
          title:'Laptop',
          price:300
        },
      ],
    }
  },
  methods:{

  },
  computed:{
    fullName(){
      return `${this.firstName} ${this.lastName}`
    },
    total(){
      return this.items.reduce((total, curr) => (total = total+ curr.price), 0)
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
