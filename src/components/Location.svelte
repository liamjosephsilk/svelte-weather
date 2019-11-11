<script>
  export let location;
  export let country;
</script>

<style>
  h3 {
    margin: 0 2px;
    font-size: 2rem;
    font-weight: lighter;
    color: #dee1ec;
  }

  div {
    display: flex;
  }

  @media only screen and (min-width: 800px) {
    h3 {
      font-size: 3rem;
    }
  }
</style>

<div>
  <h3>{location},</h3>
  <h3>{country}</h3>
</div>
