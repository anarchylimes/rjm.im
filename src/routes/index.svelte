<script>
  import { onMount } from 'svelte'

  onMount(() => {
    const setRandomSpan = () => {
      const spans = document.querySelectorAll('h1 > span')
      spans.forEach(span => {
        let random = Math.random()
        if (random > .6) {
          span.classList.toggle('flipped')
        }
      })
    }
    setRandomSpan()
  })
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
