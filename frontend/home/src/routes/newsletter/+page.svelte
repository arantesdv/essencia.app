<script lang="ts">
	import ImageBox from "$lib/ImageBox.svelte";
	import Ul from "$lib/Ul.svelte";
	let topic: string = $state("")
	let topics: Array<string> = $state([
			"Serviços, profissionais e horários da Essência",
			"Transtornos mentais",
			"Psicofármacos",
			"Terapias alternativas",
			"Atividade fisica",
			"Alimentação",
			"Sono",
			"Drogas de abuso"
	])
	function add(){
		topics.push(topic)
	}
</script>
<svelte:head>
	<title>Newsletter</title>
</svelte:head>
<article>
	<h2>Newsletter</h2>
	<div style="flex-wrap: nowrap; display: flex">
		<div style="display: grid">
			<ImageBox src="./alina-karpenko-03RUtFXdu1w-unsplash.jpg" width="400px" height="400px"></ImageBox>
		</div>
		<div style="display: grid; align-content: baseline">
			<div class="article-header">Cadastre em nossa newsletter para informações da clínica e sobre saúde mental.</div>
			<div class="article-body">
				<h4>Assuntos</h4>
				<Ul items={topics} liStyle="padding: .125rem;"></Ul>
				<input required type="text" name="topic" bind:value={topic}/>
				<button onclick={add}>cadastrar</button>
			</div>
		</div>
	
	</div>

</article>