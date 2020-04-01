<template>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
         <a class="navbar-brand" href="#">{{ titleNav }}</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            titleNav: 'Ricky & Morthy Api',
        }
    }
}
</script>

<style scoped>
    
</style>