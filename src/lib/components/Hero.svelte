<script lang="ts">
  import SearchBar from './SearchBar.svelte';
</script>

<section class="hero">
  <div class="overlay"></div>

  <div class="container content">
    <div class="text-block">
      <p class="eyebrow">Curated luxury & adventure</p>
      <h1>Discover Your Next Extraordinary Escape</h1>
      <p class="subtext">
        Custom vacations, curated experiences, and unforgettable destinations designed
        around you.
      </p>

      <div class="actions">
        <a href="/" class="primary">Plan My Trip</a>
        <a href="/" class="secondary">Explore Destinations</a>
      </div>
    </div>

    <SearchBar />
  </div>
</section>

<style>
  .hero {
    position: relative;
    min-height: 92vh;
    display: flex;
    align-items: center;
    overflow: hidden;
    background:
      linear-gradient(rgba(8, 17, 31, 0.35), rgba(8, 17, 31, 0.72)),
      url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=1600&q=80')
        center/cover no-repeat;
  }

  .overlay {
    position: absolute;
    inset: 0;
    background:
      radial-gradient(circle at 20% 30%, rgba(212, 163, 115, 0.18), transparent 30%),
      linear-gradient(180deg, rgba(13, 27, 42, 0.15), rgba(13, 27, 42, 0.7));
  }

  .container {
    position: relative;
    z-index: 1;
    max-width: 1200px;
    margin: 0 auto;
    width: 100%;
    padding: 2rem 1.5rem;
  }

  .content {
    display: grid;
    gap: 2rem;
    align-items: end;
  }

  .text-block {
    max-width: 760px;
  }

  .eyebrow {
    color: #d4a373;
    text-transform: uppercase;
    letter-spacing: 0.18em;
    font-size: 0.82rem;
    margin-bottom: 1rem;
  }

  h1 {
    font-size: clamp(2.8rem, 6vw, 5.5rem);
    line-height: 0.98;
    margin: 0 0 1rem;
    max-width: 900px;
  }

  .subtext {
    max-width: 640px;
    font-size: 1.1rem;
    line-height: 1.7;
    color: rgba(255, 255, 255, 0.88);
    margin-bottom: 1.5rem;
  }

  .actions {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
    margin-bottom: 2rem;
  }

  .primary,
  .secondary {
    text-decoration: none;
    padding: 0.95rem 1.25rem;
    border-radius: 999px;
    font-weight: 700;
    transition: 0.25s ease;
  }

  .primary {
    background: #d4a373;
    color: #08111f;
  }

  .secondary {
    background: rgba(255, 255, 255, 0.08);
    color: white;
    border: 1px solid rgba(255, 255, 255, 0.18);
    backdrop-filter: blur(10px);
  }

  .primary:hover,
  .secondary:hover {
    transform: translateY(-2px);
  }
</style>