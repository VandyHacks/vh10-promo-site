<script>
  import Question from "./question.svelte";

  export let side;
  export let selectedIndex;
  export let boardId;
</script>

<div class={`board ${side} b-${boardId}`}>
  <Question {side} bind:selectedIndex questionId={parseInt(boardId * 3) + 0} />
  <Question {side} bind:selectedIndex questionId={parseInt(boardId * 3) + 1} />
  <Question {side} bind:selectedIndex questionId={parseInt(boardId * 3) + 2} />
</div>

<style>
  .board {
    background-color: rgb(82, 56, 185);
    height: 30%;
    margin-bottom: 20px;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    border-radius: 10px;
  }
  .b-0 {
    margin-left: 20%;
    width: 70%;
  }
  .b-1 {
    margin-left: 2%;
    width: 80%;
  }
  .b-2 {
    margin-left: 10%;
    width: 90%;
  }
  .b-3 {
    margin-left: 2%;
    width: 90%;
  }
  .b-4 {
    margin-left: 20%;
    width: 65%;
  }
  .b-5 {
    margin-left: 10%;
    width: 70%;
  }
</style>
