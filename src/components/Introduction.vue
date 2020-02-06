<template>
  <div class="introduction">
    <div class="title">
      <span class="gt">&gt; </span>{{typeValue}}<span class="caret">&nbsp;</span>
    </div>
    <div class="description">
      {{ introduction }}
      <div>
        Check out some of my projects <a href="#projects">here.</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      typeValue: '',
      typeString: 'Daniel Duong',
      typeSpeed: 100,
      typeDelay: 500,
      typeStringIndex: 0,
      introduction: require('@/website.json').introduction
    }
  },
  methods: {
    typeText () {
      if (this.typeStringIndex < this.typeString.length) {
        this.typeStringIndex++
        this.typeValue = this.typeString.slice(0, this.typeStringIndex)
        setTimeout(this.typeText, this.typeSpeed)
      }
    }
  },
  created () {
    setTimeout(this.typeText, this.typeDelay)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/styles/_websiteStyle';
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.title {
  font-size: 2.8em;
  color: $blue;
}
.introduction .description {
  font-size: 1.3em;
  margin: 2.5em 0;
  line-height: 1.5em;
  a {
      color: $terminallinkfontcolor;
  }
}

.caret {
  border-left: .15em solid $blue;
  animation: blink-caret 1s step-end infinite;
}

@keyframes blink-caret {
  from, to { border-color: transparent }
  50% { border-color: $blue; }
}

.title {
    margin-top: 1em;
}

</style>
