<script setup>
import AppHeader from './components/AppHeader.vue'
import HeroSection from './components/HeroSection.vue'
import HowItWorks from './components/HowItWorks.vue'
import FeaturesGrid from './components/FeaturesGrid.vue'
import ScreensShowcase from './components/ScreensShowcase.vue'
import ProSection from './components/ProSection.vue'
import AudienceSection from './components/AudienceSection.vue'
import PricingSection from './components/PricingSection.vue'
import TechStrip from './components/TechStrip.vue'
import DownloadSection from './components/DownloadSection.vue'
import AppFooter from './components/AppFooter.vue'
</script>

<template>
  <div class="min-h-screen bg-paper">
    <AppHeader />
    <HeroSection />
    <HowItWorks />
    <FeaturesGrid />
    <ScreensShowcase />
    <ProSection />
    <AudienceSection />
    <PricingSection />
    <TechStrip />
    <DownloadSection />
    <AppFooter />
  </div>
</template>
