<script>
  import { onMount } from "svelte";

  export let url 
  let data = [];

  onMount(async function() {
    const response = await fetch(url);
    const json = await response.json();
    data = json;
  });
</script>

<slot {data}/>