<template>
  	<div class="modals">
    	<h1>Modals</h1>
		<button @click="showModal = true">Show modal</button>
		<teleport to=".modals-container">
			<div
			v-show="showModal"
			class="modal"
			>
				<h1>This is a modal</h1>
				<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Officia excepturi doloribus et beatae consequatur voluptates itaque ad recusandae voluptatum quasi. Maiores modi consequatur repellat velit quidem dicta doloribus! Maiores, quia?</p>
				<button @click="showModal = false">Hide modal</button>
			</div>
		</teleport>
  	</div>
</template>

<script setup>

/*
	import
*/
import { ref } from 'vue'

/*
	modals
*/
const showModal = ref(false)

</script>

<style>
.modal {
	background-color: beige;
	padding: 10px;
	position: absolute;
	left: 0;
	top: 0;
	width: 100%;
	height: 100%;
	z-index: 1;
}
</style>