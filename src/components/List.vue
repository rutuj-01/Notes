<template>
	<div class="container">
	<!-- <b-alert show >Primary Alert</b-alert> -->
	<b-button variant="primary" style="margin-left: 450px; margin-top:30px;">
    Profile
    <b-badge variant="light" >{{ counter }}</b-badge>
	</b-button>
	<b-form >
      <b-form-group label="Item">
        <b-form-input
          id="input-1"
          type="text"
          placeholder="Enter item to add"
			v-model="name"
        ></b-form-input>
      </b-form-group>
     </b-form>
	<b-button variant="success" style="margin-left: 450px;" @click.prevent= "add()" :disabled="check" >+Add</b-button>
	<br>
	List items
	<b-list-group>
	<b-list-group-item v-for="(item,index) in items" :key="index" style="text-align: center;">
		{{ item }}
	</b-list-group-item>
	</b-list-group>
	</div>

</template>
<script >
		export default{
			data(){
				return { 
					name : '',					
					items: []
				}
			},
			methods:
			{
				add(){

					this.items.push(this.name)
					this.name=''
					// alert(this.name)
				}
			},
			computed:
			{	
				counter(){
					return this.items.length
				},
				check()
				{	
					if(this.name.length != 0){
						return false
					}
					else{
						return true
					}
					
				}
			}
		}
</script>