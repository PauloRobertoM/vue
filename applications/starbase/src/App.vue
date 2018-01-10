<template>
	<div id="app">
		<h3>{{title}}</h3>
		<button class="btn btn-primary" @click="fetchCharacter">Busca</button>
	</div>
</template>

<script type="text/javascript">
	export default {
		name: 'app',
		data() {
			return {
				title: 'Gere o seu time'
			}
		},
		methods: {
			fetchCharacter() {
				fetch('https://swapi.co/api/people/1', {
					method: 'GET'
				})
					.then(response => response.json())
					.then(json => console.log(json))
			}
		}
	}
</script>