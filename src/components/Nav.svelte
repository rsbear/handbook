<script>
  import { TerminalIcon } from "svelte-feather-icons";
  export let posts;
</script>

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
    display: flex;
    align-items: center;
  }

  span {
    margin-left: 5px;
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

<nav>
  <p>Favish</p>
  <a href="/write">
    <button>
      <TerminalIcon size="1x" />
      <span>Write</span>
    </button>
  </a>
  <ul>
    {#each posts as post}
      <li>
        <a rel="prefetch" href="/blog/{post.slug}">{post.title}</a>
      </li>
    {/each}
  </ul>
</nav>
