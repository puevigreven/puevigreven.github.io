<template>
  <div>
    <Header></Header>
    <Profile></Profile>
    <Education :educationJSON="educationJSON"></Education>
    <Experience :experienceJSON="experienceJSON"></Experience>
    <Projects :projectsJSON="projectsJSON"></Projects>
    <Blogs :blogsJSON="blogsJSON"></Blogs>
    <Contact></Contact>
    <Footer></Footer>
    <back-to-top bottom="50px" right="50px" visibleoffset="300">
      <a  class="button is-rounded is-dark">
        <i class="fa fa-angle-up"></i>
      </a>
    </back-to-top>
  </div>
</template>

<script>
import Header from "../components/Header";
import Profile from "../components/Profile";
import Experience from "../components/Experience";
import Projects from "../components/Projects";
import Education from "../components/Education";
import Contact from "../components/Contact";
import Blogs from "../components/Blogs";
import Footer from "../components/Footer";
import BackToTop from "vue-backtotop";

// JSON data
import educationJSON from "../data/education.json";
import experienceJSON from "../data/experience.json";
import projectsJSON from "../data/projects.json";
import blogsJSON from "../data/blogs.json";

export default {
  name: "Home",
  components: {
    Header,
    Profile,
    Experience,
    Projects,
    Education,
    Contact,
    //Blogs,
    Footer,
    BackToTop,
  },
  data() {
    return {
      educationJSON,
      experienceJSON,
      projectsJSON,
     // blogsJSON,
      isVisible: false,
    };
  },
};
</script>
<style scoped>
</style>
