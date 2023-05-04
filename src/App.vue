<template>

   <MyHeader ProjectTitle="First Ten American Presidents" Country="USA" />
   <PresidentBox :pDetails=pDetails />
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import PresidentBox from './components/PresidentBox.vue';

export default {
  name: 'App',

  
  components: {
    MyHeader,
    PresidentBox
  },
  data(){
    return {
      pDetails: []
    } 
  },
  methods:{
    async fetchpDetails(){
      const res = await fetch('https://sai-sri-harsha-backend.onrender.com/api');
      const data = await res.json();
      console.log(data);
      return data;
    }
  },
  async created(){
    this.pDetails = await this.fetchpDetails();
  }

}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;

}


</style>

