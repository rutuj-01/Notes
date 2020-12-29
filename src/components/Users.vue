<template>
	<div class="container">
		<!-- {{ users }} -->
		<div class="row"  style="margin-top: 30px;">
			<div class="col-4" v-for="(user,index) in users[0]" :key="index">
		<b-card
			:title="user.first_name + ' ' + user.last_name " 
			:img-src="user.avatar"
			img-alt="Image"
			img-top
			tag="article" 
			class="mb-2"
		>
    <b-card-text>
       {{ user.email }}
    </b-card-text>
		</b-card>
	</div>
</div>


	</div>
</template>

<script>
import axios from 'axios'
export default{
	data()
	{
		return {
			users:[]
		}
	},
	created(){
		axios.get('https://reqres.in/api/users')
		.then(res => {
			console.log(res.data.data)
			this.users.push(res.data.data)
		})
		.catch(err => {
			console.log(err)
		})
	}

}

</script>