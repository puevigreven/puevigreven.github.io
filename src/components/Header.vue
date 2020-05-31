<template>
  <nav class="navbar is-fixed-top is-transparent">
    <div class="navbar-brand">
      <a class="navbar-item" href="#" style="padding-right: 0px" id="topBar">
        <span>Pralay Ramteke</span>
      </a>
      <div
          class="navbar-item is-hidden-desktop is-right"
          style="height: 3.25rem;"
        >
          <a
            class="navbar-item"
            href="docs/ResumePralayRamteke.pdf"
            target="_blank"
            style="padding-left: 0px"
          >
            <span class="icon">
              <i class="fa fa-file-text" title="Resume"></i>
            </span>
            <span>CV</span>
          </a>
        </div>
      <div
        class="navbar-burger burger"
        data-target="navbarExampleTransparentExample"
        @click="showNav = !showNav"
        :class="{ 'is-active': showNav }"
      >
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>

    <div
      id="navbarExampleTransparentExample"
      class="navbar-menu"
      :class="{ 'is-active': showNav }"
    >
      <div class="navbar-end">
        <a
          class="navbar-item"
          href="#"
          v-scroll-to="'#education'"
          @click="showNav = !showNav"
        >
          <span>🎓Education</span>
        </a>
        <a
          class="navbar-item"
          href="#"
          v-scroll-to="'#experience'"
          @click="showNav = !showNav"
        >
          <span>👨‍💻Experience</span>
        </a>
        <a
          class="navbar-item"
          href="#"
          v-scroll-to="'#projects'"
          @click="showNav = !showNav"
        >
          <span>🛠Projects</span>
        </a>
        <a
          class="navbar-item"
          href="#"
          v-scroll-to="'#blogs'"
          @click="showNav = !showNav"
        >
          <span>✍️Blogs</span>
        </a>
        <a
          class="navbar-item"
          href="#"
          v-scroll-to="'#contact'"
          @click="showNav = !showNav"
        >
          <span>🤝Contact</span>
        </a>
        <a
          href="docs/ResumePralayRamteke.pdf"
          class="navbar-item is-hidden-mobile"
          target="_blank"
        >
          <span>
            <img id="resumeIcon" src="img/resume-ico.png" />
          </span>
          <span>CV</span>
        </a>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      showNav: false,
    };
  },
};
</script>

<style scoped>
#topBar{
  letter-spacing: 3px;
  font-weight: normal;
  font-size: 25px;
  padding-left: 60px;
}
.navbar-item{
    color: #000000 !important;
    font-size: 17px;
}
.navbar {
    height: 60px;
    box-shadow: 0px 1px 10px #b7b6b6;
}
#resumeIcon{
  padding-top: 5px;
}
</style>
