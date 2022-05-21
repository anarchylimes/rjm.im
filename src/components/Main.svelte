<script>
</script>
<style>
  main {
    max-width: 67rem;
    width: 100%;
    padding: 1rem;
    margin: 2rem auto;

  }

  .noise {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: url(/images/noise.gif);
    opacity: .05;
    pointer-events: none;
  }
</style>
<main>
  <div class="noise"></div>
  <slot></slot>
</main>