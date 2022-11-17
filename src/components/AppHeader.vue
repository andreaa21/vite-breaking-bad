<script>
export default {
    name: 'AppHeader',
    props:{
        title: String
    },
    methods:{
	    getImagePath(imageName){
	    	return new URL (`./assets/img/${imageName}`, import.meta.url).href
	    }
    }
}
</script>

<template>
  <div class="header-content p-3 d-flex">
    <div class="logo me-3">
        <img :src="getImagePath('Breaking_Bad_logo.svg')" alt="Logo">
    </div>
    <h1>{{title}}</h1>
  </div>
  
</template>



<style lang="scss" scoped>
    h1{
        color: white;
        text-transform: capitalize;
        font-weight: 600;
    }
</style>