<template>
  <section class="section" id="education" ref="education">
    <div class="container">
      <h1 class="title">Education</h1>
      <hr />
      <div class="columns is-multiline has-same-height">
        <div class="column is-full" v-for="(el, i) in educationJSON" :key="i">
          <div class="card">
            <div class="card-content">
              <div class="media">
                <div class="media-left">
                  <figure class="image is-64x64">
                    <img :src="el.instituteLogo" alt="Placeholder image" />
                  </figure>
                </div>
                <div class="media-content">
                  <p class="title is-6 is-marginless">{{ el.instituteName }}</p>
                  <p class="subtitle is-6 is-marginless">
                    {{ el.courseName }} 
                  </p>
                  <p class="subtitle is-6 has-text-grey" v-if="el.fromYear || el.toYear">{{ el.fromYear }} - {{ el.toYear }}</p>
                </div>
              </div>
              <div class="content">
                {{ el.description }}
                <ul>
                  <li v-for="(extra, exIdx) in el.extras" :key="exIdx">
                    {{ extra }}
                  </li>
                </ul>
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
  name: "Education",
  props: ["educationJSON"],
};
</script>
<style scoped>
.card {
  border-radius: 5px !important;
}
</style>
