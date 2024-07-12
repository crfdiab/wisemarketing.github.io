<!-- components/landing/Faq.vue -->
<template>
    <div class="faq mt-16">
      <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight mb-8">
        Frequently Asked Questions
      </h2>
      <p class="text-lg mt-4 text-slate-600">
        Frequently Asked Questions About Our Offered SEO Services. Like Our SEO Services Types, Time Of Delivery, Difference Between Each SEO Service type , Which SEO Services Type Is the Most Suitable For My Business And More Related Questions About Type Of Our Offered SEO Solutions.
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
            <p class="text-slate-500 leading-relaxed" v-html="item.answer">
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
      question: "What Are SEO Services And How Do They Work?",
      answer: "SEO Services Are A Powerful Group Of Search Engine Optimization Strategies That Enhance Your Online Presence. These Valuable Components Include Effective On-Page SEO, Impactful Off-Page SEO And Essential Technical SEO. SEO Services Thrive Through Partnering With An Expert SEO Agency Like Wise Marketing Or Mastering These Beneficial SEO Techniques Yourself. Both Approaches Offer Exciting Opportunities For Success."
    },
    {
      question: "What Are Types Of SEO Services?",
      answer: "There Are Many SEO Services Types, But The Famous Ones Are Ecommerce SEO Services And Local SEO Services. Other SEO Services Types Like SaaS SEO Services And Enterprise SEO Services, Those Two Types Of SEO Services Can Be Offered By Dedicated SEO Agencies In SaaS SEO, Enterprise SEO, International SEO And So On. At Wise Marketing We Specialize In Local SEO Services, Ecommerce SEO Services, Multilingual SEO Services, SaaS SEO Services And SEO Services For Digital Agencies."
    },
    {
      question: "Why Are SEO Services Important For My Businesses?",
      answer: "SEO Services Are Important For Your Business Because It Helps Your Brand Stand In A Good Position In Search Engines. SEO Services Also Impacts Your Business In A Positive Way Through Standing Your Brand As An Authority Within Your Industry. SEO Services Help Businesses To Pay Less For CPC Advertising On The Long-Run, When The Brand Becomes Authority On Its Topic."
    },
    {
      question: "Can I Do These SEO Services Myself On My Website?",
      answer: "Yes Of Course, You Can Do SEO Services On Your Own, But You will miss expertise and experience. That’s The Role Of Our SEO Agency To Handle And Manage Your SEO Services For More Return On Investment From Search Engines. Hiring an SEO Agency To Provide Your Business With SEO Services Rather Than Doing SEO Yourself Is Way Much Better And Smarter."
    },
    {
      question: "Which Type Of SEO Service Is Suitable for My Business?",
      answer: "Choosing Which SEO Services Is Suitable For Your Business Is Simple Depends On How You Define Your Business. Our SEO Services Are Tailored To Each Business Type, Thereby, If You Are An Ecommerce Store, Then Your Suitable SEO Service Will Be “Ecommerce SEO Services” Simple As That. Your Business May Need One Or More SEO Services Upon Our Audit And Research."
    },
    {
      question: "How Much Does SEO Services Cost?",
      answer: "Our SEO Services Pricing Starts At <strong>12,000 EGP Or (250 USD) Up To 36,000 EGP Or (750 USD)</strong> Per Month You Can Check <a href='http://localhost:3000/pricing'>Our Pricing Pages</a>. Other SEO Agencies May Charge Higher May Charge Lower, But We Are Charging For What We Offer. SEO Agencies In Egypt Pricing Can Range From <strong>18,000 EGP to 50,000 EGP</strong> And Sometimes More Per Month. But Most Cases Are Digital Marketing Agencies, More Than A Dedicated SEO Agencies Like Wise Marketing."
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