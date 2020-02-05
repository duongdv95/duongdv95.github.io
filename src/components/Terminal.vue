<template>
  <div class="terminal">
    <div class="terminal-header">
      <div class="header-button red"></div>
      <div class="header-button yellow"></div>
      <div class="header-button green"></div>
    </div>
    <div class="terminal-window">
      <div class="statement">
        <div class="input">
          <span class="input-sign">&gt;</span>daniel.resume
        </div>
        <div class="return">
          "<a href="./daniel_duong.pdf" target="_blank">daniel_duong.pdf</a>"
        </div>
      </div>
      <div class="statement">
        <div class="input">
          <span class="input-sign">&gt;</span>daniel.contactInfo
        </div>
        <div class="return">
          {
            "email": "<a href="mailto: dvduong13@gmail.com">dvduong13@gmail.com</a>",
            "github": "<a href="https://github.com/duongdv95" target="_blank">https://github.com/duongdv95</a>"
          }
        </div>
      </div>
      <div class="statement">
        <div class="input">
          <span class="input-sign">&gt;</span>daniel.location
        </div>
        <div class="return">
          Garden Grove, California
        </div>
      </div>
      <div class="statement">
        <div class="input">
          <span class="input-sign">&gt;</span>daniel.hobbies
        </div>
        <div class="return">
          ["planted aquariums", "fishing", "web development", "national parks",
          "photography","weight lifting", "anime"]
        </div>
      </div>
      <div class="statement">
        <div class="input">
          <span class="input-sign">&gt;</span>daniel.education
        </div>
        <div class="return">
          "B.S. in Mechanical Engineering | University of California, Irvine"
        </div>
      </div>
      <div class="statement">
        <div class="input">
          <span class="input-sign">&gt;</span>daniel.skills
        </div>
        <div class="return">
          ["HTML", "CSS", "JavaScript", "React", "NodeJS"]
        </div>
      </div>
      <div class="statement">
        <div class="input">
          <span class="input-sign">&gt;</span><span class="caret">&nbsp;&nbsp;</span>
        </div>
      </div>
    </div>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.terminal {
  line-height: 1.5em;
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
  font-size: 1.2em;
}
.terminal .terminal-window .statement {
  margin-bottom: 1em;
}
.terminal .terminal-window .statement .input-sign {
  padding-right: 0.5em;
}
.terminal .terminal-window .statement .input {
  color: #f7f7f7;
}
.terminal .terminal-window .statement .return {
  color: #e7d184;
  a {
    color: #00e6e6;
  }
}

.caret {
  border-left: .15em solid #f7f7f7;
  animation: blink-caret 1s step-end infinite;
}
@keyframes blink-caret {
  from, to { border-color: transparent }
  50% { border-color: #f7f7f7; }
}

</style>
