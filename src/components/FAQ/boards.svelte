<script>
  import MediaQuery from "../../MediaQuery.svelte";

  import Answer from "./answer.svelte";
  import QuestionBoard from "./questionBoard.svelte";
  import MobileFaqBoard from "./MobileFAQBoard.svelte";

  import faq from "../../data/faq.json";

  // keep track of selected index
  let selectedIndex = 0;
  let selectedAnswer = faq[selectedIndex].answer;
  $: selectedAnswer = faq[selectedIndex].answer;

  // keep track of expanded state (for mobile only)
  let questionList = new Array(faq.length).fill(false);

  // logic for mobile question toggle
  const toggle = (index) => {
    questionList[index] = !questionList[index];
  };
</script>

<MediaQuery query="(max-width: 768px)" let:matches>
  <div class="all">
    {#if matches}
      <div class="mobileBoard">
        <MobileFaqBoard />
        {JSON.stringify(questionList)}
        {#each faq as item, index (item.question)}
          <ol>
            <li>
              <button on:click={() => toggle(index)}>
                {questionList[index] ? "▼" : "▶"}
                {item.question}
              </button>
              {#if questionList[index]}
                {item.answer}
              {/if}
            </li>
          </ol>
        {/each}
      </div>
    {:else}
      <div class="left">
        <QuestionBoard side="left" bind:selectedIndex boardId="0" />
        <QuestionBoard side="left" bind:selectedIndex boardId="1" />
        <QuestionBoard side="left" bind:selectedIndex boardId="2" />
      </div>
      <div class="center">
        <Answer bind:answer={selectedAnswer} />
      </div>
      <div class="right">
        <QuestionBoard side="right" bind:selectedIndex boardId="3" />
        <QuestionBoard side="right" bind:selectedIndex boardId="4" />
        <QuestionBoard side="right" bind:selectedIndex boardId="5" />
      </div>
    {/if}
  </div>
</MediaQuery>

<style>
  .all {
    display: flex;
    flex-direction: row;
    width: 100vw;
    color: white;
  }
  .all > * {
    width: 30%;
  }

  .left {
    left: 0;
    align-items: left;
    /* background-color: lightcoral; */
  }
  .right {
    right: 0;
    align-items: right;
    /* background-color: lightblue; */
  }

  .center {
    width: 40%;
    justify-content: center;
    align-items: center;
    /* background-color: lightgreen; */
  }
</style>
