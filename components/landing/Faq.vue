<!-- components/landing/Faq.vue -->
<template>
    <div class="faq mt-16">
      <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight mb-8">
        Frequently Asked Questions
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
      question: "What Is SEO?",
      answer: "SEO Is Abbreviation For Search Engine Optimization, Which Are A Set Of Practices And Activities Aiming To Improve Website Organic Visibility In Search Engines. SEO Target Is To Increase Website Traffic From Unpaid (Organic) Search Result Pages Through Ranking For Website’s Targeted Keywords."
    },
    {
      question: "How Much Does SEO Cost In Egypt?",
      answer: "Our SEO Agency Pricing List Starts From 250 USD (12,000 EGP) Monthly Up To 750 USD (36,000 EGP) Monthly. Our SEO Pricing Model In Egypt Varies From Project To Another, Depending On Project Size, Goals, And Long-Term Objectives From SEO Channel."
    },
    {
      question: "How Much Does SEO Results Take To Appear?",
      answer: "Our SEO Campaign Results Usually Takes From 3 To 6 Months To See Consistent Traffic And Measurable Data From SEO Channel. Our SEO Activities Are Executed On Daily, Weekly And Monthly Basis During This Timespan We See Traffic Ups And Downs For Keywords We Are Targeting For Our Clients."
    },
    {
      question: "Is It Worth Hiring an SEO Agency In Egypt?",
      answer: "Yes, Of Course It Worth Hiring An SEO Agency In Egypt Like Wise Marketing Or Any SEO Agency In Egypt Of Your Choice. Because SEO Agencies In Egypt Or In Any Market Understand Searchers Pain Point And How to Address it Properly In Form Of Custom SEO Solution For Business."
    },
    {
      question: "What Are The Factors That Affect SEO Campaign Results?",
      answer: "The Factors That Mainly Affects Our SEO Results Are Google Core Updates, Content Frequent Changes, Sitewide Authority Of The Topic, Backlinks Built From Another Websites To Our Clients And Many Factors. Those Are The Most Influential Factors That Impacts Our SEO Strategies We Implement To Our Clients Websites."
    },
    {
      question: "What Makes The Best SEO Company Over Another One?",
      answer: "What Makes A Good SEO Company Over Another Is Expertise, Accumulative Work Experience And Their Work Portfolio. Those Are The Most Important 3 Factors To Look In A Good SEO Agency, Like Wise Marketing SEO Agency In Egypt. We Have Deep Expertise About SEO, We Have Accumulative Work Experience In SEO In Different Niches And Verticals, We Have A Strong Work Portfolio For Clients In Egypt, GCC Countries And Globally."
    },
    {
      question: "Why You Should Consider Wise Marketing As Your SEO Company In Egypt?",
      answer: "Consider Hiring Wise Marketing As Your Partner SEO Agency In Egypt Has Many Benefits. On The Top Of Those Benefits, You Will have a strong positioning in Search engines for your website and brand, Our SEO Agency Will ensure that your SEO strategy is aligned with latest Google Core Updates, Our SEO Services executed by the hand of professional SEO Consultants in Egypt. In Addition To These Reasons, Our SEO Pricing Model Is Flexible and Affordable for Businesses Who Want To Invest In SEO as An Organic Traffic Channel."
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