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
          &gt; daniel.location
        </div>
        <div class="return">
          Garden Grove, California
        </div>
      </div>
      <div class="statement">
        <div class="input">
          &gt; daniel.contactInfo
        </div>
        <div class="return">
          {
            "email": "dvduong13@gmail.com",
            "github": "github.com/duongdv95"
          }
        </div>
      </div>
      <div class="statement">
        <div class="input">
          &gt; daniel.hobbies
        </div>
        <div class="return">
          ["planted aquariums", "fishing", "web development", "national parks"]
        </div>
      </div>
      <div class="statement">
        <div class="input">
          &gt; daniel.education
        </div>
        <div class="return">
          "B.S. in Mechanical Engineering | University of California, Irvine"
        </div>
      </div>
      <div class="statement">
        <div class="input">
          &gt; daniel.skills
        </div>
        <div class="return">
          ["HTML", "CSS", "JavaScript", "React", "NodeJS"]
        </div>
      </div>
    </div>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

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
  color: #f7f7f7;
}

</style>
