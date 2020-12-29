<template>
	<div class="container">
		
	<b-card
    :title="laptopData.Iname" 
    :img-src="laptopData.img"
    img-alt="Image"
    img-top
    tag="article"
    style="max-width: 20rem; height: 25rem" 
    class="mb-2"
  >
    <b-card-text>
       {{ laptopData.specs }}
    </b-card-text>

    <b-button v-if="laptopData.stock > 5" variant="primary" >In Stock</b-button>
    <b-button v-else-if="laptopData.stock > 0 && laptopData.stock <=5" variant="warning" >Very few remaining</b-button>
    <b-button v-if="laptopData.stock ==0" variant="danger" >Out Of Stock</b-button>
  </b-card>

		
	</div>
</template>
<script >
	export default{
		
			name: 'ProductCard',
			props: ['laptopData']	
	}
	

</script>

