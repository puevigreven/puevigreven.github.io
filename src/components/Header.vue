<template>
  <nav class="navbar is-fixed-top is-transparent">
    <div class="navbar-brand">
      <a class="navbar-item navbar-center" href="#" style="padding-right: 0px" id="topBar">
        <span>Pralay Ramteke</span>
      </a>
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
        <scrollactive active-class="active" :modifyUrl="options.modifyUrl" :offset="options.offset" :duration="options.duration" class="my-nav">
        <a
          class="navbar-item scrollactive-item"
          href="#education"
          @click="showNav = !showNav"
        >
          <span class="icon">🎓</span>
          <span>Education</span>
        </a>
        <a
          class="navbar-item scrollactive-item"
          href="#experience"
          @click="showNav = !showNav"
        >
          <span class="icon">👨‍💻</span>
          <span>Experience</span>
        </a>
        <a
          class="navbar-item scrollactive-item"
          href="#projects"
          @click="showNav = !showNav"
        >
          <span class="icon">🛠</span>
          <span>Projects</span>
        </a>
        <a
          class="navbar-item scrollactive-item"
          href="#blogs"
          @click="showNav = !showNav"
        >
          <span class="icon">✍️</span>
          <span>Blogs</span>
        </a>
        <a
          class="navbar-item scrollactive-item"
          href="#contact"
          @click="showNav = !showNav"
        >
          <span class="icon">🤝</span>
          <span>Contact</span>
        </a>
        <a
          href="docs/ResumePralayRamteke.pdf"
          class="navbar-item"
          target="_blank"
        >
          <span class="resumeIcon">
            <img id="resumeIcon" src="img/resume.png" />
          </span>
          <span>CV</span>
        </a>
        </scrollactive>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      showNav: false,
      options:{
        offset: 20,
        duration: 1500,
        modifyUrl: false,
      }
    };
  },
};
</script>

<style scoped>
.active{
  font-weight: bold;
}
.my-nav{
  display:inherit
}
#topBar {
  letter-spacing: 3px;
  font-weight: normal;
  font-size: 25px;
  padding-left: 60px;
}
.navbar-item {
  color: #000000 !important;
  font-size: 17px;
}
.navbar {
  height: 60px;
  box-shadow: 0px 1px 10px #b7b6b6;
}
.resumeIcon {
  align-items: center;
  display: inline-flex;
  justify-content: center;
  height: 1.5rem;
  width: 1.5rem;
  margin-left: -5px;
  margin-right: 5px;
}
.icon {
  padding-right: 10px;
}
.navbar-item.navbar-center {
    flex-grow: 1;
    flex-direction: column;
    justify-content: center;
}
</style>
