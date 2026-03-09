<script lang="ts">
  const navItems = ['Home', 'Destinations', 'Packages', 'About', 'Reviews', 'Contact'];
</script>

<header class="header">
  <div class="container">
    <div class="brand">Aether Travel</div>

    <nav>
      {#each navItems as item}
        <a href="/" class:item-active={item === 'Home'}>{item}</a>
      {/each}
    </nav>

    <a href="/" class="cta">Start Planning</a>
  </div>
</header>

<style>
  .header {
    position: sticky;
    top: 0;
    z-index: 20;
    backdrop-filter: blur(14px);
    background: rgba(8, 17, 31, 0.55);
    border-bottom: 1px solid rgba(255, 255, 255, 0.08);
  }

  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 1rem 1.5rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
  }

  .brand {
    font-size: 1.25rem;
    font-weight: 700;
    letter-spacing: 0.08em;
  }

  nav {
    display: flex;
    gap: 1.5rem;
    flex-wrap: wrap;
  }

  nav a {
    color: rgba(255, 255, 255, 0.78);
    text-decoration: none;
    font-size: 0.95rem;
    transition: 0.25s ease;
  }

  nav a:hover,
  .item-active {
    color: white;
  }

  .cta {
    text-decoration: none;
    color: #08111f;
    background: #d4a373;
    padding: 0.75rem 1rem;
    border-radius: 999px;
    font-weight: 700;
    white-space: nowrap;
  }

  @media (max-width: 900px) {
    .container {
      flex-direction: column;
      align-items: flex-start;
    }

    nav {
      gap: 1rem;
    }
  }
</style>