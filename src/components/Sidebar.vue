<script setup>
const emits = defineEmits(['selectPage']);
const props = defineProps(['pages']);

</script>

<template>
	<!-- sidebar bg -->
	<div class="sidebar  rounded w-100 p-3">

		<!-- logo -->

		<!-- list -->
		<div v-for="name in pages"
				 role="button"
				 @click="emits('selectPage', name)"
				 class="card btn btn-light text-start text-uppercase p-2 mb-2 border-0	">
			{{ name }}
		</div>

	</div>
</template>

<style scoped>
.sidebar {
	position: sticky;
	top: 20px;
}
</style>