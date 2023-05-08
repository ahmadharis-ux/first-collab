<script setup>
import { getCurrentInstance, ref } from 'vue';
import VirtualTour from '../components/VirtualTour.vue';
VirtualTour;

const componentName = getCurrentInstance()?.type.__name;
const virtualTourSrc = ref('https://virtualtoureasy.com/tour/viewer/index.php?v=UKsy7lPFd8HYr415NOTq');
</script>

<template>
	<!-- <h1>Virtual tour make "{{ componentName }}"</h1> -->
	<VirtualTour :src="virtualTourSrc" />
</template>
<style scoped>
.full {
	min-height: 100%;
	width: 100%;
}

.frame-view {
	height: 100%;
	width: 100%;
	background-color: red;
}
</style>

