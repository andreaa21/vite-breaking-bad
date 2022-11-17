<script>
export default {
    name: 'SerieSwitcher'

}
</script>


<template>

    <div class="container">
        <div class="select-container p-3">
            <select class="form-select" aria-label="Default select example">
                <option value="1">Breaking Bad</option>
                <option value="2">Better Call Saul</option>
                <option value="3">Both</option>
            </select>
        </div>
    </div>
  
</template>


<style lang="scss" scoped>

.form-select{
    width: 200px;
}

</style>