<script>
  export let temp;
  let degree = "&deg; ";
</script>

<style>
  h3 {
    font-size: 10rem;
    margin: 0;
  }
  span {
    font-size: 4.2rem;
  }

  .temp {
    display: flex;
    color: #f35538;
  }

  @media only screen and (min-width: 800px) {
    h3 {
      font-size: 20rem;
    }
    span {
      font-size: 10.2rem;
    }
  }
</style>

<div class="temp">
  <h3>{Math.round(temp)}</h3>
  <span>&deg;</span>
</div>
