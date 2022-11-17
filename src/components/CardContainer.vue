<script>
export default {
    name: 'CardContainer'

}
</script>


<template>

  <div class="wrapper">
    <div class="finder d-flex align-items-center">
        <span class="px-3">found 62 characters</span>
    </div>
    <div class="cards d-flex flex-wrap"></div>
  </div>

</template>


<style lang="scss" scoped>

@use '../styles/partials/vars' as *;

.wrapper{
    height: 100vh;
    background-color: white;
    padding: 50px;
    .finder{
        background-color: $finder-color;
        min-height: 60px;
        span{
            color: white;
            text-transform:capitalize;
            font-weight: 600;
        }
    }
}

</style>