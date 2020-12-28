<template>
	<div class="container"  >
		<!-- {{ laptops }} -->
		<div class="row" v-for="(laptop,index) in laptops" :key="index" style="margin-top: 30px;">
			<div class="col-4">
				<b-img :src=" laptop.img" fluid alt="Responsive image"></b-img>
				Name is :{{ laptop.Iname }}
				<br>
				Specs are : {{ laptop.specs }}
				<br>
				Stock Status: {{ laptop.stock }}
			</div>
		</div>
	</div>
</template>

<script>
	export default{
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