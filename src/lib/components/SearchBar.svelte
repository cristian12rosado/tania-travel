<script lang="ts">
  let destination = '';
  let dates = '';
  let travelers = '';
  let style = '';

  function handleSearch() {
    console.log({ destination, dates, travelers, style });
  }
</script>

<div class="search-card">
  <div class="field">
    <label>Destination</label>
    <input bind:value={destination} placeholder="Where to?" />
  </div>

  <div class="field">
    <label>Travel Dates</label>
    <input bind:value={dates} placeholder="Select dates" />
  </div>

  <div class="field">
    <label>Travelers</label>
    <input bind:value={travelers} placeholder="2 Adults" />
  </div>

  <div class="field">
    <label>Trip Style</label>
    <input bind:value={style} placeholder="Luxury, Adventure..." />
  </div>

  <button on:click={handleSearch}>Search</button>
</div>

<style>
  .search-card {
    width: 100%;
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 0.85rem;
    padding: 1rem;
    background: rgba(10, 24, 40, 0.72);
    border: 1px solid rgba(255, 255, 255, 0.12);
    border-radius: 22px;
    backdrop-filter: blur(16px);
    box-shadow: 0 18px 60px rgba(0, 0, 0, 0.25);
  }

  .field {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
  }

  label {
    font-size: 0.8rem;
    color: rgba(255, 255, 255, 0.7);
  }

  input {
    border: none;
    outline: none;
    border-radius: 14px;
    padding: 0.95rem 1rem;
    background: rgba(255, 255, 255, 0.07);
    color: white;
  }

  input::placeholder {
    color: rgba(255, 255, 255, 0.45);
  }

  button {
    border: none;
    border-radius: 14px;
    background: #d4a373;
    color: #08111f;
    font-weight: 800;
    cursor: pointer;
    padding: 0 1rem;
  }

  @media (max-width: 950px) {
    .search-card {
      grid-template-columns: 1fr 1fr;
    }
  }

  @media (max-width: 600px) {
    .search-card {
      grid-template-columns: 1fr;
    }
  }
</style>