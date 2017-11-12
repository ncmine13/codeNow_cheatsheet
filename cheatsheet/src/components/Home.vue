<template>
    <div>
      <h1>{{header}}</h1>
      <div>
        <ul>
          <li :key="page.id" v-for="page in pages">{{ page }}</li>
        </ul>
      </div>  
    </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      header: "CodeNow Study Guide",
      pages: [
        "HTML Elements",
        "Anatomy of an Element",
        "Git Commands",
        "CLI",
        "Terminology",
        "Main CSS Rules",
        "CSS Selectors",
        "Positioning and Display",
        "Key Strokes and Shortcuts",
        "Did you..?"
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
  ul {
    list-style-type: none;
    -moz-column-count: 2;
    -moz-column-gap: 20px;
    -webkit-column-count: 2;
    -webkit-column-gap: 20px;
    column-count: 2;
    column-gap: 20px;
  }
</style>