<template>
  <div id="app">
    <h2> Ping Pong League</h2>
  <div class="table-responsive">
  <table class="table">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">Name</th>
      <th scope="col">Won</th>
      <th scope="col">Lost</th>
      <th scope="col">Points</th>
    </tr>
  </thead>
  <tbody v-for="item in games" :key="item.name">
    <tr>
      <th scope="row"> {{ item.id}}  </th>
      <td> {{ item.name }} </td>
      <td> {{ item.won }} </td>
      <td> {{ item.lost }} </td>
      <td> {{ item.points }} </td>
    </tr>
  </tbody>
</table>
  </div>
  </div>
</template>

<script>
export default {
  name: 'App',
   data () {
    return {
      games: [
      { id: 1, name: 'Sani', won: 0, lost: 1, points: 0 },
      { id: 2, name: 'Elmar', won: 1, lost: 0, points: 2 },
    ]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color:antiquewhite;
  margin-top: 60px;
}

body{
  background-color: #2c3e50;
}
</style>
