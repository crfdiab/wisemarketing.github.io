<script setup>
import { ref, computed } from 'vue'
import TeamImg1 from '@/assets/img/mohamed-diab-seo-specialist.jpg'  // Adjust the path as needed
definePageMeta({
  layout: "landing",
});
const title = ref('About Us');
const description = ref('Explore our Wise Marketing Story, And Who Is Behind Wise Marketing SEO Agency And What Are Our Aims.');

//const TeamImg1 = "https://lh3.googleusercontent.com/drive-viewer/AKGpihYYpKl1-BvN-4kHCeAtzLs_-ozcSij4VnJIaEizeHyBfdX5SZJAMyU0NJJ6D_7GqUI7tTKDTbEzSMMTCWGkaJ7f2gs3gz2iYtA=w1440-h2960";

const team = [
  {
    name: "Mohamed Diab",
    title: "SEO Expert And Founder Of Wise Marketing SEO Agency",
    avatar: {
      src: TeamImg1,
      width: 480,
      height: 560,
    },
  },
];
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
    <LandingSectionhead>
      <template v-slot:title>About Wise Marketing</template>
      <template v-slot:desc>Wise Marketing Is A Leading Search Engine Optimization Company In Egypt.</template>
    </LandingSectionhead>

    <div class="flex flex-col gap-3 mx-auto max-w-4xl mt-16">
      <h2 class="font-bold text-3xl text-gray-800">
        Who Is Behind Wise Marketing SEO Agency?
      </h2>
      <p class="text-lg leading-relaxed text-slate-500">
        Wise Marketing, SEO Agency In Egypt Founded By <u><strong><a href="https://www.linkedin.com/in/diaab/">Mohamed Diab</a></strong></u>, SEO Expert With More Than 13 Years Of Experience In Search Engine Optimization. 3 Years Of Working In Digital Marketing Agencies As A Senior SEO Specialist.
      </p>
      <ul class="text-lg leading-relaxed text-slate-500">
        <li>Osolutions Digital Agency From Feb, 2020 To Dec, 2020</li>
        <li>Digital Brandria From Mar, 2022 To July, 2024</li>
      </ul>
      <p class="text-lg leading-relaxed text-slate-500">
        In Addition To Running Multiple Successful Portfolio Of Personal Websites Which Were Driving Passive Revenue From SEO Channel At Time.
      </p>
    </div>

    <div class="grid md:grid-cols-3 gap-10 mx-auto max-w-4xl mt-12">
      <div v-for="item of team" class="group">
        <div class="w-full aspect-square">
          <img
            :src="item.avatar.src"
            :width="item.avatar.width"
            :height="item.avatar.height"
            format="jpeg"
            alt="Mohamed Diab SEO Expert"
            class="w-full h-full object-cover rounded transition group-hover:-translate-y-1 group-hover:shadow-xl"
          />
        </div>

        <div class="mt-4 text-center">
          <h2 class="text-lg text-gray-800">{{ item.name }}</h2>
          <h3 class="text-sm text-slate-500">{{ item.title }}</h3>
        </div>
        
      </div>
      
    </div>
  </LandingContainer>
  <LandingContainer>
    <div class="flex flex-col gap-3 mx-auto max-w-4xl mt-16">
      <h2 class="font-bold text-3xl text-gray-800">
          Born Of Wise Marketing
      </h2>
      <p class="text-lg leading-relaxed text-slate-500">
        Wise Marketing Was Born To Serve The Egyptian Market High-Quality Search Engine Optimization Services For Any Type Of Business. Our Area Of Expertise Through Years Helped Us To Create Success Stories For Multiple Clients In Egypt And Globally.<br><br>

Our SEO Agency Delivers Up-To-Date SEO Strategies And Services For Their Clients, And These SEO Strategies Are Tested On Our Personal Websites Before Rolling-It Out To Client’s Websites.

      </p>
      <h2 class="font-bold text-3xl text-gray-800">
        Wise Marketing Vision
      </h2>
      <p class="text-lg leading-relaxed text-slate-500">
        Rather Than Our Offered SEO Services, We Have An Extensive SEO Library To Learn About Search Engine Optimization. Wise Marketing Vision Is To Change The SEO Landscape In Egypt, Through Helping Business To Understand What Is SEO Before Buying Our SEO Services For Their Brand.<br><br>

Our SEO Library Aims To Simplify SEO In Simple Meanings And Terms Through Multiple Forms Articles, Glossary Terms, Videos, PDFS And More.

      </p>
    </div>
  </LandingContainer>
</template>