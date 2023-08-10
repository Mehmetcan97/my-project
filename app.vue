<template>
  <div>
    <h1>Second App</h1>
    <ul>
       
      <li><nuxt-link to="/page1">Page 2</nuxt-link></li>
      <li><nuxt-link to="/page2">Page 4</nuxt-link></li>
    </ul>
  </div>
</template>

<script>
export default {
  head() {
    let pageTitle = 'Second App';
      if (this.$route && this.$route.path === '/page1') {
      pageTitle = 'Page 1';
    } else if (this.$route && this.$route.path === '/page2') {
      pageTitle = 'Page 2';
    }

    return {
      title: pageTitle
    };
  },

  mounted() {
    if (this.$route.path === '/page1') {
      window.location.href = 'https://www.google.com';
    }
    if (this.$route.path === '/page2') {
      window.location.href = 'https://nuxt.com/docs/getting-started/installation';
    }
  }
};
</script>
