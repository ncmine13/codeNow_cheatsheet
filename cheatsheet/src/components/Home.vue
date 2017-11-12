<template>
    <div class="home-wrapper">
      <div class="header-wrapper"><h1>{{header}}</h1></div>
      <div class="list-wrapper">
        <ul>
          <div class="li-wrapper" :key="page.id" v-for="page in pages">
            <div class="arrow">➤</div>
            <div><li class="pointer">{{ page }}</li></div>
          </div>
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
  @import '../assets/stylesheets/main.css.scss';

  .home-wrapper {
    padding: 0 5%;
    .header-wrapper {
      border-bottom: 1px dashed $base-green;
    }
    .list-wrapper {
      padding: 40px 0;
    }
  }
  h1 {
    font-size: 45px;
    padding: 10px 0;
  }
  ul {
    list-style-type: none;
    font-size: 20px;
    -moz-column-count: 2;
    -moz-column-gap: 20px;
    -webkit-column-count: 2;
    -webkit-column-gap: 20px;
    column-count: 2;
    column-gap: 20px;
    .li-wrapper {
      display: flex;
      align-items: center;
      li {
        padding: 5px 0;
        font-weight: bold;
        transition: 0.2s all;
      }
      .arrow {
        padding-right: 10px;
        opacity: 0;
      }
      &:hover {
        color: $base-green;
        li {
          text-decoration: underline;
        }
        .arrow {
          opacity: 1;
        }
      }
    }
  }
</style>