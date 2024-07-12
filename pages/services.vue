<script setup>
definePageMeta({
  layout: "landing",
});
const title = ref('Our SEO Services List');
const description = ref('Explore Our Professional SEO Services List We Provide For Our Clients As A Professional SEO Services Provider In Egypt. Explore Our Services !');

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
        <LandingServicesHero></LandingServicesHero>
        <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight" id="services-list">
            Our SEO Services List
        </h2>
        <p class="text-slate-500 leading-relaxed flex-grow">
            At Our SEO Agency We Handle Different Types Of SEO Solutions For Businesses. Our Search Engine Optimization Services Ranges From Optimizing For Local Queries And Nearby Searches To Optimizing Ecommerce Stores SEO Like Woocommerce And Shopfiy.
        </p>
        <LandingServiceFeatures></LandingServiceFeatures>
        <LandingServicesFaq></LandingServicesFaq>
        <LandingCta></LandingCta>
    </LandingContainer>
</template>