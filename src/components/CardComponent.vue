<template>
    <div class="card">
      <img :src="image" />
      <p id="title">{{ title }}</p>
      <Button :url="sitio"/>
    </div>
  </template>
  
  <script>
  import Button from './ButtonComponent.vue'
  export default {
    name: "CardComponent",
    props:{
        image:String,
        title:String,
        sitio:String
    },
    components:{
        Button
    }
  };
  </script>
  
  <style scoped>
  img {
    width: 50%;
  }
  #title{
    color: #070a52;
    font-weight: bolder;
    font-size: 24px;
  }
  .card{
    background-color: aliceblue;
    border: 2px solid #78c1f3;
    width: 30%;
    margin: 10px;
    border-radius: 30px;
    text-align: center;
    padding: 2%;
  }
  </style>