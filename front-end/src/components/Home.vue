<template>
	<main class="container row spaceBetween wrap">
		<Left></Left>
		<Right></Right>
		<Contact></Contact>
	</main>
</template>

<script>
import Left from '@/components/Left'
import Right from '@/components/Right'
import Contact from '@/components/Contact'
export default {
  name: 'Home', //this is the name of the component
  components: {
  	'Left' : Left,
  	'Right': Right,
  	'Contact': Contact
  }
}
</script>
	
<style lang="scss">
	@import '../assets/style/variables.scss';
	main{width:80%; max-width:960px; margin-left:auto; margin-right:auto; margin-top: 50px; background:$lightBlue; padding:20px; 
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