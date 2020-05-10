<script>
	import { TerminalIcon } from 'svelte-feather-icons'
	export let posts
</script>

<nav>
	<p>Favish</p>
	<a href="/write">
	<button>Write</button>
	</a>
	<ul>
	{#each posts as post}
		<li><a rel='prefetch' href='/blog/{post.slug}'>{post.title}</a></li>
	{/each}
	</ul>
</nav>

<style>
	nav {
		font-weight: 300;
		padding: 0 40px 0 0;
		border-right: solid 1px lavender;
	}

	p {
		font-weight: 600;
	}

	button {
		margin: 20px 0;
	}

	ul {
		margin: 0;
		padding: 0;
		list-style: none;
	}

	a {
		text-decoration: none;
		display: block;
	}
</style>
