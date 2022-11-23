<template>
    <Parent/>
</template>
<script>

    import Parent from "./views/Parent";
    export default {
        components: {Parent}
    }
</script>

<style lang="scss">


nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
