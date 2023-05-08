<script setup>
import { ref } from 'vue';
import VirtualTour from '../components/VirtualTour.vue';

const listVirtualTourSrc = ref([
	'https://virtualtoureasy.com/tour/viewer/index.php?v=UKsy7lPFd8HYr415NOTq',
	'https://quiet-centaur-39e815.netlify.app/'
]);
</script>

<template>
	<div>
		<h1 class="display-1">Lorem gipsum</h1>
		<h2 class="display-5 text-disabled">dulur sing amit<sup>2</sup></h2>


		<!-- <img src="https://picsum.photos/id/16/2500/1667"
				 class="w-100 my-5 rounded"> -->

		<!-- vt gede -->
		<div style="height: 600px;"
				 class="my-5">
			<VirtualTour src="https://www.marzipano.net/demos/sample-tour/" />
		</div>


		<!-- lorem -->
		<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fuga reiciendis voluptatem perspiciatis fugit earum
			dolorem commodi dolore tempore impedit. Culpa fugit provident repudiandae magnam nemo expedita delectus similique
			dolor adipisci!
			Facere fuga aliquid nulla? Ipsam numquam cumque, itaque eos minus quo quas voluptas animi voluptate ut tempora
			quasi, nihil aut? Impedit ipsa molestias aspernatur explicabo reprehenderit officiis vero quos tempora?
			Laudantium nihil reprehenderit expedita omnis, sint, deleniti illum labore provident officiis adipisci rerum dolorem
			non. Excepturi, dolore earum quibusdam voluptates est modi officiis consequuntur. Expedita tempora minus dignissimos
			corporis eaque.
			Eius ducimus perferendis modi unde fuga, obcaecati quisquam possimus est dolor dolore rerum quod quasi officiis
			impedit in inventore quidem magnam commodi reiciendis labore, nostrum saepe. Vel dolorum omnis magnam.
			Corporis, non facere accusamus hic optio illo eos modi cupiditate accusantium. Error sequi aliquam molestias, quis
			ipsa et ullam laborum! Assumenda esse ullam atque reiciendis nemo quisquam mollitia sint repudiandae!
		</p>


		<h2 class="display-5 mt-5">
			Virtual tour
		</h2>

		<div class="row">
			<div v-for="src in listVirtualTourSrc"
					 class="col mx-1">

				<!-- virtual tour -->
				<div class="rounded shadow"
						 style="height: 600px;">
					<VirtualTour :src="src" />
				</div>
			</div>

			<h2 class="display-5 mt-5">
				Marzipano virtual tour
			</h2>

			<!-- vt gede 2 -->
			<div style="height: 600px;"
					 class="">
				<VirtualTour src="https://quiet-centaur-39e815.netlify.app/" />
			</div>

		</div>

	</div>
</template>

<style scoped>
p {
	text-align: justify;
}
</style>