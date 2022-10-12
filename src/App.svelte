<script lang="ts">
  import { onMount } from "svelte";

  let comic = ""
  onMount(async () => {
    await fetch("https://web-production-32e6.up.railway.app/https://xkcd.com/info.0.json")
    .then((response) => response.json())
    .then((data) => {
      console.log(data);
      comic = data.img
    })
  })
  
</script>

<img class="w-full h-full" src={comic} alt="daily comic">

<style>
</style>
