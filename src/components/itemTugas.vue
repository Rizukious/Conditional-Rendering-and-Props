<template>
    <div>
        <div class="form-check">
            <input class="form-check-input" onclick="" type="checkbox" value="" id="defaultCheck1">
                  <!-- Conditional Rendering Vue-->
                  <!-- and Props -->
            <label class="form-check-label item" v-bind:class="{'item-completed' : tugasSaya.isDone}" for="defaultCheck1">
                    {{tugasSaya.namaTugas}}
            </label>
        </div>
    </div>
</template>

<script>
export default {
    nama : "ItemTugas",
    props : ["tugasSaya"]
};
</script>

<style scoped>

</style>