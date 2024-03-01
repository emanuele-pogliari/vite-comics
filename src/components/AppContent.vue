<script>
export default {
    data() {
        return {


        }
    },
    name: 'AppContent',
}
</script>

<template>
    <div class="content-container">
        <div class="content"> -> Content goes here </div>
    </div>
</template>

<style lang="scss">
@use '../src/styles/variables' as *;
@use '../src/styles/mixins' as *;

.content-container {
    background-color: #303030;
    color: white;

    .content {
        width: 70%;
        margin: auto;
        padding-top: 55px;
        padding-bottom: 45px;
        font-size: 28px;
    }
}
</style>

