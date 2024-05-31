<script>
  export default {
    name: "ColLeft",
  };
</script>
<template>
  <div class="col">
    <a href=""> Donna</a>
    <a href=""> Uomo</a>
    <a href=""> Bambini</a>
  </div>
</template>

<style lang="scss" scoped>
  .col {
    width: 30%;
    display: flex;
    justify-content: left;
    align-items: center;
    gap: 25px;
    padding: 20px;

    a {
      font-size: 20px;
      font-weight: 600;
      color: white;
      text-decoration: none;

      &:hover {
        text-decoration: underline;
        color: black;
      }
    }
  }
</style>
