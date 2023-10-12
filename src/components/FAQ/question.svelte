<script>
  import faq from "../../data/faq.json";

  export let selectedIndex;
  export let questionId;

  const handleKeyPress = () => {
    selectedIndex = questionId;
  };
</script>

<div
  class="question-block"
  on:click={handleKeyPress}
  on:keypress={handleKeyPress}
>
  <!-- fallback if no question exists -->
  {#if !faq[questionId]}
    <div>Question not found</div>
  {:else}
    <div>Q: {faq[questionId].question}</div>
  {/if}
</div>

<style>
  .question-block {
    vertical-align: middle;
    line-height: 1.5;
  }
  .question-block:hover {
    cursor: pointer;
  }
</style>
