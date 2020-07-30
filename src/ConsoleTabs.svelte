<script>
  export let focusedOption = "DISTANCE";
  export let isExpanded = true;

  function setFocusedOption(option) {
    focusedOption = option;
  }

  function toggleIsExpanded() {
    isExpanded = !isExpanded;
  }
</script>

<div class="flex items-center justify-between">
  <nav class="flex items-center">
    <button
      on:click={() => setFocusedOption('DISTANCE')}
      class={`${focusedOption == 'DISTANCE' ? 'text-blue-600  focus:text-blue-800 focus:border-blue-700 border-blue-500' : 'text-gray-500  hover:text-gray-700 hover:border-gray-300 focus:text-gray-700 focus:border-gray-300'} inline-flex items-center px-1 py-4 text-sm font-medium leading-5 border-b-2 border-transparent group focus:outline-none`}>
      <svg
        class={`${focusedOption == 'DISTANCE' ? 'text-blue-600 focus:text-blue-800 focus:border-blue-700 border-blue-500' : 'text-gray-400 group-hover:text-gray-500 group-focus:text-gray-600'} -ml-0.5 mr-2 h-5 w-5`}
        fill="none"
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        viewBox="0 0 24 24"
        stroke="currentColor">
        <path
          d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0
          104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
      </svg>
      <span>Distance</span>
    </button>
    <button
      on:click={() => setFocusedOption('INFO')}
      class={`${focusedOption == 'INFO' ? 'text-blue-600  focus:text-blue-800 focus:border-blue-700 border-blue-500' : 'text-gray-500  hover:text-gray-700 hover:border-gray-300 focus:text-gray-700 focus:border-gray-300'} inline-flex items-center px-1 py-4 text-sm font-medium leading-5 border-b-2 border-transparent group focus:outline-none ml-2`}>
      <svg
        class={`${focusedOption == 'INFO' ? 'text-blue-600 focus:text-blue-800 focus:border-blue-700 border-blue-500' : 'text-gray-400 group-hover:text-gray-500 group-focus:text-gray-600'} -ml-0.5 mr-2 h-5 w-5`}
        fill="none"
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        viewBox="0 0 24 24"
        stroke="currentColor">
        <path d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
      </svg>
      <span>Aircraft Info</span>
    </button>
  </nav>
  {#if isExpanded}
    <button
      on:click={toggleIsExpanded}
      class={`text-blue-500 transition duration-150 ease-in-out border border-transparent rounded-md outline-none focus:border-blue-700 focus:shadow-outline-blue focus:outline-none`}>
      hide
    </button>
  {:else}
    <button
      on:click={toggleIsExpanded}
      class={`text-blue-500 transition duration-150 ease-in-out border border-transparent rounded-md outline-none focus:border-blue-700 focus:shadow-outline-blue focus:outline-none`}>
      show
    </button>
  {/if}
</div>
