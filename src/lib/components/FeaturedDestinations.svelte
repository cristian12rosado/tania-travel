<script lang="ts">
  import DestinationCard from './DestinationCard.svelte';
  import { destinations } from '$lib/data/destinations';
</script>

<section class="section">
  <div class="container">
    <div class="heading">
      <p class="eyebrow">Featured destinations</p>
      <h2>Places worth dreaming about</h2>
    </div>

    <div class="grid">
      {#each destinations as destination}
        <DestinationCard {...destination} />
      {/each}
    </div>
  </div>
</section>

<style>
  .section {
    padding: 5rem 1.5rem;
  }

  .container {
    max-width: 1200px;
    margin: 0 auto;
  }

  .heading {
    margin-bottom: 2rem;
  }

  .eyebrow {
    color: #d4a373;
    text-transform: uppercase;
    letter-spacing: 0.14em;
    font-size: 0.8rem;
  }

  h2 {
    margin: 0.35rem 0 0;
    font-size: clamp(2rem, 4vw, 3rem);
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1.25rem;
  }

  @media (max-width: 1000px) {
    .grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media (max-width: 640px) {
    .grid {
      grid-template-columns: 1fr;
    }
  }
</style>