<script lang="ts" >
  let isvisible = false;
  export let title= "";
  export let content= "";
  const plus = '/images/icon-plus.svg';
  const minus = '/images/icon-minus.svg';

  function togglevisibility() {
    isvisible = !isvisible;
  }
</script>
<div class="py-5">
  <div class="flex items-center mx-7 justify-between">
    <p class="font-semibold 
      text-md 
      text-black 
      hover:text-violet-500 hover:cursor-pointer" 
      on:click={togglevisibility} >{title}</p>
    <img
      src={isvisible ? minus : plus}
      alt="plus"
      on:click={togglevisibility}
      class="w-7 h-7 hover:cursor-pointer"
    >
  </div>
  {#if isvisible}
    <div class="pt-5">
      <p class="text-gray-500 font-normal mx-7">{content}</p>
    </div>
  {/if}
</div>
