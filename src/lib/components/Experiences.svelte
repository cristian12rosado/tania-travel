<script lang="ts">
  import { experiences } from '$lib/data/experiences';
</script>

<section class="section">
  <div class="container">
    <div class="heading">
      <p class="eyebrow">Signature experiences</p>
      <h2>Travel tailored to every kind of dream</h2>
    </div>

    <div class="chips">
      {#each experiences as item}
        <div class="chip">{item}</div>
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

  .chips {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
  }

  .chip {
    padding: 1rem 1.25rem;
    border-radius: 999px;
    background: rgba(255, 255, 255, 0.06);
    border: 1px solid rgba(255, 255, 255, 0.09);
    color: white;
    font-weight: 600;
  }
</style>