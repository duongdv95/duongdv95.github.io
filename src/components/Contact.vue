<template>
  <div class="contact">
    <h1 id="contact" class="contact-header">
      Contact me
    </h1>
    <div class="contact-links">
      <a :href="mailto + email">
        {{ email }}
      </a>
      <a :href="github">
        github
      </a>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      email: require('@/website.json').email,
      github: require('@/website.json').github,
      mailto: 'mailto: '
    }
  }
}
</script>

<style scoped lang="scss">
@import '@/styles/_websiteStyle';

.contact {
  margin: 5em 0;
}
.contact .contact-links {
  display: flex;
  justify-content: center;
  a {
    text-decoration: none;
    color: $terminallinkfontcolor;
    font-size: 1.5em;
    margin-right: 1em;
  }
}

.contact .contact-header {
  text-align: center;
}
</style>
