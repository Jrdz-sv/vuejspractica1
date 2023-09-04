<template>
    <a :href="url" target="_blank" id="button">Ir a sitio official</a>
</template>

<script>
export default{
    name: 'ButtonComponent',
    props:{
        url:String
    }
}
</script>

<style>
#button{
    background-color: #007bff;
    color: aliceblue;
    padding: 1%;
    border-radius: 20px;
    text-decoration: none;
}
</style>