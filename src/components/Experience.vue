<template>
  <section class="section" id="experience" ref="experience">
    <div class="container">
      <h1 class="title">Experience</h1>
      <hr />
      <div class="columns is-multiline has-same-height">
        <div class="column is-half" v-for="(el, i) in experienceJSON" :key="i">
          <div class="card">
            <div class="card-content">
              <div class="media">
                <div class="media-left">
                  <figure class="image is-64x64">
                    <img :src="el.companyLogo" alt="Placeholder image" />
                  </figure>
                </div>
                <div class="media-content">
                  <p class="title is-6 is-marginless">{{ el.companyName }}</p>
                  <p class="subtitle is-6 is-marginless">
                    {{ el.jobProfile }} 
                  </p>
                  <p class="subtitle is-6 has-text-grey" v-if="el.fromYear || el.toYear">{{ el.fromYear }} - {{ el.toYear }}</p>
                </div>
              </div>
              <div class="content">
                <p>
                  {{ el.description }}
                </p>
                <ul>
                  <li v-for="(item, exIn) in el.extras" :key="exIn">
                    {{ item }}
                  </li>
                </ul>
                <div class="tags">
                  <span
                    v-for="(tag, tagIn) in el.tags"
                    :key="tagIn"
                    class="tag"
                    >{{ tag }}</span
                  >
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
  name: "Experience",
  props: ["experienceJSON"],
};
</script>
<style scoped>
.card {
  border-radius: 5px!important;
  min-height: 350px;
}


</style>
