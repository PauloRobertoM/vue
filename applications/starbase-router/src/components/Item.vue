<template>
	<div class="col-md-4">
		<h4 class="card-title">{{item.name}}</h4>
		<div v-for="(value, key, index) in item">
			<div v-if="index < 5">
				<strong>{{key}}</strong>: {{value}}
			</div>
		</div>
	</div>
</template>

<script type="text/javascript">
	export default {
		props: ['item']
	}
</script>