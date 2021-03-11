<template lang="pug">
  .wrapper
    header
      .navbar
        .container
          .navbar-content
            router-link.header-logo(
              to="/"
            ) Filmlibrary
            .button-burger
              span.line.line-1
              span.line.line-2
              span.line.line-3
            .navbar-list__wrapper
              ul.navbar-list
                li.navbar-item(
                  v-for="link in linkMenu"
                  :key="link.title"
                )
                  router-link.navbar-link(
                    :to="`${link.url}`"
                  ) {{link.title}}

    .content-wrapper
</template>

<script>
export default {
  data () {
    return {
      linkMenu: [
        {title: 'Home', url: '/home'},
        {title: 'Login', url: '/login'},
        {title: 'Registration', url: '/registration'}
      ]
    }
  }
}
</script>

<style>
@import './assets/stylus/umini.min.css';
</style>
