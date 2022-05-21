<script>
  import ky from 'ky';
  let weather
  const getWeather = async () => {
    const getweatherInfo = await ky.get('https://wttr.in/ric?format=j1').json();
    weather = getweatherInfo
  };

  $: getWeather()

</script>

<footer>
  <div class="wrapper">
    {#if weather}
      <p>{weather.current_condition[0]["weatherDesc"][0].value} // {weather.current_condition[0]["FeelsLikeF"]}°F</p>
    {/if}
  </div>
</footer>

<style>
  footer {
    padding: 1rem;
    background: var(--darkgrey);
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .wrapper {
    max-width: 65rem;
    width: 100%;
    margin: 0 auto;
  }
</style>
