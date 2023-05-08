<script setup>
import Sidebar from './components/Sidebar.vue';
import Footer from './components/Footer.vue';
import Virt360 from './pages/Virt360.vue';
import Marzipano from './pages/Marzipano.vue';
import Attempt from './pages/Attempt.vue';
import { ref, watch } from 'vue';
import { computed } from '@vue/reactivity';


const pages = {
	v360: Virt360,
	marzipano: Marzipano,
	cobaan: Attempt,
};

const pageNames = computed(() => {
	let nameList = [];
	for (let pageName of Object.keys(pages)) {
		nameList.push(pageName);
	}

	return nameList;
});

const selectedPage = ref('v360');

function changePage(to) {
	selectedPage.value = to;
}

watch(selectedPage, (newVal) => {
	document.title = `VT | ${newVal}`;
})

</script>

<template>
	<!-- outer container -->
	<div class="d-flex justify-content-around container-fluid bg-info p-0"
			 style="min-height: 100vh;">

		<!-- sidebar -->
		<div class="sidebar-container">
			<Sidebar :pages="pageNames"
							 @select-page="changePage" />
		</div>

		<!-- main content -->
		<div class="container bg-light shadow rounded p-5"
				 style="margin: 20px 20px 20px 0px; min-height: 90vh;">
			<component :is="pages[selectedPage]" />
		</div>

	</div>

	<!-- footer -->
	<!-- <Footer /> -->
</template>

<style scoped>
.sidebar-container {
	background-color: transparent;
	min-height: 90vh;
	width: 20rem;
	padding: 20px;
	display: flex;
	justify-content: center;
	align-items: start;
}
</style>