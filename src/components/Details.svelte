<script>
  import Detail from "./Detail.svelte";

  export let humidity;
  export let wind;
  export let visibility;
</script>

<style>
  .details {
    height: 60%;
    display: flex;
    justify-content: flex-end;
    flex-direction: column;
  }

  .card {
    background: #49506c;
    margin: 10px 10px;
    border-radius: 5px;
    box-sizing: border-box;
  }

  h3 {
    margin: 0 10px;
  }

  .title {
    font-size: 0.7rem;
    font-weight: lighter;
    letter-spacing: 0.4px;
    color: #dee1ec;
  }

  @media only screen and (min-width: 800px) {
    .details {
      justify-content: center;
      height: 100%;
      width: 40%;
    }
  }
</style>

<div class="details">
  <h3 class="title">Details</h3>
  <div class="card">
    <Detail name="Humidity" detail={humidity} value="%" />
    <Detail name="Wind Speed" detail={Math.round(wind * 3.6)} value="km/h" />
    <Detail name="Visibility" detail={visibility / 1000} value="km" />
  </div>
</div>
