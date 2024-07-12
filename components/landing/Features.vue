<script setup>
import ProcessToggle from '~/components/landing/Toggle.vue';

const features = [
  {
    title: "We Have A Professional SEO Team",
    description:
      "Our SEO Professional Consultants Understand The Needs And Objectives Of Your Business. Our SEO Agency Is Built By The Manpower Of Our Professional SEO Experts Who Work At Wise Marketing Agency.",
    icon: "bx:bxs-briefcase",
  },
  {
    title: "We Are Always Updated",
    description:
      "At Wise Marketing We Are Always Updated With Latest SEO Industry Updates To Ensure We Only Deliver Data-Driven SEO Services For Our Clients. Our SEO Services Aligned With Recent Google Core Updates Which Makes As An SEO Agency In Top Of Many SEO Agencies In Egypt.",
    icon: "bx:bxs-window-alt",
  },
  {
    title: "We Play SEO Safe",
    description:
      "We Only Do White-Hat SEO Services For Our Client For Brand Safety And Securing Reputable SEO Profile For Our Clients. We Only Adopt Tested And Working SEO Strategies Across Of All Our SEO Campaigns We Manage.",
    icon: "bx:bxs-data",
  },
  {
    title: "We Have Transparency In Reporting",
    description:
      "Our SEO Reports Are Transparent To Build Trust Bridge Between Our SEO Agency And Our Clients. At Wise Marketing Our SEO Reports We Sent To Our Clients Explains Everything Happening Over A 30-Day Period.",
    icon: "bx:bxs-bot",
  },
  {
    title: "We Can Scale Your SEO Strategy",
    description:
      "Our SEO Agency In Egypt Wise Marketing Can Scale Your Current SEO To A Higher Levels Of Targeting And Expanding. Our SEO Consultants At Wise Marketing Can Handle Any Type Of SEO Strategies For Any Type Of Business Which Is Our Expertise.",
    icon: "bx:bxs-file-find",
  },
  {
    title: "Our SEO Agency Has Code Of Ethics",
    description:
      "At Wise Marketing, we believe in delivering results the right way. Our Team adheres to a strict Code Of Ethics, ensuring all our SEO Practices are transparent, honest, and in compliance with Search Engine Guidelines.",
    icon: "bx:bxs-user",
  },
];
</script>

<template>
  <div class="flex flex-col md:flex-row gap-8"></div>
  <div class="mt-16 md:mt-0">
    <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
      Who Are We?
    </h2>
    <p class="text-lg mt-4 text-slate-600">
      We Are Wise Marketing Top Leading SEO Agency In Egypt. Wise Marketing Team Backed-Up With 13+ Years Of Extensive SEO Experience. Our SEO Services Has Helped Many Businesses To Rank For Their Targeted Keywords And Drive More Revenue. With Our SEO Services Your Brand Will Shines In Organic Search Result Pages.
    </p>
    <div class="mt-6 flex flex-col sm:flex-row gap-3 justify-center">
        <LandingLink
          href="/about-us"
          target="_blank"
          rel="noopener"
          >More About Us</LandingLink
        >
    </div>
    <br>
    <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
      What We Do?
    </h2>
    <p class="text-lg mt-4 text-slate-600">
      Wise Marketing Provides Professional SEO Services In Egypt. Our Search Engine Optimization Services Are Adjustable As Per Each Business Type And Goal. Our SEO Company Take Care Of Various SEO Aspects Like On-Page Optimization, Off-Page Optimization, Technical SEO, Local SEO And More. Our SEO Agency Is Excellent In Surviving Google Core Updates.
    </p>
  </div>

  <div class="grid sm:grid-cols-2 md:grid-cols-3 mt-16 gap-16">
    <div v-for="item of features" class="flex gap-4 items-start">
      <div class="mt-1 bg-black rounded-full p-2 w-8 h-8 shrink-0">
        <Icon class="text-white" :name="item.icon" />
      </div>
      <div>
        <h3 class="font-semibold text-lg">{{ item.title }}</h3>
        <p class="text-slate-500 mt-2 leading-relaxed">
          {{ item.description }}
        </p>
      </div>
    </div>
    <div class="sm:col-span-2 md:col-span-3 flex justify-center">
      <div class="mt-6 flex flex-col sm:flex-row gap-3">
        <LandingLink
          href="/services"
          target="_blank"
          rel="noopener"
        >Our SEO Services</LandingLink>
      </div>
    </div>
  </div>
  
  <br>
  <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
      Our SEO Agency Process
  </h2>
  <div class="flex justify-center items-center mt-8">
  <div class="md:order-1 md:block">
    <img
      class="object-center hover:object-top"
      src="~/assets/img/our-seo-agency-process.webp"
      alt="Our SEO Agency Process"
      loading="eager"
      format="webp"
      width="628"
      height="1200"
    />
  </div>
</div>

  <p class="text-lg mt-4 text-slate-600">
    Our SEO Company Follows Organized Process And Workflow Across All Of Our SEO Campaigns. Our SEO Agency Combines Art And Science To Achieve Unattained Success For Our Clients Which Enables Us To Build A Strong SEO Portfolio Across Years. Here Is Our Organized SEO Process We Follow To In Our SEO Campaigns To Rank Websites Successfully In The First Page:
  </p>  
  <ProcessToggle />
  <br>
  <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
      Our SEO Agency In Egypt Price List
  </h2>
  <p class="text-lg mt-4 text-slate-600">
    Our Affordable SEO Services in Egypt Start at <strong>250 USD (12,000 EGP) Monthly, up to 750 USD (36,000 EGP)</strong>. We Offer Flexible SEO Pricing Models, Tailored to Your Needs After a Thorough Website Audit to Maximize Our Search Engine Optimization Efforts.
    
    We Proudly Position Our SEO Agency In Egypt Pricing As Affordable For Businesses. Because SEO Is A Great Long-Term Investment For Your Business And Brand To Have A Good Stand In Search Engines.
  </p> 
  <div class="mt-6 flex flex-col sm:flex-row gap-3 justify-center">
        <LandingLink
          href="/pricing"
          target="_blank"
          rel="noopener"
          >Our SEO Pricing List</LandingLink
        >
    </div>
    <br>
    <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
      We Would Like To Hear From You
  </h2>
  <p class="text-lg mt-4 text-slate-600">
    Wise Marketing SEO Agency’s Team Would Like To Hear From You And Discuss Your Next Project Or How To Scale Up Your Current SEO For Your Business. Fill In The Form Below And Within 24 Hours We Will Reply To You Shortly.
  </p>
    <br>
    <div class="max-w-screen-xl mx-auto px-5">
  <div class="flex flex-col md:flex-row gap-8">
    <div class="w-full md:w-1/2">
      <LandingContactform />
    </div>
    <div class="w-full md:w-1/2">
      <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d13667.782782842749!2d29.7409375!3d31.0834375!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x14f5934a7fc5b29d%3A0x87d4e0618e931856!2sWise%20Marketing%20-%20SEO%20Agency%20In%20Egypt!5e0!3m2!1sen!2seg!4v1720647854809!5m2!1sen!2seg" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </div>
  </div>
</div>
  
</template>
