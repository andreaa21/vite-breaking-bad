<script>
export default {
    name: 'CharacterCard',
    props:{
        character: Object
    }

}
</script>

<template>
  
    <div class="x-card col-2 p-3">
        <!-- img name status category -->
        <div class="card-image">
            <img :src="character.img" :alt="character.name">
        </div>
        <div class="card-text text-center">
            <div class="char-name my-3">
                <span>{{character.name}}</span>
            </div>
            <div class="char-category my-2">
                <span>{{character.category}}</span>
            </div>
            <div class="char-status">
                <span>{{character.status}}</span>
            </div>
        </div>
    </div>

</template>



<style lang="scss" scoped>

@use '../styles/partials/vars' as *;

.x-card{
    height: 400px;
    padding: .5rem;
    margin: 1rem;
    background-color: $primary-color;
    .card-text{
        color: darkgrey;
    }
    .char-name{
        font-weight: 600;
        text-transform: uppercase;
        color: white;
    }
}

</style>