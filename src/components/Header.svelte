<script>
  // your script goes here
</script>

<header>
  <div class="wrapper">
    <a href="/"><span class="circle"></span></a>
  </div>
</header>

<style lang="scss">
  header {
    padding: 0.75rem 1rem;
    background: var(--darkgrey);
    color: white;
    display: flex;
    align-items: center;
    justify-content: flex-start;
  }

  .wrapper {
    max-width: 65rem;
    width: 100%;
    margin: 0 auto;
  }

  .circle {
    width: 2.5rem;
    height: 2.5rem;
    background: var(--grey);
    border-radius: 50%;
    display: block;

    &:hover {
      background-color: var(--maroon)
    }
  }

  a {
    text-decoration: none;
  }
</style>
