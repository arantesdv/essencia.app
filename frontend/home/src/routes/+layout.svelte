<script lang="ts">
	import type {Snippet} from "svelte";
	let {children}: {children: Snippet} = $props()
</script>
<svelte:head>
	<script src="https://unpkg.com/htmx.org@2.0.2"></script>
	<style>
		.article-body, .article-header {
			padding: .5rem;
		}
		.article-image {
			padding: .5rem;
			display: flex;
			justify-content: center;
			align-items: center;
			&>img{
				width: 300px;
				margin: auto;
		}
		}
	</style>
</svelte:head>
<nav>
	<ul>
		<li><a href="/">Home</a></li>
		<li><a href="/about">Sobre Nós</a></li>
		<li><a href="/contact">Contato</a></li>
		<li><a href="/newsletter">Newsletter</a></li>
	</ul>
</nav>
<main>
	{@render children()}
</main>

<style>
	main {
		display: grid;
		justify-content: center;
		align-items: center;
		/*width: 90vw;*/
		border: black solid 1px;
		padding: .5rem;
	}
	nav{
		background-color: rgba(100,100,100,.25);
		padding: .5rem;
		&>ul{
			display: flex;
			flex-wrap: wrap;
			&>li{
				list-style: none;
				margin-right: 1rem;
				&>a{
					color: black;
					text-shadow: white 1px 1px 1px;
					text-decoration: none;
					font-variant: small-caps;
					font-weight: 800;
				}
			}
		}
		
	}
</style>