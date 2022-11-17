<script>

import SerieSwitcher from './SerieSwitcher.vue';
import CardContainer from './CardContainer.vue';

export default {
    name: 'AppMain',
    components:{
        SerieSwitcher,
        CardContainer
    }
}
</script>
    
<template>

    <div class="container">
        <SerieSwitcher />
        <CardContainer />
    </div>
  
</template>


<style>

</style>