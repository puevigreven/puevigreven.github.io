<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">

@import "./assets/styles/styles.scss";

/* width */
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #f1f1f1; 
}
 
/* Handle */
::-webkit-scrollbar-thumb {
  background: #bbb; 
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #888; 
}

</style>
