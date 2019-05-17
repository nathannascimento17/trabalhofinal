 <template>
	<div class="details">
		<div class="container">
			<div class="row">
				<div class="col-md-12" v-for="(product,index) in products" :key="index"> 
					<div v-if="proId == product.productId">
							<h1>{{product.productTitle}}</h1>
							<img :src="product.image" class="img-fluid" width="400px" id="anunciodetalils"/>
							<div class="col-md-4" id="descriçãodetails">
								<div class="card">
									<div class="card-header">
										<h3>Descrição</h3>
											</div>
										<div class="card-body">	
								{{product.productDescricao}}
								</div>
							</div>
						</div>
							<button id="btn-comprar" type="button" class="btn btn-success" style="width: 300px; height: 50px">COMPRAR</button>
								<button id="valor">{{product.productValor}}</button>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
	export default{
		name:'details',
		data(){
			return{
				proId:this.$route.params.Pid,
				title:"details",
				products:[
				{
				productTitle:"ZOTAC GTX 1060",
				image       : require('../assets/images/zotac.jpg'),
				productValor:"R$:1.059,90",
				productDescricao:"PLACA DE VIDEO ZOTAC GEFORCE GTX 1060 AMP! EDITION, 6GB GDDR5, 192BIT, ZT-P10600B-10M",
				productId:1
				},
				{
				productTitle:"NVIDIA GeForce GTX 1060",
				image       : require('../assets/images/nvidia.jpg'),
				productValor:"R$:1.059,90",
				productDescricao:"EVGA GeForce GTX 1060 SC GAMING, 06G-P4-6163-KR, 6GB GDDR5, ACX 2.0 (Single Fan)",
				productId:2
				},
				{
				productTitle:"Intel Core i5-8400",
				image       : require('../assets/images/corei5.jpg'),
				productValor:"R$:1.059,90",
				productDescricao:"PROCESSADOR INTEL CORE I5 8400 2.8GHZ (4.0GHZ TURBO), 8ª GERAÇÃO, 6-CORE 6-THREAD, LGA 1151, BX80684I58400",
				productId:3
				},
				{
				productTitle:"Samsung Galaxy S9",
				image       : require('../assets/images/galaxy.jpg'),
				productValor:"R$:1.059,90",
				productDescricao:"Samsung · Galaxy · Galaxy S · Galaxy S9 · Galaxy S9 (Original) · Android · Tela de 5,8 polegadas · Impressão digital · Reconhecimento facial · Reconhecimento de íris",
				productId:4
				},
				{
				productTitle:"PlayStation 4",
				image       : require('../assets/images/play4.jpg'),
				productValor:"R$:1.059,90",
				productDescricao:"Console Sony PlayStation 4 1TB Slim Hits Bundle v4 - God Of War",
				productId:5
				},
				{
				productTitle:"HD Seagate, 2TB",
				image       : require('../assets/images/hd.jpg'),
				productValor:"R$:1.059,90",
				productDescricao:"HD Seagate BarraCuda, 2TB, 3.5´, SATA - ST2000DM006",
				productId:6
				}
				]
				 
			}
		}
		
	}
</script>
<style>
#btn-comprar{
	position: relative;
	top:-250px;
	left: 450px;

}


#valor{
	position: relative;
	font-size: 40px;
	color:forestgreen;
	top: -330px;
	left: 180px;	 
}
h1{
	 box-shadow: 0 4px 20px 0 rgb(7, 241, 38);
}

#anunciodetalils{
	 box-shadow: 0 4px 20px 0 rgb(7, 241, 38);
	 position: relative;
	 left: -250px;
	 top:35PX;
	 
}

#descricao{
	position: relative;
	top:90px;
}

#descriçãodetails{
	position: relative;
	top: -355px;
	left: 705px;

}
</style>
