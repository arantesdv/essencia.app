<script lang="ts">
	import ImageTextBox from "$lib/ImageTextBox.svelte";
	// let {src = "./alina-karpenko-03RUtFXdu1w-unsplash.jpg", text = "Aqui você encontra informações sobre a Clínica Essência e saúde mental."}:{
	// 	src: string;
	// 	text: string;
	// } = $props()
</script>
<svelte:head>
	<title>Essência</title>
</svelte:head>
<h1>Bem vindo à Essência</h1>
<!--<div class="article-image"><enhanced:img src="/static/alina-karpenko-03RUtFXdu1w-unsplash.jpg?w=300;200;100" alt="" sizes="(min-width:1920px) 300px, (min-width:1080px) 200px, (min-width:768px) 100px"></div>-->

<div>
	<ImageTextBox src="./alina-karpenko-03RUtFXdu1w-unsplash.jpg" text="Aqui você encontra informações sobre a Clínica Essência e saúde mental." width="300px"></ImageTextBox>
	<ImageTextBox src="./favicon.png" text="Aqui você encontra informações sobre a Clínica Essência e saúde mental." width="150px"></ImageTextBox>

</div>

<style>
	h1{
		text-align: center;
	}
	div{
		display:flex;
		flex-wrap: wrap;
		justify-content: center;
		align-items: start;
	}
</style>