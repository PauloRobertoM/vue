<template>
	<div class="col-md-4" @click="switchCharacter">
		<div class="character-card">
			<div class="card-block">
				<h4 class="card-title">{{character.name}}</h4>
				<p class="card-text">Tamanho: {{character.height}} cm</p>
				<p class="card-text">Mass: {{character.mass}} Kg</p>
				<p class="card-text">Hair Color: {{character.hair_color}}</p>
				<p class="card-text">Eye Color: {{character.eye_color}}</p>
			</div>
		</div>
	</div>
</template>

<script type="text/javascript">
	export default {
		props: ['id'],
		data() {
			return {
				character: {}
			}
		},
		methods: {
			fetchCharacter(id) {
				fetch(`https://swapi.co/api/people/${id}`, {
					method: 'GET'
				})
					.then(response => response.json())
					.then(json => this.character = json)
			},
			switchCharacter() {
				let random_id = Math.floor(Math.random() * 83) + 1
				this.fetchCharacter(random_id)
			}
		},
		created() {
			this.fetchCharacter(this.id)
		}
	}
</script>