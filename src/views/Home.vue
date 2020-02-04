<template>
  <div class="home">
    <Introduction/>
    <Terminal/>
    <Projects/>
    <Contact/>
  </div>
</template>

<script>
// @ is an alias to /src
import Introduction from '@/components/Introduction.vue'
import Terminal from '@/components/Terminal.vue'
import Projects from '@/components/Projects.vue'
import Contact from '@/components/Contact.vue'

export default {
  name: 'home',
  components: {
    Introduction,
    Terminal,
    Projects,
    Contact
  }
}
</script>
