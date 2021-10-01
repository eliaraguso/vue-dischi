<template>
  <div class="album">
      <img src="https://cdn2.jazztimes.com/2018/05/SteveGadd-800x723.jpg" alt="">
      <h2>NEW JERSEY</h2>
      <p>Bon Jovi</p>
      <p>1988</p>
  </div>
</template>

<script>
export default {
    name: "Component"
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