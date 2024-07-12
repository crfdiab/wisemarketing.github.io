<template>
  <footer class="my-20">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div>
          <h4 class="text-lg font-semibold mb-4">Important Links</h4>
          <ul class="space-y-2">
            <li><a href="/services" class="text-slate-500 hover:text-slate-700">Our SEO Services</a></li>
            <li><a href="/pricing" class="text-slate-500 hover:text-slate-700">Our SEO Pricing</a></li>
            <li><a href="/contact-us" class="text-slate-500 hover:text-slate-700">Contact Us</a></li>
            <li><a href="/seo" class="text-slate-500 hover:text-slate-700">Learn SEO</a></li>
          </ul>
        </div>
        <div>
          <h4 class="text-lg font-semibold mb-4">About Us</h4>
          <p class="text-slate-500">
            Wise Marketing, SEO Agency In Egypt Founded By Mohamed Diab, SEO Expert With More Than 13 Years Of Experience In Search Engine Optimization.
          </p>
        </div>
        <div>
          <h4 class="text-lg font-semibold mb-4">Connect With Us</h4>
          <ul class="space-y-2">
            <li><a href="https://www.facebook.com/wisemarketingseoagency/" class="text-slate-500 hover:text-slate-700">Facebook</a></li>
            <li><a href="https://x.com/wmseoagency" class="text-slate-500 hover:text-slate-700">X</a></li>
            <li><a href="https://www.linkedin.com/company/wise-marketing-seo-agency/" class="text-slate-500 hover:text-slate-700">LinkedIn</a></li>
            <li><a href="https://www.youtube.com/@WiseMarketingSEOAgency" class="text-slate-500 hover:text-slate-700">YouTube</a></li>
            <li><a href="https://www.pinterest.com/wisemarketingseoagency/" class="text-slate-500 hover:text-slate-700">Pinterest</a></li>
            <li><a href="https://www.tiktok.com/@wisemarketingseoagency" class="text-slate-500 hover:text-slate-700">TikTok</a></li>
          </ul>
        </div>
      </div>
    </div>
    <p class="text-center text-sm text-slate-500 mt-8">
      Copyright © {{ new Date().getFullYear() }} Wise Marketing. All rights reserved.
    </p>
    <!--
      Can we ask you a favor 🙏
      Please keep this backlink on your website if possible.
    -->
    <p class="text-center text-xs text-slate-500 mt-1">
      Built With ❤️ Powered By <strong>Nuxt 3</strong>
    </p>
  </footer>
</template>