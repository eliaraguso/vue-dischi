<template>
    <section class="albums">
        <div class="container">
            <Album v-for="(album, index) in albums" :key="index" :info="album"/>
        </div>
    </section>
</template>

<script>
import axios from 'axios';
import Album from './Album.vue';

export default {
    name:"Albums",
    components : {
        Album
    },
    data() {
        return {
            albums: []
        }
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then( (response) => {
                this.albums = response.data.response;
            });
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';

.albums {
    background-color: $backgroundBlue;
    height: calc(100vh - 4.375rem);
    display: flex;
    
    .container {
        display: flex;
        flex-wrap: wrap;
        width: 60%;
        margin: auto;
        max-width: 72.5rem;
    }
}

</style>