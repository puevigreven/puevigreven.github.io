<template>
  <section class="section" id="education" ref="education">
    <div class="container">
      <h1 class="title">Education</h1>
      <hr />
      <div class="columns is-multiline has-same-height">
        <div class="column is-full" v-for="(el, i) in educationJSON" :key="i">
          <div class="card">
            <div class="card-content">
              <div class="content">
                <p class="title is-4">{{ el.instituteName }}</p>
                <p class="subtitle is-6" v-if="el.courseName">
                  {{ el.courseName }} -
                  <span class="has-text-grey"
                    ><time>{{ el.fromYear }}</time> -
                    <time>{{ el.toYear }}</time></span
                  >
                </p>
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
