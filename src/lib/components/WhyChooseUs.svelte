<script lang="ts">
  const items = [
    { title: 'Personalized Itineraries', text: 'Trips crafted around your pace, style, and priorities.' },
    { title: 'Exclusive Deals', text: 'Premium access to offers and curated packages.' },
    { title: '24/7 Travel Support', text: 'Confidence wherever you go, whenever you need help.' },
    { title: 'Trusted Experts', text: 'Experienced planners with a taste for unforgettable travel.' }
  ];
</script>

<section class="section">
  <div class="container">
    <div class="heading">
      <p class="eyebrow">Why choose us</p>
      <h2>Luxury planning with effortless execution</h2>
    </div>

    <div class="grid">
      {#each items as item}
        <div class="card">
          <div class="icon"></div>
          <h3>{item.title}</h3>
          <p>{item.text}</p>
        </div>
      {/each}
    </div>
  </div>
</section>

<style>
  .section {
    padding: 2rem 1.5rem 5rem;
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
    gap: 1rem;
  }

  .card {
    padding: 1.5rem;
    border-radius: 22px;
    background: rgba(255, 255, 255, 0.05);
    border: 1px solid rgba(255, 255, 255, 0.08);
    backdrop-filter: blur(10px);
  }

  .icon {
    width: 48px;
    height: 48px;
    border-radius: 14px;
    background: linear-gradient(135deg, #d4a373, rgba(212, 163, 115, 0.25));
    margin-bottom: 1rem;
  }

  h3 {
    margin: 0 0 0.6rem;
  }

  p {
    margin: 0;
    line-height: 1.65;
    color: rgba(255, 255, 255, 0.78);
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