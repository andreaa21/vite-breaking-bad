<script>

import { store } from '../data/store'

import CharacterCard from './CharacterCard.vue'

export default {
    name: 'CardContainer',
    components:{
        CharacterCard
    },
    data(){
        return{
            store
        }
    }

}
</script>


<template>

    <div class="container">
        <div class="wrapper">
            <div class="finder d-flex align-items-center">
                <span class="px-3">found 62 characters</span>
            </div>
            <div class="cards mt-3 d-flex flex-wrap">
                <CharacterCard 
                    v-for="character in store.characterData" 
                    :key="character.char_id"
                    :character="character"/>
            </div>
         </div>
    </div>

</template>


<style lang="scss" scoped>

@use '../styles/partials/vars' as *;

.wrapper{
    height: 100vh;
    background-color: white;
    padding: 50px;
    overflow: hidden;
    .cards{
        overflow-y: scroll;
        max-height: 100vh;
    }
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