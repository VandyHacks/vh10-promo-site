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
        <div class="boardContainer">
          <MobileFaqBoard />
        </div>
        <div class="qAndA">
        {#each faq as item, index (item.question)}
          <ol>
            <li>
              <button on:click={() => toggle(index)} class="mobileQuestion">
                {questionList[index] ? "▼" : "▶"}
                {item.question}
              </button>
              <div class="answerText">
              {#if questionList[index]}
                {item.answer}
              {/if}
              </div>
            </li>
          </ol>
        {/each}
        </div>
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

  .mobileBoard {
    position: relative;
    align-items: center;
    justify-content: center;
    top: 100px;
    /* background: green; */
    width: 100vw;
  }

  .boardContainer {
    width:90vw;
    margin: 0 auto;
    position: relative;
    align-items: center;
    justify-content: center;
  }

  .qAndA {
    position: absolute;
    top: 10%;
    left: 50%;
    transform: translateX(-50%);
    width: 70vw;
    max-height: 70%;
    overflow: auto;
  }

 
  .answerText {
    padding-left: 10px;
    font-size: 1.3em;
    
  }

  button {
      margin: 0;
      padding: 0;
      border: none;
      background: none;
      text-shadow: 0 0 7px #fff;
      color: white;
      padding-left: 10px;
      padding-top: 2vh;
      font-size: 1.5em;
      text-align: left;
    }

    ol {
      margin: 5px;
      padding: 0;
      list-style: none;
    }
</style>