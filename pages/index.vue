<script setup lang="ts">
definePageMeta({
  layout: "landing",
});
const title = ref('Top Leading SEO Agency In Egypt');
const description = ref('We Are Wise Marketing A Top Leading SEO Agency In Egypt Helping Businesses With Professional SEO Services To Rank In First Pages For Search Engines.');
useHead({
  title: computed(() => title.value),
  meta: [
    {
      name: 'description',
      content: computed(() => description.value)
    }
  ]
})
</script>
<template>
  <LandingContainer>
    <LandingHero></LandingHero>
    <LandingFeatures></LandingFeatures>
    <br>
    <hr></hr>
    <LandingCta></LandingCta>
    <br>
    <hr></hr>
    <LandingFaq></LandingFaq>
  </LandingContainer>
</template>
