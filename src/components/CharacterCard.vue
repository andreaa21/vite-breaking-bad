<script>
export default {
    name: 'CharacterCard',
    props:{
        character: Object
    }

}
</script>

<template>
  
    <div class="x-card">
        <!-- img name status category -->
        {{character.name}}
    </div>

</template>



<style lang="scss" scoped>

@use '../styles/partials/vars' as *;

.xcard{
    color: black;
}

</style>