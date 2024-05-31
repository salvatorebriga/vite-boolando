<script>
  import ColLeft from "./ColLeft.vue";
  import Logo from "./Logo.vue";
  import ColRight from "./ColRight.vue";
  export default {
    name: "AppHeader",
    components: {
      ColLeft,
      ColRight,
      Logo,
    },
  };
</script>

<template>
  <header>
    <div class="container">
      <div class="row">
        <ColLeft class="colLeft" />
        <Logo class="logo" />
        <ColRight class="colRight" />
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
  header {
    position: fixed;
    z-index: 1;
    background-color: #ff6900;
    box-shadow: 0px 0.2px 0.2px #ff6900;
    border: 0.1px solid rgb(0, 0, 0);
    width: 100%;

    .container {
      max-width: 1200px;
      margin: 0 auto;

      .row {
        display: flex;
        flex-wrap: wrap;
      }
    }
  }

  @media screen and (max-width: 720px) {
    header {
      .container {
        .row {
          .colLeft {
            width: 50%;
          }

          .logo {
            width: 50%;
          }

          .colRight {
            display: none;
          }
        }
      }
    }
  }

  @media screen and (max-width: 500px) {
    header {
      .container {
        .row {
          .colLeft {
            display: none;
          }

          .logo {
            width: 100%;
          }

          .colRight {
            display: none;
          }
        }
      }
    }
  }
</style>
