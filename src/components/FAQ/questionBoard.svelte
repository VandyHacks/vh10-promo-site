<script>
  import Question from "./question.svelte";

  export let side;
  export let selectedIndex;
  export let boardId;
</script>

<div class={side}>
  <Question bind:selectedIndex questionId={parseInt(boardId * 3) + 0} />
  <Question bind:selectedIndex questionId={parseInt(boardId * 3) + 1} />
  <Question bind:selectedIndex questionId={parseInt(boardId * 3) + 2} />
</div>

<style>
  .left {
    background-color: rgb(82, 56, 185);
    height: 30%;
    margin-bottom: 20px;
    border-top-right-radius: 25px;
    border-bottom-right-radius: 25px;
  }

  .right {
    background-color: rgb(82, 56, 185);
    height: 30%;
    margin-bottom: 20px;
    border-top-left-radius: 25px;
    border-bottom-left-radius: 25px;
  }
</style>
