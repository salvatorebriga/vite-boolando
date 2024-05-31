<script>
  export default {};
</script>

<template>
  <div class="col">
    <h2>Boolando S.R.L</h2>
    <ul>
      <li><a href="">Informazioni legali</a></li>
      <li><a href="">Informativa sulla privacy</a></li>
      <li><a href="">Diritto di recesso</a></li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
  .col {
    width: 50%;
    color: white;
    h2 {
      margin-bottom: 50px;
    }
    ul {
      display: flex;
      gap: 10px;
      li {
        list-style-type: none;
        a {
          color: white;
          text-decoration: none;

          &:hover {
            text-decoration: underline;
          }
        }
      }
    }
  }
</style>
