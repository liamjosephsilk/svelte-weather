<script>
  export let name;
  export let detail;
  export let value;
</script>

<style>
  h3 {
    margin: 0;
    font-size: 2.2rem;
  }

  .detail {
    margin: 10px 20px;
    padding-bottom: 10px;
    border-bottom: solid 1px #252d48;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .detail:last-child {
    border-bottom: none;
  }

  .name {
    margin: 0;
    font-size: 0.7rem;
    font-weight: lighter;
    letter-spacing: 0.5px;
    color: #dee1ec;
  }

  .value {
    font-size: 0.7rem;
    font-weight: lighter;
    color: #dee1ec;
  }

  @media only screen and (min-width: 800px) {
    .name {
      font-size: 1rem;
    }
    h3 {
      font-size: 3rem;
    }
  }
</style>

<div class="detail">
  <h3 class="name">{name}</h3>
  <h3>
    {detail}
    <span class="value">{value}</span>
  </h3>

</div>
