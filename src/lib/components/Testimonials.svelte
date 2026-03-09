<script lang="ts">
  import { testimonials } from '$lib/data/testimonials';
</script>

<section class="section">
  <div class="container">
    <div class="heading">
      <p class="eyebrow">Testimonials</p>
      <h2>What travelers say about us</h2>
    </div>

    <div class="grid">
      {#each testimonials as item}
        <div class="card">
          <div class="avatar">{item.name.charAt(0)}</div>
          <p class="quote">“{item.quote}”</p>
          <p class="name">{item.name}</p>
        </div>
      {/each}
    </div>
  </div>
</section>

<style>
  .section {
    padding: 0 1.5rem 5rem;
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
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
  }

  .card {
    padding: 1.5rem;
    border-radius: 24px;
    background: linear-gradient(180deg, rgba(255,255,255,0.07), rgba(255,255,255,0.04));
    border: 1px solid rgba(255, 255, 255, 0.08);
  }

  .avatar {
    width: 54px;
    height: 54px;
    display: grid;
    place-items: center;
    border-radius: 50%;
    background: #d4a373;
    color: #08111f;
    font-weight: 800;
    margin-bottom: 1rem;
  }

  .quote {
    font-size: 1.05rem;
    line-height: 1.75;
    color: rgba(255, 255, 255, 0.9);
  }

  .name {
    margin-top: 1rem;
    color: #d4a373;
    font-weight: 700;
  }

  @media (max-width: 900px) {
    .grid {
      grid-template-columns: 1fr;
    }
  }
</style>