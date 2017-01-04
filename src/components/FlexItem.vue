<template>
  <div :style="style" class="flexitem">
    <slot></slot>
  </div>
</template>

<script>
function getRandomColor() {
    var letters = '0123456789ABCDEF';
    var color = '#';
    for (var i = 0; i < 6; i++ ) {
        color += letters[Math.floor(Math.random() * 16)];
    }
    return color;
}


export default {
  name: 'flexitem',
  props: {
    w: {
      type: String,
      default: "100px"
    },
    h: {
      type: String,
      default: "200px"
    },
    grow: {
      type: Number,
      default: 1
    },
    shrink: {
      type: Number,
      default: 0
    },
    color: {
      default: getRandomColor
    }
  },
  computed: {
    style: function() {
      return {
        "background-color": this.color,
        "flex-grow": this.grow,
        "flex-shrink": this.shrink,
        "flex-basis": this.w,
        //"min-width": this.w,
        "min-height": this.h
      }
    }
  },
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .flexitem:hover {
    opacity: 0.5;
    cursor: pointer;
  }
</style>
