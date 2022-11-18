<script>

import {store} from '../data/store'

export default {
    name: 'SerieSwitcher',
    data(){
        return{
            store
        }
    }

}
</script>


<template>

    <div class="container">
        <div class="select-container p-3">
            <select 
            @click="$emit('startSearch')"
            v-model="store.categorySearch"
            class="form-select">
                <option value="" selected>Choose Category</option>
                <option value="Breaking Bad">Breaking Bad</option>
                <option value="Better Call Saul">Better Call Saul</option>
                <option value="Breaking Bad, Better Call Saul">Both</option>
            </select>
        </div>
    </div>
  
</template>


<style lang="scss" scoped>

.form-select{
    width: 200px;
}

</style>