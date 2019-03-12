<template>
  <div>
    <Header/>
    <main>
      <nuxt />
    </main>
  </div>
</template>

<script>
import Header from '@/components/Header'

export default {
  components: {
    Header
  }
}
</script>


<style>
@import url('https://fonts.googleapis.com/css?family=Lato:300,400,700');

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

body {
  font-family: 'Lato', sans-serif;
}

main {
  margin-top: 4.5rem;
}
</style>
