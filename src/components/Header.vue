<template>
    <header id="header">
        <img src="../assets/images/spotify-logo.png" alt="Spotify logo image">
    </header>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';
    #header {
        height: 4.375rem;
        background-color: $componentsBlue;
        display: flex;
        align-items: center;
        img {
            height: 2.8125rem;
            padding-left: 1.25rem;
        }
    }

</style>