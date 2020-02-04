<template>
  <div class="projects">
    <h1 id="projects" class="projects-header">
      Projects
    </h1>
    <div class="projects-container">
      <div class="project-card">
        <h2>
          Aquarium PAR Database
        </h2>
        <div>
          Built a web app using ReactJS and NodeJS to share aquarium PAR data on various lighting fixtures.
          Developed REST API and utilized DynamoDB and AWS S3 with Cloudfront CDN to store data and images.
          Applied CSS to style responsive pages for desktop and mobile devices.
          Generated $22.16 in revenue and averaged 116 new users per month with a 46% bounce rate
        </div>
      </div>
      <div class="project-card">
        <h2>
          Kawaii Pet Prints
        </h2>
        <div>
          Developed an image proofing app that allows a graphic designer to upload completed artwork where
          customers are able to approve the work with a selection of backgrounds
          Wrote 9 REST endpoints for logging a customer in, retrieving data, updating data, and uploading images
        </div>
      </div>
      <div class="project-card">
        <h2>
          How Many Jelly Beans?
        </h2>
        <div>
          Built a web app using ReactJS, NodeJS, and PostGreSQL to rank players participating in a fundraising
          game in a guessing game. Wrote 9 API endpoints to control the flow of data and utilitized sockets.io
          for real-time updates of new players and calculating rank when the game ends.
        </div>
      </div>
      <div class="project-card">
        <h2>
          Portfolio
        </h2>
        <div>
          Built this website using VueJS
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">

.projects .projects-container .project-card {
  background-color: #fff;
  border-radius: 4px;
  box-shadow: 0 50px 100px rgba(50,50,93,.05), 0 15px 35px rgba(50,50,93,.1), 0 5px 15px rgba(0,0,0,.1);
  margin-bottom: 1.5em;
  padding: 1.5em;
}

.projects .projects-header {
  text-align: center;
  padding-top: 2em;
  margin-bottom: 3em;
}
</style>
