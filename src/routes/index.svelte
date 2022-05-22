<script>
  import { onMount } from 'svelte'
  import Letterize from 'letterizejs'

  onMount(() => {
    const letters = new Letterize({
      targets: 'h1'
    })
    const setRandomSpan = () => {
      let random
      const spans = document.querySelectorAll('h1 > span')
      spans.forEach(span => {
        random = Math.random()
        if (random > .6) {
          span.classList.toggle('flipped')
        }
      })
    }
    setRandomSpan()
    return () => {
      clearInterval(interval)
    }
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
