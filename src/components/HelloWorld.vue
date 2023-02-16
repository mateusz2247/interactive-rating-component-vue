<template src="./index.html"></template>

<script>
import {ref} from 'vue';
export default {
	name: "HelloWorld",
	setup(){

		let isVoted = ref(false);
		let rateValue = ref(0);
		let isSelected = ref(false);
		

		function clickRate(e){	
			rateValue.value=e.target.value		
			isSelected.value=true;
		}

		function clickSubmit(){
			isVoted.value=true;
			console.log(`send ${rateValue.value} to server`);
		}

		return{
			clickRate,
			clickSubmit,
			isVoted,
			rateValue,
			isSelected	
		}
	}
};
</script>
<style>
@import url(./style.css);
@import url(./mobile.css);
</style>