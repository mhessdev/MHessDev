<template>
  <div>
    <nav class="container row end botShadow">
       	<router-link
       	v-for="routes in links" 
      	v-bind:key="routes.id"
      	:to="`${routes.page}`">{{routes.text}}</router-link>
    </nav>
  </div>
</template>

<script>
export default {
	name: 'Nav', //this is the name of the component
  	data() { 
	  return { 
	    links: [ //The links array holds objects that specify the ID, what text to display, and the path to go to
	    	{id: 0, text: '< m\\h >', page: '/'},
	    	{id: 1, text: 'Projects', page: '/projects'},
	    	{id: 2, text: 'Blog', page: '/blog'},
	    	{id: 3, text: 'Contact', page: '/#contact'}
	    ] 
	  } 
	}
}
</script>
<style lang="scss">
	@import '../assets/style/variables.scss';
	nav{padding:25px; background:$darkBlue;}
	nav a{margin-left:calc(100% - 95%); color:white;}
	nav a:first-of-type{margin-left:0px;margin-right:auto; color:$green;}

</style>