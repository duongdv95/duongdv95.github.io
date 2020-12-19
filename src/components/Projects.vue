<template>
  <div class="projects">
    <h1 id="projects" class="projects-header">
      Projects
    </h1>
    <hr class="header-underline">
    <div class="projects-container">
      <div class="project-card" v-for="(item, index) in projects" v-bind:key="index">
        <img :src="require(`@/assets/` + item.image)">
        <div class="project-background"></div>
        <div class="card-content">
          <h2>
          {{ item.title }}
          </h2>
          {{ item.body }}
          <Technologies :techUsed="item.techUsed"/>
          <div class="project-links">
            <a :href="item.demoLink" target="_blank">
              Live Demo <i class="fas fa-external-link-alt"></i>
            </a>
            <a v-if="item.sourceLink" :href="item.sourceLink" class="secondary" target="_blank">
              View Source <i class="fab fa-github"></i>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Technologies from '@/components/Technologies.vue'
export default {
  data: () => {
    return {
      projects: require('@/website.json').projects
    }
  },
  components: {
    Technologies
  }
}
</script>

<style scoped lang="scss">
@import '@/styles/_websiteStyle';

.project-background {
  background-image: url('~@/assets/projectoverlay.svg');
  position: absolute;
  background-size: cover;
  height: 163%;
  width: 64%;
  right: 130px;
  top: -86px;
  display: none;
}
.projects .projects-container .project-card {
  background-color: $projectcardbackgroundcolor;
  border-radius: 4px;
  box-shadow: 0 50px 100px rgba(50,50,93,.05), 0 15px 35px rgba(50,50,93,.1), 0 5px 15px rgba(0,0,0,.1);
  margin-bottom: 3em;
  position: relative;
  overflow: hidden;

  .card-content h2 {
    margin-top: 0;
  }

  img {
    display: none;
  }

  .card-content {
    line-height: 1.8em;
    padding: 2em;
    z-index: 1;
    font-size: 1.05em;
  }
  .project-links {
    a {
      display: inline-block;
      line-height: 40px;
      padding: 0 14px;
      box-shadow: 0 4px 6px rgba(50,50,93,.11), 0 1px 3px rgba(0,0,0,.08);
      border-radius: 4px;
      letter-spacing: .025em;
      text-decoration: none;
      transition: all .15s ease;
      font-size: 1em;
      font-weight: 600;
      box-sizing: border-box;
      background: $blue;
      color: #fff;
      margin-right: 1em;
    }
    a:last-child {
      margin-top: 1em;
    }
    a:hover {
      background: $blue;
      transform: translateY(-1px);
      box-shadow: 0 7px 14px rgba(50,50,93,.1), 0 3px 6px rgba(0,0,0,.08);
    }
    .secondary {
      background: #fff;
      color: $blue;
    }
    .secondary:hover {
      background: #fff;
    }
  }
}

.projects {
  .projects-header {
    text-align: center;
    padding-top: 2em;
  }

  .header-underline {
    width: 100px;
    margin-top: 4px;
    height: 0px;
    border: 0;
    border-top: 3px solid $blue;
    margin-bottom: 6em;
  }
}

@media (min-width: 1000px) {
  .projects .projects-container .project-card {
    display: grid;
    grid-template-columns: minmax(auto, 23em) 1fr;
  }

  .project-background {
    display: block;
  }

  .project-card img {
    // display: flex !important;
    display: block !important;
    position: absolute;
    align-items: center;
    grid-column: 1 / 2;
  }

  .card-content {
    grid-column: 2 / 3;
  }
  }
</style>
