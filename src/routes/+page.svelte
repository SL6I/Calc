<script lang='ts'>
    import Sqrt from '$lib/icons/sqrt.svelte';
import sqrt from '$lib/icons/sqrt.svelte';
let eq:string = '';
function addTwoEq(value:string){
    eq += value
}
</script>

<svelte:head>
    <title>Calc</title>
</svelte:head>
<style>
    .sqrt-icon {
      width: 40px;
      height: 40px;
    }
  </style>
<div class="bg-slate-50 hover:bg-slate-100 h-fit w-fit rounded-3xl grid grid-cols-4 gap-3 py-6 px-4 font-semibold
    shadow-2xl">
    <div class="bg-blue-600 rounded-full col-span-4 h-12 flex
     items-center px-4 mb-2 text-white text-2xl font-semibold">
        {eq}
    </div>
    <button class="bg-[#f3f6fc]"> <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="currentColor" d="m18.5 3.5l-15 15l2 2l15-15M7 4a3 3 0 0 0-3 3a3 3 0 0 0 3 3a3 3 0 0 0 3-3a3 3 0 0 0-3-3m10 10a3 3 0 0 0-3 3a3 3 0 0 0 3 3a3 3 0 0 0 3-3a3 3 0 0 0-3-3"/></svg> </button>
    <button class="bg-[#f3f6fc] text-5xl"> <Sqrt /></button>
    <button class="bg-[#f3f6fc]"> CE </button>
    <button class="bg-[#1f2b54] text-white"> C </button>
    <button> 7 </button>
    <button> 8 </button>
    <button> 9 </button>
    <button class="bg-[#fd3f59] text-white"> <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="currentColor" d="M18 11H6a2 2 0 0 0 0 4h12a2 2 0 0 0 0-4"/></svg> </button>
    <button> 4 </button>
    <button> 5 </button>
    <button> 6 </button>
    <button class="bg-[#2285fd] text-white"> <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"><circle cx="12" cy="6" r="1" fill="currentColor"/><circle cx="12" cy="18" r="1" fill="currentColor"/><path d="M5 12h14"/></g></svg> </button>
    <button on:click={addTwoEq}> 1 </button>
    <button> 2 </button>
    <button> 3 </button>
    <button class="bg-[#f9c80e] text-white"> <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="currentColor" d="M20 6.91L17.09 4L12 9.09L6.91 4L4 6.91L9.09 12L4 17.09L6.91 20L12 14.91L17.09 20L20 17.09L14.91 12z"/></svg> </button>
    <button> . </button>
    <button on:click={addTwoEq}> 0 </button>
    <button> = </button>
    <button class="bg-[#63dc74] text-white"> <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20"><path fill="currentColor" d="M17 7v3h-5v5H9v-5H4V7h5V2h3v5z"/></svg> </button>
</div>
