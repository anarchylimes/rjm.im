<script>
  import ky from 'ky';
  let weather
  const getWeather = async () => {
    const getweatherInfo = await ky.get('https://wttr.in/23230?format=j1').json();
    weather = getweatherInfo
  };

  $: getWeather()

</script>

<footer>
  {#if weather}
     <p>{weather.current_condition[0]["weatherDesc"][0].value} // {weather.current_condition[0]["FeelsLikeF"]}°F</p>
  {/if}
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
</style>
