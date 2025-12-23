<script>
  import Header from '$lib/components/landingpage/Header.svelte';
  import HeroSection from '$lib/components/landingpage/HeroSection.svelte';
  import BadgesSection from '$lib/components/landingpage/BadgesSection.svelte';
  import After10thSection from '$lib/components/landingpage/After10thSection.svelte';
  import After12thSection from '$lib/components/landingpage/After12thSection.svelte';
//   import WhyChooseSection from '$lib/components/WhyChooseSection.svelte';
//   import TestimonialsSection from '$lib/components/TestimonialsSection.svelte';
//   import CTASection from '$lib/components/CTASection.svelte';
   import Footer from '$lib/components/landingpage/Footer.svelte';
</script>

<svelte:head>
  <title>Shardha DigiSetu - Digital Certificate Management</title>
  <meta name="description" content="A trusted digital platform for student certificates and education services across India" />
</svelte:head>

<div class="min-h-screen bg-white">
  <Header />
  <main>
    <HeroSection />
    <BadgesSection />
    <After10thSection />
    <After12thSection />
    <!-- <WhyChooseSection /> -->
    <!-- <TestimonialsSection /> -->
    <!-- <CTASection /> --> 
  </main>
  <Footer />
</div>