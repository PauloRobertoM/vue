<template>
	<div id="app">
		<h3>{{title}}</h3>
		<Character />
	</div>
</template>

<script type="text/javascript">
	import Character from './components/Character.vue'

	export default {
		name: 'app',
		data() {
			return {
				title: 'Gere o seu time'
			}
		},
		components: {
			Character
		}
	}
</script>