<template>
    <header id="header">
        <img src="../assets/images/spotify-logo.png" alt="Spotify logo image">
        <select name="" id="selezione-generi" v-model="Genre" @change="$emit('selectGenres','Genre')">
            <option value="">Seleziona un genere</option>
            <option value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>
        </select>
    </header>
</template>

<script>
export default {
    name: "Header",
    data() {
        return {
            Genre: ""
        }
    },
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';
    #header {
        height: 4.375rem;
        background-color: $componentsBlue;
        display: flex;
        align-items: center;
        justify-content: space-between;
        img {
            height: 2.8125rem;
            padding-left: 1.25rem;
        }
        #selezione-generi {
            margin-right: 1.25rem;
            padding: .3125rem;
        }
    }

</style>