<template>
  <div :style="style">
  </div>
</template>

<script>
export default {
  name: 'flexitem',
  data () {
    return {
      style: {
        "background-color": "#51aa9f",
        "flex-grow": 5,
        width: "100px",
        "min-height": "200px"
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
