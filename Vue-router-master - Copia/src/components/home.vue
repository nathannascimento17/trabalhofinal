<template>
<div id="app">
  <div class="home">
    <h1>{{title}}</h1>
      <div class="row">
        <div class="col-md-4 col-lg7" v-for="(data,index) in products" :key="index">
          <div class="sombra">
            <img :src="data.image" class="img-fluid">
              <h3 @click="goTodetail(data.productId)" >{{data.productTitle}}</h3>
              <h8 @click="goTodetail(data.productId)" >{{data.productDescricao}}</h8>
              <h3 @click="goTodetail(data.productId)" >{{data.productPreco}}</h3>
              <button @click="goTodetail(data.productId)" type="button" class="btn btn-success">Ver Produto</button>
            </div>
            <br>
          </div>
        </div>
      </div>
  </div>
</template>
<script>
export default {
  name: 'home',
  data () {
    return {
       data: [
          '<div class="example-slide">Slide 1</div>',
          '<div class="example-slide">Slide 2</div>',
          '<div class="example-slide">Slide 3</div>',
        ],
      title: 'Seja Bem Vindo',
      products:[
      {
        productTitle:"NVIDIA GTX 1060",
        productDescricao:"Placa de Vídeo Zotac NVIDIA GeForce GTX 1060 6GB, GDDR5X - ZT-P10620A-10M",
        productPreco:"R$:1.059,90",
        image       : require('../assets/images/zotac.jpg'),
        productId:1
      },
      {
        productTitle:"NVIDIA GeForce GTX 1060",
        productDescricao:"Placa de Vídeo EVGA NVIDIA GeForce GTX 1060 Gaming 6GB, GDDR5 - 06G-P4-6161-KR",
        productPreco:"R$:999,90",
        image       : require('../assets/images/nvidia.jpg'),
        productId:2
      },
      {
        productTitle:"Intel Core i5-8400",
        productDescricao:"Processador Intel Core i5-8400 Coffee Lake, Cache 9MB, 2.8GHz, LGA 1151",
        productPreco:"R$:999,90",
        image       : require('../assets/images/corei5.jpg'),
        productId:3
      },
      {
        productTitle:"Samsung Galaxy S9",
        productDescricao:"Smartphone Samsung Galaxy S9+ 128GB, 12MP, Tela 6.2´, Preto - G9650",
        productPreco:"R$:3.314,90",
        image       : require('../assets/images/galaxy.jpg'),
        productId:4
      },
      {
        productTitle:"PlayStation 4",
        productDescricao:"Console Sony PlayStation 4 1TB Slim Hits Bundle v4 - God Of War",
        productPreco:"R$:2.149,90",
        image       : require('../assets/images/play4.jpg'),
        productId:5
      },
      {
        productTitle:"HD Seagate, 2TB",
        productDescricao:"HD Seagate BarraCuda, 2TB, 3.5´, SATA - ST2000DM006",
        productPreco:"R$:354,90 ",
        image       : require('../assets/images/hd.jpg'),
        productId:6
      }
      ]
    }
  },
  methods:{
  goTodetail(prodId) {
    let proId=prodId
    this.$router.push({name:'details',params:{Pid:proId}})
  }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.row img{
  max-height: 15em;
  width: 100%;

}

.row h3{  
  cursor:pointer;
}

.sombra{
   box-shadow: 0 4px 20px 0 rgb(7, 241, 38);
}

</style>


