<!-- components/landing/ProcessToggle.vue -->
<template>
    <div class="process-toggle mt-16">
      <div class="grid sm:grid-cols-2 md:grid-cols-3 gap-8">
        <div v-for="(item, index) in processSteps" :key="index" class="process-step">
          <button
            @click="toggleStep(index)"
            class="w-full text-left p-4 bg-white border border-gray-200 rounded-lg shadow-sm hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
          >
            <div class="flex items-center justify-between">
              <h3 class="font-semibold text-lg">{{ item.title }}</h3>
              <Icon :name="isStepOpen(index) ? 'heroicons:chevron-up' : 'heroicons:chevron-down'" class="w-5 h-5" />
            </div>
          </button>
          <div v-if="isStepOpen(index)" class="mt-2 p-4 bg-gray-50 rounded-lg">
            <p class="text-slate-500 leading-relaxed">
              {{ item.description }}
            </p>
          </div>
        </div>
      </div>
      <div class="mt-8 flex justify-center">
        <LandingLink
          href="https://github.com/Gr33nW33n/nuxtship-template"
          target="_blank"
          rel="noopener"
        >
          Our SEO Process
        </LandingLink>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const processSteps = [
    {
      title: "Client Briefing",
      description: "First We Take The Client Brief To Understand Business Goals And Objectives From Our SEO Services.",
      icon: "heroicons:magnifying-glass"
    },
    {
      title: "Competition Analysis",
      description: "Second We Begin Doing Our SEO Competition Analysis To List Ourselves Among Other Direct And Indirect Organic Competitors.",
      icon: "heroicons:document-magnifying-glass"
    },
    {
      title: "Keyword Research And Planning",
      description: "Then We Do Our Deep Keyword Research To Find The Best Winning Keywords That Best Match And Represent Business’ Products Or Services.",
      icon: "heroicons:document-check"
    },
    {
      title: "Technical Audit",
      description: "We Conduct A Technical Audit For Our Client Website To Find And Address Technical Issues That May Obstacle Our SEO Work.",
      icon: "heroicons:document-text"
    },
    {
      title: "Content Creation And Optimization",
      description: "We Begin By Content Creation Through Creating And Writing Content That Google And People Loves And Rank Better In Organic Search Results.",
      icon: "heroicons:link"
    },
    {
      title: "Building Links And Citations",
      description: "We Build Strong And Relevant Backlinks from Reputable Sources Around The Web. To Establish Our Client As An Industry Leader And Authoritative Resource.",
      icon: "heroicons:chart-bar"
    }
  ];
  
  const openSteps = ref([]);
  
  const toggleStep = (index) => {
    const stepIndex = openSteps.value.indexOf(index);
    if (stepIndex === -1) {
      openSteps.value.push(index);
    } else {
      openSteps.value.splice(stepIndex, 1);
    }
  };
  
  const isStepOpen = (index) => openSteps.value.includes(index);
  </script>