<template>
  	<div class="modals">
    	<h1>Modals</h1>
			<div>
				<label>
					Show dark modals?
					<input 
						v-model="showDarkModals" 
						type="checkbox"
					>
				</label>
			</div>
		<button @click="showModal = true">Show modal</button>
		<component 
			v-model="showModal"
			:is="showDarkModals ? ModalDark : Modal"
			title="My modal title (via prop)"
		>
			<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Officia excepturi doloribus et beatae consequatur voluptates itaque ad recusandae voluptatum quasi. Maiores modi consequatur repellat velit quidem dicta doloribus! Maiores, quia?</p>
		</component>
  	</div>
</template>

<script setup>

/*
	import
*/
import { ref } from 'vue'
import Modal from '@/components/Modal.vue'
import ModalDark from '@/components/ModalDark.vue'
/*
	modals
*/
const showDarkModals = ref(false)
const showModal = ref(false)

</script>

<style scoped>
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