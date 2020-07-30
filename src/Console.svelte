<script>
  import { slide } from "svelte/transition";
  import Tabs from "./ConsoleTabs.svelte";
  import DistanceList from "./DistanceList.svelte";
  import ConsoleSubscriptionManager from "./ConsoleSubscriptionManager.svelte";

  export let isExpanded = true;
  export let focusedOption = "DISTANCE";
</script>

<div class="p-4 overflow-hidden bg-white rounded-lg shadow sm:p-6">
  <Tabs bind:focusedOption bind:isExpanded />
  {#if isExpanded}
    <div transition:slide class="w-full m-2 h-72">
      <DistanceList />
    </div>
  {/if}
</div>

<ConsoleSubscriptionManager />
