<template>
  <!-- <section class="section is-light" id="blogs">
    <div class="container">
      <h1 class="title">Blogs</h1>
      <hr />
      <div class="columns features has-same-height">
        <div class="column is-4">
          <div class="card is-shady">
            <div class="card-image">
              <figure class="image is-4by3">
                <img
                  src="https://source.unsplash.com/RWnpyGtY1aU"
                  alt="Placeholder image"
                />
              </figure>
            </div>
            <div class="card-content">
              <div class="content">
                <h4>Blog title</h4>
                <p>
                  Purus semper eget duis at tellus at urna condimentum mattis.
                  Non blandit massa enim nec. Integer enim neque volutpat ac
                  tincidunt vitae semper quis. Accumsan tortor posuere ac ut
                  consequat semper viverra nam.
                </p>
                <a class="button is-danger is-outlined is-normal is-rounded">Read More</a>
              </div>
            </div>
          </div>
        </div>
        <div class="column is-4">
          <div class="card is-shady">
            <div class="card-image">
              <figure class="image is-4by3">
                <img
                  src="https://source.unsplash.com/RWnpyGtY1aU"
                  alt="Placeholder image"
                />
              </figure>
            </div>
            <div class="card-content">
              <div class="content">
                <h4>Blog title</h4>
                <p>
                  Purus semper eget duis at tellus at urna condimentum mattis.
                  
                </p>
                <a class="button is-danger is-outlined is-normal is-rounded">Read More</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section> -->
    <section class="section" id="blogs" ref="blogs">
    <div class="container">
      <h1 class="title">Blogs</h1>
      <hr />
      <div class="columns is-multiline has-same-height">
        <div class="column is-4" v-for="(el, i) in blogsJSON" :key="i">
          <div class="card">
            <div class="card-image">
              <figure class="image is-16by9">
                <img :src="el.blogThumbnail" alt="Placeholder image" />
              </figure>
            </div>
            <div class="card-content has-text-centered">
              <div class="media">
                <div class="media-content has-text-centered">
                  <p class="title is-5">{{ el.blogTitle }}</p>
                  <div class="card-description">
                  <p>{{ el.blogDescription }}</p>
                  </div>
                </div>
              </div>
              <hr />
              <div class="content">
                <div class="buttons is-centered" v-if="el.blogButton">
                  <a
                    :href="el.blogButton.url"
                    class="button is-fullwidth is-outlined"
                    target="_blank"
                    :class="{
                      'is-black': el.blogButton.type=='medium',
                      }"
                  >
                  <i :class="{
                    'fab fa-medium': el.blogButton.type=='medium',
                    }" style="margin-right:10px"></i>
                    <span>{{el.blogButton.text}}</span>
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
  name: "Blogs",
  props: ["blogsJSON"],
};
</script>

<style scoped>
img {
  padding: 25px;
}
.card-content {
  padding-top: 0px;
  min-height: 280px;
}
.card-description{
  min-height: 200px;
  max-height: 200px;
}
</style>
