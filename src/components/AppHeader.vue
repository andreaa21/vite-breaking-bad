<script>
export default {
    name: 'AppHeader',
    props:{
        title: String
    }
}
</script>

<template>
  <div class="header-content p-3 d-flex">
    <div class="logo me-3">
        <img src="../assets/img/Breaking_Bad_logo.svg" alt="Logo">
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