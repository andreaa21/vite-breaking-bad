  <script>

  import axios from 'axios';
  import {store} from './data/store'

  import AppHeader from './components/AppHeader.vue';
  import SerieSwitcher from './components/SerieSwitcher.vue';
  import CharacterCard from './components/CharacterCard.vue';
  import CardContainer from './components/CardContainer.vue';


  export default {
    name: 'App',
    data(){
      return{
        store
      }
    },
    components:{
      AppHeader,
      CharacterCard,
      CardContainer,
      SerieSwitcher
    },
    methods: {
      getCharacters(){
        axios.get(store.apiUrl)
        .then( result => {
          store.characterData = result.data;
          console.log(store.characterData);
        })
        .catch( error =>{
          console.log(error);
        })
        }
    },
    mounted(){
      this.getCharacters();
    }
  }
  </script>

<template>
  <AppHeader title="breaking bad api"/>
  <main>
    <SerieSwitcher />
    <CardContainer />
  </main>
  
</template>


<style lang="scss">

  @use './styles/general.scss';
  @use './styles/partials/vars' as *;


  body{
    background-color: $primary-color;
  }
</style>