<script>
  import WeatherContainer from "./components/WeatherContainer.svelte";
  import Details from "./components/Details.svelte";
  import Heading from "./components/Heading.svelte";

  let width = screen.width;

  let weather = getWeather();

  async function getWeather() {
    const res = await fetch(
      "https://api.openweathermap.org/data/2.5/weather?q=London,uk&units=metric&appid=8583d3d75196696c2dff7e5ca9cb95b8"
    );
    const weather = await res.json();
    return weather;
  }
</script>

<style>
  .container {
    height: 100vh;
    display: flex;
    flex-direction: column;
  }

  .loading {
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  @media only screen and (min-width: 800px) {
    .container {
      flex-direction: row;
      align-items: center;
      justify-content: space-between;
      width: 70%;
      margin: auto;
    }
  }
</style>

<div class="container">
  {#await weather}
    <!-- promise is pending -->
    <div class="loading">
      <h2>Loading...</h2>
    </div>

  {:then data}
    <!-- promise was fulfilled -->
    {#if width < 800}
      <!-- content here -->

      <Heading />
    {/if}

    <WeatherContainer
      temp={data.main.temp}
      location={data.name}
      country={data.sys.country} />
    <Details
      humidity={data.main.humidity}
      wind={data.wind.speed}
      visibility={data.visibility} />
  {/await}
</div>
