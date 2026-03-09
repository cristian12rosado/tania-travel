<script lang="ts">
  export let name: string;
  export let subtitle: string;
  export let image: string;
</script>

<div class="card" style={`background-image: linear-gradient(180deg, rgba(8,17,31,0.1), rgba(8,17,31,0.8)), url('${image}')`}>
  <div class="content">
    <div>
      <h3>{name}</h3>
      <p>{subtitle}</p>
    </div>

    <a href="/">View Packages</a>
  </div>
</div>

<style>
  .card {
    min-height: 340px;
    border-radius: 24px;
    background-size: cover;
    background-position: center;
    overflow: hidden;
    position: relative;
    transition: transform 0.28s ease;
    box-shadow: 0 12px 35px rgba(0, 0, 0, 0.22);
  }

  .card:hover {
    transform: translateY(-8px);
  }

  .content {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: end;
    padding: 1.25rem;
    gap: 1rem;
  }

  h3 {
    margin: 0;
    font-size: 1.5rem;
  }

  p {
    margin: 0.4rem 0 0;
    color: rgba(255, 255, 255, 0.82);
    line-height: 1.5;
  }

  a {
    width: fit-content;
    color: white;
    text-decoration: none;
    border: 1px solid rgba(255, 255, 255, 0.25);
    background: rgba(255, 255, 255, 0.08);
    padding: 0.7rem 1rem;
    border-radius: 999px;
    backdrop-filter: blur(8px);
  }
</style>