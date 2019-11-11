<script>
  import Temp from "./Temp.svelte";
  import Location from "./Location.svelte";
  import Date from "./Date.svelte";

  export let temp;
  export let location;
  export let country;
</script>

<style>
  .weather-container {
    height: 50%;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
  }
</style>

<div class="weather-container">
  <Date />
  <Temp {temp} />
  <Location {location} {country} />
</div>
