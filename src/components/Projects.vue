<template>
  <section class="section" id="projects" ref="projects">
    <div class="container">
      <h1 class="title">Projects</h1>
      <hr />
      <div class="columns is-multiline has-same-height">
        <div class="column is-4" v-for="(el, i) in projectsJSON" :key="i">
          <div class="card">
            <div class="card-image">
              <figure class="image is-16by9">
                <img :src="el.projectThumbnail" alt="Placeholder image" />
              </figure>
            </div>
            <div class="card-content has-text-centered">
              <div class="media">
                <div class="media-content is-full has-text-centered">
                  <p class="title is-6">{{ el.projectTitle }}</p>
                  <div class="card-description">
                    <p>{{ el.projectDescription }}</p>
                  </div>
                </div>
              </div>
              <hr />
              <div class="content">
                <div class="buttons is-centered" v-if="el.projectButton">
                  <a
                    :href="el.projectButton.url"
                    class="button is-fullwidth is-outlined"
                    target="_blank"
                    :class="{
                      'is-black': el.projectButton.type == 'github',
                      'is-link': el.projectButton.type == 'website',
                      'is-success': el.projectButton.type == 'article',
                      'is-info': el.projectButton.type == 'book',
                      'is-danger': el.projectButton.type == 'video',
                    }"
                  >
                    <i
                      :class="{
                        'fab fa-github': el.projectButton.type == 'github',
                        'fas fa-laptop': el.projectButton.type == 'website',
                        'far fa-newspaper': el.projectButton.type == 'article',
                        'fa fa-book': el.projectButton.type == 'book',
                        'fas fa-video': el.projectButton.type == 'video',
                      }"
                      style="margin-right:10px"
                    ></i>
                    <span>{{ el.projectButton.text }}</span>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "Projects",
  props: ["projectsJSON"],
};
</script>
<style scoped>
img {
  box-shadow:0 0.1em 0.5em -0.125em ;
}
.card-content {
  padding-top: 0px;
  min-height: 280px;
}
.card-description{
  min-height: 120px;
}

</style>
