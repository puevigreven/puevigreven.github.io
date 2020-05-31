<template>
  <footer class="footer" id="footer">
    <div class="container">
      <hr />
      <div class="content has-text-centered">
        <p>© {{ year }} Pralay Ramteke</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      year: "",
    };
  },
  created() {
    this.year = new Date().getFullYear();
  },
};
</script>

<style></style>
