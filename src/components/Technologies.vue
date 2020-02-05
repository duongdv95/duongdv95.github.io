<template>
  <div class="technologies">
    <div class="technologies-images">
      <img src='@/assets/css.svg'/>
      <img src='@/assets/html.svg'/>
      <img src='@/assets/javascript.png'/>
      <img src='@/assets/node.png'/>
      <img src='@/assets/react.png'/>
      <img src='@/assets/vue.png'/>
      <img src='@/assets/dynamodb.png'/>
      <img src='@/assets/s3.png'/>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Technologies',
  props: {
    techUsed: {
      type: Array
    }
  },
  data: () => {
    return {
      techUsed: this.techUsed
    }
  },
  methods: {
    logg () {
      console.log(this.techUsed)
    }
  },
  created () {
    this.logg()
  }
}

</script>

<style scoped lang="scss">
.technologies {
  margin: 1em 0;
}
.technologies .technologies-images {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  img {
    height: 60px;
    padding: 1em;
  }
}
</style>
