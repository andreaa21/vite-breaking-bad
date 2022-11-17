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

    <div class="container debug">
        <SerieSwitcher />
        <CardContainer />
    </div>
  
</template>


<style>

</style>