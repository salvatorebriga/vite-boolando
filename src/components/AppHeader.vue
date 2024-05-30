<script>
  export default {
    name: "AppHeader",
  };
</script>

<template>
  <header>
    <div class="container">
      <div class="row">
        <div class="col-30-left">
          <a href=""> Donna</a>
          <a href=""> Uomo</a>
          <a href=""> Bambini</a>
        </div>
        <div class="col-40">
          <img src="/public/img/boolean-logo.png" alt="logo" />
        </div>
        <div class="col-30-right"></div>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
  header {
    background-color: orange;
    position: fixed;
    z-index: 2;
    box-shadow: 0px 0.2px 0.2px #ff6900;
    border: 0.1px solid rgb(0, 0, 0);
    width: 100%;

    .container {
      width: 1200px;
      margin: 0 auto;

      .row {
        display: flex;
        flex-wrap: wrap;

        .col-30-left {
          width: 30%;
          display: flex;
          justify-content: left;
          align-items: center;
          gap: 25px;
          padding: 20px;

          a {
            font-size: 20px;
            color: white;
            text-decoration: none;

            &:hover {
              text-decoration: underline;
            }
          }
        }
        .col-40 {
          width: 40%;
          display: flex;
          justify-content: center;
          align-items: center;
          padding: 20px;

          img {
            width: 200px;
          }
        }
        .col-30-right {
          width: 30%;
          display: flex;
          justify-content: right;
          align-items: center;
          padding: 20px;
        }
      }
    }
  }
</style>
