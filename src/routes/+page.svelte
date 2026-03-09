<script lang="ts">
  import Header from '$lib/components/Header.svelte';
  import Hero from '$lib/components/Hero.svelte';
  import FeaturedDestinations from '$lib/components/FeaturedDestinations.svelte';
  import WhyChooseUs from '$lib/components/WhyChooseUs.svelte';
  import Experiences from '$lib/components/Experiences.svelte';
  import Testimonials from '$lib/components/Testimonials.svelte';
  import FinalCTA from '$lib/components/FinalCTA.svelte';
</script>

<svelte:head>
  <title>Travel Agency | Extraordinary Escapes</title>
  <meta
    name="description"
    content="Discover curated vacations, luxury escapes, and unforgettable destinations."
  />
</svelte:head>

<div class="page">
  <Header />
  <Hero />
  <FeaturedDestinations />
  <WhyChooseUs />
  <Experiences />
  <Testimonials />
  <FinalCTA />
</div>

<style>
  .page {
    min-height: 100vh;
    background:
      radial-gradient(circle at top, rgba(37, 89, 133, 0.25), transparent 35%),
      linear-gradient(180deg, #08111f 0%, #0d1b2a 40%, #08111f 100%);
  }
</style>