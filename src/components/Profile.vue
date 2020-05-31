<template>
  <section class="hero is-fullheight is-fullheight-with-navbar">
    <div class="hero-body">
      <div class="container">
        <div class="level">
          <div class="level-item has-text-centered">
            <figure class="image is-128x128">
              <img class="is-rounded" src="img/me-white.jpg" />
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
        <div class="container has-text-centered">Hello! I am
        <h1 class="title is-1" id="name">
          Pralay Ramteke
        </h1>
        <h2 class="subtitle is-3">
          Data Science Engineer
        </h2>
        <p class="subtitle is-5 has-text-grey">Here is something about me.</p>
      </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
#name{
  margin-bottom: 1.5rem!important;
}
</style>
