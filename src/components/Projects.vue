<template>
  <div class="projects">
    <h1 id="projects" class="projects-header">
      Projects
    </h1>
    <div class="projects-container">
      <div class="project-card" v-for="(item, index) in projects" v-bind:key="index">
        <div class="card-image">
            <img :src="require(`@/assets/` + item.image)">
        </div>
        <div class="card-content">
          <h2>
          {{ item.title }}
          </h2>
          {{ item.body }}
          <Technologies :techUsed="item.techUsed"/>
          <div class="project-links">
            <a :href="item.demoLink">
              Live Demo <i class="fas fa-external-link-alt"></i>
            </a>
            <a :href="item.sourceLink" class="secondary">
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

.projects .projects-container .project-card {
  background-color: #fff;
  border-radius: 4px;
  box-shadow: 0 50px 100px rgba(50,50,93,.05), 0 15px 35px rgba(50,50,93,.1), 0 5px 15px rgba(0,0,0,.1);
  margin-bottom: 1.5em;
  position: relative;

  .card-content h2 {
    margin-top: 0;
  }
  .card-image {
    display: none;
    img {
      width: 100%;
    }
  }

  .card-content {
    line-height: 1.7em;
    padding: 2em;
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
      background: #747fe0;
      color: #fff;
      margin-right: 1em;
    }
    a:hover {
      background: #7795f8;
      transform: translateY(-1px);
      box-shadow: 0 7px 14px rgba(50,50,93,.1), 0 3px 6px rgba(0,0,0,.08);
    }
    .secondary {
      background: #fff;
      color: #747fe0;
    }
    .secondary:hover {
      background: #fff;
    }
  }
}

.projects .projects-header {
  text-align: center;
  padding-top: 2em;
  margin-bottom: 3em;
}

@media (min-width: 1000px) {
  .projects .projects-container .project-card {
    display: grid;
    grid-template-columns: minmax(auto, 23em) 1fr;
  }

  .card-image {
    display: flex !important;
    align-items: center;
    // position: absolute;
    padding-left: 2em;
    grid-column: 1 / 2;
  }

  .card-content {
    grid-column: 2 / 3;
  }
  }
</style>
