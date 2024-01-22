<script lang="ts">
  import Infos from '$components/Infos.svelte';
  let background = "/images/background-pattern-desktop.svg";
  let star = "/images/icon-star.svg";
  let data = {
    faq1: {
      question: "How to do something?",
      answer: "Here is the answer to your question.",
    },
    faq2: {
      question: "What is something?",
      answer: "Here is the explanation of that something.",
    },
    faq3: {
      question: "Why is something important?",
      answer: "Here is why it matters.",
    },
    faq4: {
      question: "When does something happen?",
      answer: "Here is the timeline of events.",
    },
  };</script>
<div class="relative">
  <img src={background} alt="background">
   <div class="flex items-center justify-center top-2/3">
    <div class="bg-white rounded-lg h-auto w-2/5 absolute z-1 top-2/3">
      <div class="flex py-5 items-center space-x-4">
        <img src={star} alt="star" class="ml-7 h-9 w-9">
        <h1 class="text-5xl font-bold">FAQs</h1>
      </div>
      {#each Object.values(data) as {question, answer}}
        <Infos title={question} content={answer}/>
      {/each}
    </div>
  </div>
</div>
