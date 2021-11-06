<template>
  <div>
    <h1>{{ test.title }}</h1>
    <!-- <nuxt-content :document="page" /> -->
   <span> {{ test.glossary.title }}</span>
    <nuxt-content :document="test.glossary.GlossDiv" />
  </div>
</template>
ß

<script>
export default {
  async asyncData({ $content }) {
    // const page = await $content('hello').fetch()
    const test = await $content('test').fetch()

    console.log(test)
    return {
      test,
    }
  },
}
</script>
