<template>
  <section class="hero is-fullheight is-fullheight-with-navbar">
    <div class="hero-body">
      <div class="container">
        <div class="level">
          <div class="level-item has-text-centered">
            <figure class="image is-128x128" id="profile_image">
              <img class="is-rounded" src="img/profile_pic.jpg" />
            </figure>
          </div>
        </div>
        <!-- <div class="columns has-text-centered">
          <div class="column">
            <h1 class="title is-1">
              John Doe
            </h1>
            <h2 class="subtitle">
              FullStack Dev, VueJs, NodeJs
            </h2>
          </div>
        </div> -->
        <div class="container has-text-centered" id="hello">Hello! I am
        <h1 class="title is-1" id="name">
          Pralay Ramteke
        </h1>
        <h2 class="subtitle is-5" id="title">
          Data Scientist @ WTC
        </h2>
        <p class=" is-5" id="description"> My technical interests are in Recommender Systems, Natural Language Processing and Full-Stack Data Science. I try to put my research and engineering efforts to projects with positive societal impact, including solving healthcare and environmental challenges. 
        </p>
      </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
#hello{
    font-size: 1.1rem;
}
#name{
  font-size: 2.5rem;
  margin-bottom: 1.5rem!important;

}
#title{
  margin-bottom: 1.5rem!important;
  font-size: 1.2rem;

}
#description{
    font-size: 1.15rem;


}
#profile_image{
  box-shadow: none;
}
</style>
