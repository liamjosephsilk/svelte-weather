<script>
  let date = getDate();

  function getDate() {
    let date = new Date();
    const months = [
      "Jan",
      "Feb",
      "Mar",
      "Apr",
      "May",
      "Jun",
      "Jul",
      "Aug",
      "Sep",
      "Oct",
      "Nov",
      "Dec"
    ];

    const days = [
      "Sunday",
      "Monday",
      "Tuesday",
      "Wednesday",
      "Thursday",
      "Friday",
      "Saturday"
    ];
    const month = months[date.getMonth()];
    const day = date.getDate();
    const week = days[date.getDay()];
    return {
      month: month,
      day: day,
      week: week
    };
  }
</script>

<style>
  div {
    display: flex;
  }
  h5 {
    font-size: 2rem;
    margin-right: 5px;
    margin-bottom: 0;
    margin-top: 0;
  }
  .week {
    margin-bottom: 20px;
    font-weight: lighter;
    color: #dee1ec;
  }

  @media only screen and (min-width: 800px) {
    h5 {
      font-size: 2rem;
    }
    .week {
      margin-bottom: 0;
    }
  }
</style>

<div>
  <h5>{date.day}</h5>
  <h5>{date.month}</h5>
</div>
<h5 class="week">{date.week}</h5>
