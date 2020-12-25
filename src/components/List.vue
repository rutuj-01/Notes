
<template>
	<div class="container">
	<b-alert show >Primary Alert</b-alert>
	<b-button variant="primary" style="margin-left: 450px;">
    Profile
    <b-badge variant="light" >9 <span class="sr-only">unread messages</span></b-badge>
	</b-button>
	<b-form >
      <b-form-group
        id="input-group-1"
        label="item"
      >
        <b-form-input
          id="input-1"
          type="text"
          placeholder="Enter item to add"
   
        ></b-form-input>
      </b-form-group>
     </b-form>
	<b-button variant="success" style="margin-left: 450px;">+Add</b-button>
	<br>
	List items
	<b-list-group>
	<b-list-group-item>Cras justo odio</b-list-group-item>
	</b-list-group>


	</div>

</template>
<script >
		
</script>