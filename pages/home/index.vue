<template>
	<div>
		<h1>home</h1>
		<h2>{{title.name}}</h2>
		<h2>{{err}}</h2>
		<h2>{{k1}}</h2>
	</div>
</template>
<script>
import axios from 'axios';
	export default{
		asyncData ({ params }) {
    		return axios.get('/data/data.json')
    		.then((res) => {
      			return { title: res.data }
    })
  },
  data:()=>{
    return{
      err:"Jack",
      k1:""
    }
  },
  mounted(){
      axios.get('/data/data1.json')
    		.then((res) => {
      		this.k1=res.data.k1
    })
  }
	}
</script>
<style type="text/css">

</style>
