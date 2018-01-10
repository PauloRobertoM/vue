<template>
	<div id="app">
		<h3>{{title}}</h3>
		<div class="col-md-12">
			<Character
				v-for="(id, index) in initial_ids"
				:id="id"
				key="index"
			/>
		</div>
	</div>
</template>

<script type="text/javascript">
	import Character from './components/Character.vue'

	export default {
		name: 'app',
		data() {
			return {
				title: 'Gere o seu time',
				initial_ids: [1, 13, 14]
			}
		},
		components: {
			Character
		}
	}
</script>