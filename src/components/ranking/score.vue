<template>
  <div class="scoring-table">
    <table>
      <thead>
        <tr><th colspan="3">得分</th></tr>
      </thead>
      <tbody>
        <tr v-for="content in contents" :key="content.id">
          <td>{{ content.rank }}</td>
          <td>
            <p>{{ content.player }}</p>
            <p>{{ content.departement}}</p>
          </td>
          <td>{{ content.scoring }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import { reactive } from 'vue'
export default {
  setup() {
    const contents = reactive([
      {id: 1, rank: 1,player:"徐聖哲" ,departement:"資工" ,scoring:"25.5"},
      {id: 2, rank: 2,player:"徐聖哲" ,departement:"資工" ,scoring:"25.5"},
      {id: 3, rank: 3,player:"徐聖哲" ,departement:"資工" ,scoring:"25.5"},
      {id: 4, rank: 4,player:"徐聖哲" ,departement:"資工" ,scoring:"25.5"},
      {id: 5, rank: 5,player:"徐聖哲" ,departement:"資工" ,scoring:"25.5"},
      {id: 6, rank: 6,player:"徐聖哲" ,departement:"資工" ,scoring:"25.5"},
      {id: 7, rank: 7,player:"徐聖哲" ,departement:"資工" ,scoring:"25.5"},
      {id: 8, rank: 8,player:"徐聖哲" ,departement:"資工" ,scoring:"25.5"},
      {id: 9, rank: 9,player:"徐聖哲" ,departement:"資工" ,scoring:"25.5"},
      {id: 10, rank: 10,player:"徐聖哲" ,departement:"資工" ,scoring:"25.5"},
    ])
    return { contents }
  }
}
</script>

<style>
.scoring-table{
  position: sticky;
  top: 80%;
  /* top: 60%; */
  left: 0px;
  width: 30vw;
  height: 56vh;
  margin: 0 10%;
  border-radius: 20px;
  background-color: black;
  overflow-y: scroll; 
}

.scoring-table::-webkit-scrollbar{
  display: none;
}

.scoring-table table{
  width: 100%;
}

.scoring-table table thead {
  width: 100%;
  height: 60px;
  border-bottom: 1px solid #9F8950;
  font :bold 22px 'Bai Jamjuree';
  position:relative;
}

.scoring-table table thead th {
  padding-left: 20px;
  position: sticky;
  background-color: black;
  top: 0px;
}

.scoring-table table tbody {
  width: 100%;
  height: 480px;
  /* overflow-y: auto; */
}
.scoring-table table tbody tr {
  width: 100%;
  height: 20%;
  text-align: center;
  border-bottom: 1px solid #9F8950;
}
.scoring-table table tbody tr:last-child {
  border: none;
}
.scoring-table table tbody td {
  font: bold 22px "Bai Jamjuree";
  width: 35%; 
}
.scoring-table table tbody td:first-child {
  width: 2%;
}
.scoring-table table tbody td:nth-child(2) {
  width: 3%;
}

.scoring-table table tbody td:nth-child(n+3) {
  width: 3%;
}

.scoring-table table tbody td p:first-child{
    color: white;
}

.scoring-table table tbody td p:nth-child(2){
    color: #9F8950;
}
</style>