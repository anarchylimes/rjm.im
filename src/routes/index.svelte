<script>
  import { onMount } from 'svelte'
</script>

<h1 class="intro">Hi! I'm Ryan</h1>

<style>
  h1 {
    letter-spacing: -0.025rem;
    font-weight: normal;
    font-size: 20px;
  }
  :global(span) {
    line-height: 25px;
  }
  :global(.flipped) {
    transform: rotate(180deg);
    display: inline-block;

  }

</style>
