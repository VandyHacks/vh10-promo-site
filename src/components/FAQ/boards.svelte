<script>
  import MediaQuery from "../../MediaQuery.svelte";

  import Answer from "./answer.svelte";
  import QuestionBoard from "./questionBoard.svelte";
  import MobileFaqBoard from "./MobileFAQBoard.svelte";
  import DuckFinal from "./duckFinal.svelte";
  import DuckInitial from "./duckInitial.svelte";

  import faq from "../../data/faq.json";

  // keep track of selected index
  let selectedIndex = -1;
  let selectedAnswer = "Click on a question to see the answer!";
  // change answer when selected index changes only if it is a valid index
  $: if (selectedIndex >= 0) {
    selectedAnswer = faq[selectedIndex].answer;
  }

  // keep track of expanded state (for mobile only)
  let questionList = new Array(faq.length).fill(false);

  // logic for mobile question toggle
  let icons = new Array(faq.length).fill(DuckInitial);

  const toggle = (index) => {
    questionList[index] = !questionList[index];
    icons[index] = questionList[index] ? DuckFinal : DuckInitial;
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
                <div
                  class="duckAndQuestion"
                  on:click={() => toggle(index)}
                  on:keypress={() => toggle(index)}
                >
                  <svelte:component this={icons[index]} />
                  <span class="questionMobile">{item.question}</span>
                </div>
                <div class="answerText">
                  {#if questionList[index]}
                    <br />
                    {@html item.answer}
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
    width: 90vw;
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
  .duckAndQuestion {
    display: flex;
    flex-direction: row;
    align-items: center;
  }
  .questionMobile {
    margin-left: 5px;
  }
  .answerText {
    padding-left: 10px;
    text-align: left;
    width: 80%;
    margin-left: 45px;
  }

  ol {
    margin: 5px;
    padding: 0;
    list-style: none;
  }
</style>
