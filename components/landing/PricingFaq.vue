<!-- components/landing/Faq.vue -->
<template>
    <div class="faq mt-16">
      <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight mb-8">
        FAQs About Our SEO Agency Pricing
      </h2>
      <p class="text-lg mt-4 text-slate-600">
        Frequently Asked Questions About Our SEO Agency And Our SEO Services We Provide. Questions And Their Direct Answers To Commonly Asked Questions About Our SEO Services.
      </p>
      <br>
      <div class="space-y-4">
        <div v-for="(item, index) in faqItems" :key="index" class="faq-item">
          <button
            @click="toggleItem(index)"
            class="w-full text-left p-4 bg-white border border-gray-200 rounded-lg shadow-sm hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
          >
            <div class="flex items-center justify-between">
              <h3 class="font-semibold text-lg">{{ item.question }}</h3>
              <Icon :name="isItemOpen(index) ? 'heroicons:chevron-up' : 'heroicons:chevron-down'" class="w-5 h-5" />
            </div>
          </button>
          <div v-if="isItemOpen(index)" class="mt-2 p-4 bg-gray-50 rounded-lg">
            <p class="text-slate-500 leading-relaxed">
              {{ item.answer }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const faqItems = [
    {
      question: "How SEO Services Pricing Works?",
      answer: "Our SEO Services Pricing At Our SEO Agency Follows A Fixed Pricing Model. However, That’s Why We Have A 30-Minutes Call Briefing From Client To Understand Project Needs, Time To Setting Up Our SEO Strategy, Analyzing Competitors, Market Research And Many Factors. Our SEO Agency Pricing Is Fair And Affordable For Businesses And Can Fit Any Type Of Organizations, Because Search Engine Optimization is a Long-Term Game."
    },
    {
      question: "What’s Included In Our SEO Packages?",
      answer: "Our SEO Packages Whether Beginner, Intermediate Or Advanced SEO Packages All Comes With 30-Minutes Client Briefing Call, Keyword Research, Technical Audit, Monthly Reports, Google Analytics GA4 Goal Setup, Google Tag Manager Integration For Intermediate And Advanced SEO Plans Only. In Addition Our SEO Packages Includes Google Business Profile Optimization For Intermediate And Advanced SEO Plans Only, Also We Provide Within Our SEO Services, Creation Of Custom Content Types Like Glossary Term Pages, PDFs, Infographics For Advanced SEO Plan Only."
    },
    {
      question: "What Is The Payment Frequency For Our SEO Agency?",
      answer: "Our SEO Agency Payment Frequency Is On Monthly Basis And Our Minimum Contract Period Is 3 Months. Because Search Engine Optimization Campaign Results Take At Least 3 To 6 Months To Begin Seeing Significant And Consistent Results From SEO. That’s Why Most SEO Agencies In Egypt Or Worldwide Will Have At Least 3 Months Contracting Period For SEO Services We Offer For Our Clients. Plus, We Are Committed To Monthly Subscriptions for SEO Tools we Use For Our Clients, Reporting And Our General SEO Daily Tasks."
    },
    {
      question: "Is There Any Invoice For Our SEO Services?",
      answer: "Definitely, We give Away Invoices For Our Offered SEO Services To Make Sure We Track Every Payment In Or Out Our SEO Agency And For Client Trust. Our SEO Agency is Committed To Provide Solid And Digital Proofs For Our Clients To Make Sure That We Are A Real World Entity And Company."
    },
    {
      question: "Is There A Refund For My Payment For Wise Marketing SEO Services?",
      answer: "No There Is No Refund For Our SEO Services. Because We Already Paid For It (As An SEO Agency), We Pay From Our Resources (Time And Money) To Deliver Your Services. And We Don’t Guarantee Rankings, Neither, We Do Our Job As A Professional SEO Agency And Results May Be Impacted By Google Core Updates, Competition Is Ultra Fierce And Client Budget Is Not Sufficient. That’s Why SEO Industry Is A Little-Bit Complex, due to the nature of the Offered Service which is “SEO”."
    }
  ];
  
  const openItems = ref([]);
  
  const toggleItem = (index) => {
    const itemIndex = openItems.value.indexOf(index);
    if (itemIndex === -1) {
      openItems.value.push(index);
    } else {
      openItems.value.splice(itemIndex, 1);
    }
  };
  
  const isItemOpen = (index) => openItems.value.includes(index);
  </script>