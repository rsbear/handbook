<script>
  import wretch from "wretch";
  let title = "";
  let content = "";

  function onClick() {
    event.preventDefault();
    wretch()
      .url("https://api.github.com/repos/rsbear/handbook/pulls")
      .post({
        title: "Amazing new feature",
        body: "Please pull these awesome changes in!",
        head: "rsbear:writing",
        base: "master"
      })
      .res(res => console.log(res));
  }
  // why am i getting 404
</script>

<form>
  <input type="text" bind:value={title} placeholder="title" />
  <input
    type="text"
    bind:value={content}
    placeholder="start writing in markdown" />
  <button on:click={onClick}>try this</button>
</form>
