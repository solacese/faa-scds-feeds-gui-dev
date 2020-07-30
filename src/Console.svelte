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
    <div transition:slide class="w-full mt-4 h-72">
      <!-- header -->
      <div class="flex items-center p-3 rounded-t-lg bg-gray-50">
        <div class="tracking-wider text-gray-500 uppercase w-36">Name</div>
        <div class="ml-4 tracking-wider text-gray-500 uppercase w-28">Identifier</div>
        <div class="ml-4 tracking-wider text-gray-500 uppercase">Distance</div>
      </div>
      <DistanceList />
    </div>
  {/if}
</div>

<ConsoleSubscriptionManager />
