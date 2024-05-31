<script>
  export default {};
</script>

<template>
  <div class="col">
    <h3>Trovaci anche su</h3>
    <ul>
      <li><i class="fab fa-twitter-square"></i></li>
      <li><i class="fab fa-facebook-square"></i></li>
      <li><i class="fab fa-instagram-square"></i></li>
      <li><i class="fab fa-pinterest-square"></i></li>
      <li><i class="fab fa-youtube"></i></li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
  .col {
    width: 50%;
    color: white;
    text-align: right;
    h3 {
      margin-bottom: 50px;
    }
    ul {
      display: flex;
      justify-content: right;
      gap: 10px;
      li {
        list-style-type: none;
        i {
          font-size: 25px;
        }
      }
    }
  }
</style>
