<script setup>

definePageMeta({
  layout: "landing",
});

const title = ref('Our SEO Agency In Egypt Pricing List');
const description = ref('Explore our SEO services pricing list in Egypt. We offer simple and predictable pricing with no surprises.');

useHead({
  title: computed(() => title.value),
  meta: [
    {
      name: 'description',
      content: computed(() => description.value)
    }
  ]
})

const pricing = [
  {
    name: "Wise Beginner SEO",
    price: "12,000 EGP",
    usdPrice: "250 $",
    popular: false,
    features: [
      "30-Minutes-Call Client Briefing",
      "100 Keywords Optimized",
      "30 SEO-Optimized Pages",
      "Foundational Backlinks Only",
      "Website Technical Audit",
      "Google Tag Manager Integration",
      "Monthly Reporting"
    ],
    button: {
      text: "Get Started",
      link: "/contact-us",
    },
  },
  {
    name: "Wise Intermediate SEO",
    price: "24,000 EGP",
    usdPrice: "500 $",
    popular: false,
    features: [
      "30-Minutes-Call Client Briefing",
      "Unlimited Keywords Optimized",
      "Unlimited SEO-Optimized Pages",
      "Foundational Links And Quality Links Built Each Month",
      "Google My Business Profile Optimization",
      "Website Technical Audit",
      "Google Analytics GA4Goal Setup",
      "Google Tag Manager Integration",
      "Monthly Reporting"
    ],
    
    button: {
      text: "Get Started",
      link: "/contact-us",
    },
  },
  {
    name: "Wise Advanced SEO",
    price: "36,000 EGP",
    usdPrice: "750 $",
    popular: false,
    features: [
      "30-Minutes-Call Client Briefing",
      "Unlimited Keywords Optimized",
      "Unlimited SEO-Optimized Pages",
      "Foundational Links And Quality Links Built Each Month",
      "Custom Content Types Per Competition Demand",
      "Google My Business Profile Optimization",
      "Website Technical Audit",
      "Google Analytics GA4Goal Setup",
      "Google Tag Manager Integration",
      "Monthly Reporting"
    ],
    
    button: {
      text: "Get Started",
      link: "/contact-us",
    },
  },
  
];
</script>

<template>
  <LandingContainer>
    <LandingSectionhead>
      <template v-slot:title>Our SEO Agency In Egypt Pricing List</template>
      <template v-slot:desc>
        Our SEO Agency In Egypt Pricing List Is Flexible And Affordable For Businesses Who Want Quality SEO Services And At The Same Time Affordable And Flexible SEO Pricing Model Like Ours. Here Are Our SEO Packages Pricing In Egypt :
      </template>
    </LandingSectionhead>

    <div class="grid md:grid-cols-3 gap-10 mx-auto max-w-screen-lg mt-12">
      <template v-for="(item, index) in pricing" :key="index">
        <div>
          <LandingPricing :plan="item">
            <template v-slot:additional-price>
              <p class="text-sm font-bold mt-2"> Or {{ item.usdPrice }} Per Month</p>
            </template>
          </LandingPricing>
          <!-- PayPal Button Container only for Beginner SEO -->
        </div>
      </template>
    </div>
    <LandingPricingFaq></LandingPricingFaq>
    <LandingCta></LandingCta>
  </LandingContainer>
</template>