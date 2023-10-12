<script>
  import faq from "../../data/faq.json";

  export let selectedIndex;
  export let questionId;
</script>

<div
  class="question-block"
  on:click={() => {
    selectedIndex = questionId;
  }}
  on:keypress={() => {
    selectedIndex = questionId;
  }}
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
    /* height: 30%; */
    vertical-align: middle;
  }
  .question-block:hover {
    cursor: pointer;
  }
</style>
