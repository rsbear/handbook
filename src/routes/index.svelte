<script context="module">
  export function preload({ params, query }) {
    return this.fetch(`blog.json`)
      .then(r => r.json())
      .then(posts => {
        return { posts };
      });
  }
</script>

<script>
  import Nav from "../components/Nav.svelte";

  export let posts;
</script>

<svelte:head>
  <title>Favish handbook</title>
</svelte:head>

<div class="sidebar">
  <Nav {posts} />
</div>
<div class="content">
  <p>content</p>
</div>
