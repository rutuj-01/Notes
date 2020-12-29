<template>
	<div class="container"  >
		{{ Users }}
		<!-- <div class="row"  style="margin-top: 30px;">
			<div class="col-4"> -->
				
				<Users />
				<!-- <ProductCard :laptopData="laptop" /> -->
			<!-- </div> -->
		<!-- </div> -->
	</div>
</template>

<script>
	// import ProductCard from './ProductCard'
	import Users from './Users'
	export default{
		components:{
			// ProductCard,
			Users
		},
		data(){
			return{
				laptops:[{
					Iname:'Mackbook pro',
					specs:'some spec',
					img:'https://images.unsplash.com/photo-1532617392008-5399d3d8a599?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=771&q=80',
					stock:'10'
				},
				{
					Iname:'Mackbook air',
					specs:'some air spec',
					img:'https://images.unsplash.com/photo-1520155346-36773ab29479?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=889&q=80',
					stock:'4'
				}]
			}

		}
	}

</script>