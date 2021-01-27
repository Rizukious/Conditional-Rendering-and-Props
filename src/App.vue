<template>
  <div id="app">
    <div class="container">
      <div class="row header mb-5 p-3">
        <div class="col-lg-12">
          <h2>
            What I do Today?
          </h2>
        </div>
      </div>

      <div class="row content">
        <div class="col-lg-12">
          <div class="pekerjaan-rumah">
            <!-- v-for digunakan sebagai perulangan data JSON -->
            <!-- v-bind:key digunakan sebagai pengambil key didalam JSON -->
            <div class="row">
              <div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id" class="mb-4 tugas col-lg-12 text-left">
                <!-- melempar data dengan props -->
                <itemTugas v-bind:tugasSaya="tugasSaya" />
            </div>  
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import "bootstrap/dist/css/bootstrap.css";
import itemTugas from "./components/itemTugas.vue";

export default {
  name: 'App',
  data : function() {
    return {
      tugas : [
      {
        // id sebagai Properties dan sebagai key
        // 1 sebagai values/nilai
        id : 1,
        namaTugas : "Membersihkan Toilet",
        isDone : false
      },
      {
        id:2,
        namaTugas : "Menyapu Halaman",
        isDone : false
      },
      {
        id:3,
        namaTugas : "Bermain Warnet",
        isDone : false
      }
    ]
    }
  },
  components: {
    itemTugas,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.header {
  background: #1abc9c;
}
.header h2 {
  margin: 0;
}
.tugas .item {
  font-size: 20px;
}
.item-completed {
  color: #1abc9c;
}
</style>
