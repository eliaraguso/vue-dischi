<template>
  <div class="album">
      <img :src="info.poster" alt="">
      <h2>{{info.title}}</h2>
      <p>{{info.author}}</p>
      <p>{{info.year}}</p>
  </div>
</template>

<script>
export default {
    name: "Album",
    props: ['info']
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';

  .album {
    text-align: center;
    background-color: $componentsBlue;
    width: calc((100% / 5) - 40px);
    display: flex;
    flex-direction: column;
    padding: 15px 15px 80px 15px;
    margin: 10px 20px;

    h2 {
      color: $albumTitle;
      padding: 20px 0;
    }
    p {
      color: $albumInfo;
    }
  }
</style>