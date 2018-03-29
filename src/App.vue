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
  <div class="container">
  <div class="row">
    <div class="col-sm">
      <h2> Add a new player </h2>
       <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
      <button type="button" class="btn btn-primary btn-lg btn-block">Add a player</button>
    </div>
    <div class="col-sm">
     <h2> Add Games </h2>
     <select>
  <option value="volvo">Game 1</option>
  <option value="saab">Game 2</option>
  <option value="opel">Game 3</option>
  <option value="audi">Game 4</option>
</select>
Vs
<select>
  <option value="volvo">Game 1</option>
  <option value="saab">Game 2</option>
  <option value="opel">Game 3</option>
  <option value="audi">Game 4</option>
</select>
 <button type="button" class="btn btn-primary btn-lg btn-block">Add Set</button>
     <button type="button" class="btn btn-primary btn-lg btn-block">Add Game</button>
    </div>
    <div class="col-sm">
      <h2> Latest Games </h2>
    </div>
  </div>
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
