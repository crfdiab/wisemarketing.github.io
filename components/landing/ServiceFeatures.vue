<!-- components/landing/ServiceCards.vue -->
<template>
    <div class="service-cards mt-16">
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="(service, index) in services" :key="index" class="service-card">
          <div class="bg-white border border-gray-200 rounded-lg shadow-sm p-6 h-full flex flex-col">
            <div class="flex items-center mb-4">
              <Icon :name="service.icon" class="w-6 h-6 text-indigo-600 mr-2" />
              <h3 class="font-semibold text-lg">{{ service.title }}</h3>
            </div>
            <p class="text-slate-500 leading-relaxed flex-grow">
              {{ service.description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  const services = [
    {
      title: "Local SEO Services",
      description: "Our SEO Agency Provides Professional Local SEO Services For Businesses, Services Providers, Local Retailers And Any Type Of Local Business. If Your Business Needs More Phone Calls From Your Google Business Profile, More Requesting Your Business Direction And Leads, Then Our Local SEO Services Is The Solution."
    },
    {
      title: "Ecommerce SEO Services",
      description: "We Provide Professional Ecommerce SEO Services For Ecommerce Stores Built With Woocommerce, Shopify, Salla And More. We Have A Deep Experience In Ecommerce SEO And Ranking For Commercial Keywords In Front Of Big Players Like Amazon, Noon And Other Retailers."
    },
    {
      title: "Multilingual SEO Services",
      description: "We Provide Professional SEO Services For Multilingual Websites Who Offer Their Content In Multiple Languages For Multiple GEOs. Our SEO Agency Has A Good Experience In Managing Global SEO Campaigns For Multilingual Websites And Ranking In High Positions In Both Languages."
    },
    {
      title: "SaaS SEO Services",
      description: "We Provide Professional SEO Services For Software As A Service-Type Businesses. Wise Marketing SEO Solutions Are not All-In-One, Rather, We Have A Custom SEO Solution For Every Type Of Business In Every Niche Or Market With Any Language. Our SEO Services For SaaS Companies Can Help them Drive More Revenue, Subscriptions and Raise Their Brand Awareness."
    },
    {
      title: "SEO Services For Digital Agencies",
      description: "Wise Marketing Also Provides Professional SEO Services For Digital Marketing Agencies Who Want To Establish Themself In A Good Positioning In Search Engines. Our SEO Services For Digital Agencies Includes Optimizing Their Landing Pages For Nearby Searches, Optimize Their Google Business Profile, Build Citations To Business From Local Directories And Matchmaking Platforms."
    }
  ];
  </script>