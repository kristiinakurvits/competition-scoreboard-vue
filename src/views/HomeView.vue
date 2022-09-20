<template>
  <div class="scoreboard">

    <h2 class="heading">1500m</h2>
    <table class="table table-hover">
      <thead class="thead-light">
      <tr>
        <th scope="col">Rank</th>
        <th scope="col">Country</th>
        <th scope="col">Athlete</th>
        <th scope="col">Time</th>
        <th scope="col">Points</th>
      </tr>
      </thead>
      <tbody>
      <tr v-for="result in results">
        <th scope="row">{{ result.rank }}</th>
        <td>{{ result.country }} <span class="flag-icon flag-icon-ad"></span></td>
        <td>{{ result.athlete }}</td>
        <td>{{ result.time }}</td>
        <td>{{ result.points }}</td>
      </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'HomeView',
  data() {
    return {
      results: [
        {rank: 1, country: "JPN", athlete: "Akihiko Nakamura", time: "4:18.370", points: 823},
        {rank: 2, country: "AUS", athlete: "Cedric Dubler", time: "4:32.120", points: 731},
        {rank: 3, country: "AUT", athlete: "Dominik Distelberger", time: "4:33.470", points: 722},
        {rank: 4, country: "EST", athlete: "Karl Robert Saluri", time: "4:39.400", points: 684},
        {rank: 5, country: "POL", athlete: "Pawel Wiesiolek", time: "4:42.270", points: 666},
        {rank: '', country: "CZE", athlete: "Jiri Sykora", time: "Did not finish", points: 0}
      ]
    }
  },
};
</script>

<style scoped>
.scoreboard thead{
  background-color: lightgray;
}
.scoreboard table{
  margin: 20px;
}
.scoreboard .heading{
  margin: 20px;
  text-align: left;
}

</style>
