<template>
	<div>
		<li v-for="item in list" :key="item.id"><nuxt-link :to="'/detail/'+item.id">{{item.name}}</nuxt-link></li>
	</div>
</template>
<script>
	export default{
		data:()=>{
			return {
				list:[
					{id:'001',name:'jerry'}
				]
			}
		}
	}
	
</script>
<style type="text/css">
	
</style>