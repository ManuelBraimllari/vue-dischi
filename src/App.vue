<template>
  <div>
    <page-header />
    <page-main />
    <page-footer />
  </div>
</template>

<script>
import PageHeader from './components/PageHeader.vue';
import PageMain from './components/PageMain.vue';
import PageFooter from './components/PageFooter.vue';



export default {
  components: { PageHeader, PageMain, PageFooter },
  comments: {
    PageHeader,
    PageMain,
    PageFooter,
  },

};
</script>

<style lang="scss">
//bootsrapp
@import "../node_modules/bootstrap/scss/bootstrap";
//font
//@import url('https://fonts.googleapis.com/css2?family=Lato&display=swap');

  body {
  font-family: 'Lato', sans-serif;
}
</style>