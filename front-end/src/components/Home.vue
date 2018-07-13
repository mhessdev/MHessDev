<template>
	<main class="container col">
		<div class="circleDot">
			<i class="fas fa-terminal"></i>
		</div>
		<div id="aboutBox">
		    <h1>Marc Hess</h1>
		    <h2>Developer</h2>
		    <h3>Imagine | Create</h3>
		    <p>Here is some information. This is the home page</p>
	  </div>
	</main>	
  
</template>

<script>
export default {
  name: 'Home' //this is the name of the component
}
</script>
	
<style lang="scss">
	@import '../assets/style/variables.scss';
	main{width:80%; margin-left:auto; margin-right:auto; margin-top: 50px; background:$lightBlue; padding:20px; 
		-webkit-box-shadow: 0px 5px 5px 0px rgba(0,0,0,0.45);
		-moz-box-shadow: 0px 5px 5px 0px rgba(0,0,0,0.45);
		box-shadow: 0px 5px 5px 0px rgba(0,0,0,0.45);
		-webkit-border-radius: 5px;
		-webkit-border-bottom-right-radius: 2px;
		-webkit-border-bottom-left-radius: 2px;
		-moz-border-radius: 5px;
		-moz-border-radius-bottomright: 2px;
		-moz-border-radius-bottomleft: 2px;
		border-radius: 5px;
		border-bottom-right-radius: 2px;
		border-bottom-left-radius: 2px;
	}
</style>