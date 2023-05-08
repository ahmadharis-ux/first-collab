<script setup>
const props = defineProps(['src']);
</script>

<template>
	<iframe class="rounded"
					height="100%"
					width="100%"
					allowfullscreen=""
					frameborder="0"
					:src="src"
					allowcontrols="true"
					allowsceneselector="true"
					allowaudio="true"></iframe>
</template>