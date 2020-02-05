<template>
  <div class="introduction">
    <div class="title">
      <span class="gt">&gt; </span>{{typeValue}}<span class="caret">&nbsp;</span>
    </div>
    <div class="description">
      Hello world! I am an aspiring web developer. My passion is developing apps that
      solve unique problems.
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
      typeStringIndex: 0
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
  font-size: 3.5em;
  color: #6292d0;
}
.introduction .description {
  font-size: 1.3em;
  margin: 2.5em 0;
  line-height: 1.5em;
  a {
      color: #00e6e6;
  }
}

.caret {
  border-left: .15em solid #6292d0;
  animation: blink-caret 1s step-end infinite;
}

@keyframes blink-caret {
  from, to { border-color: transparent }
  50% { border-color: #6292d0; }
}

.title {
    margin-top: 1em;
}
.terminal {
  margin-bottom: 2.5em;
}

.terminal .terminal-header {
  height: 2em;
  background-color: #e4e3e5;
  border-radius: 10px 10px 0 0;
  display: flex;
  align-items: center;
}

.terminal .terminal-header .header-button {
  width: 0.8em;
  height: 0.8em;
  border-radius: 50%;
  margin-left: 0.8em;
}

.terminal .terminal-header .red {
  background-color: #f96256;
  border: 1px solid #f65549;
}

.terminal .terminal-header .yellow {
  background-color: #fdbc3d;
  border: 1px solid #ffb524;
}

.terminal .terminal-header .green {
  background-color: #33c948;
  border: 1px solid #2dbb41;
}

.terminal .terminal-window {
  padding: 2em;
  background-color: #5a5d7a;
  border-radius: 0 0 4px 4px;
  box-shadow: 0 50px 100px rgba(50,50,93,.15), 0 15px 35px rgba(50,50,93,.2), 0 5px 15px rgba(0,0,0,.12);
  color: white;
}

.images-container {
  display: flex;
  flex-wrap: wrap;
}

.images-container img {
  height: 150px;
  padding: 1em;
}

</style>
