<script>
  import faq from "../../data/faq.json";

  export let side;
  export let selectedIndex;
  export let questionId;

  const handleKeyPress = () => {
    selectedIndex = questionId;
  };
</script>

<div
  class="question-block color-{questionId - (questionId % 3)} {side}"
  on:click={handleKeyPress}
  on:keypress={handleKeyPress}
>
  <!-- fallback if no question exists -->
  {#if !faq[questionId]}
    <div>Question not found</div>
  {:else}
    <div>{faq[questionId].question}</div>
  {/if}
</div>

<style>
  .question-block {
    vertical-align: middle;
    line-height: 1.5;
    text-indent: 5px;
    font-weight: bold;
  }
  .left {
    border-bottom-left-radius: 7px;
    border-top-left-radius: 7px;
    margin-left: 15px;
  }
  .right {
    border-bottom-right-radius: 7px;
    border-top-right-radius: 7px;
    margin-right: 15px;
  }
  .color-0 {
    background-color: rgb(231, 137, 182);
    box-shadow: 3px 3px 50px 1px rgb(231, 137, 182);
  }
  .color-3 {
    background-color: rgb(173, 95, 223);
    box-shadow: 3px 3px 30px 1px rgb(173, 95, 223);
  }
  .color-6 {
    background-color: rgb(246, 198, 97);
    box-shadow: 3px 3px 30px 1px rgb(246, 198, 97);
  }
  .color-9 {
    background-color: rgb(218, 114, 207);
    box-shadow: 3px 3px 30px 1px rgb(218, 114, 207);
  }
  .color-12 {
    background-color: rgb(105, 205, 216);
    box-shadow: 3px 3px 30px 1px rgb(105, 205, 216);
  }
  .color-15 {
    background-color: rgb(173, 113, 247);
    box-shadow: 3px 3px 30px 1px rgb(173, 113, 247);
  }
  .question-block:hover {
    cursor: pointer;
  }
</style>
