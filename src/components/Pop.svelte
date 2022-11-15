<script>
</script>

<div class="pop flex-center">
	<div class="content">
		<h3 class="title">
			<slot name="title">Title</slot>
		</h3>
		<p class="body">
			<slot name="body">Body text</slot>
		</p>
	</div>
</div>

<style>
	.pop {
		background: hsla(0, 0%, 0%, 0.5);
		width: 100vw;
		height: 100vh;
	}
	.content {
		background: #f4f4f4;
		padding: 20px 30px;
		border-radius: 4px;
		max-width: 650px;
	}
	.title {
		padding: 0;
		margin: 0;
	}
	.body {
		margin: 20px 0 0;
	}
	@media only screen and (max-width: 768px) {
		.content {
			max-width: 90%;
		}
	}
</style>
