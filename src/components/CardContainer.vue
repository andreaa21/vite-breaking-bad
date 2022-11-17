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

    <div class="container x-container">
        <div class="wrapper p-5">
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

.x-container{
    margin-bottom: 100px;
}

.wrapper{
    height: 100vh;
    background-color: white;
    overflow: auto;
    .cards{
        margin-bottom: 50px;
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