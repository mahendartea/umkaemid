<template>
  <div class="flex justify-center mx-auto">
    <button
      type="button"
      class="flex bg-yellow-600 py-2 px-5 rounded-lg items-center"
      disabled
    >
      <!-- svg spinner animation taiwindcss -->
      <svg
        class="animate-spin -ml-1 mr-3 h-5 w-5 text-white"
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
      >
        <circle
          class="opacity-25"
          cx="12"
          cy="12"
          r="10"
          stroke="currentColor"
          stroke-width="4"
        ></circle>
        <path
          class="opacity-75"
          fill="currentColor"
          d="M4 12a8 8 0 018-8v8z"
        ></path>
      </svg>
      <p class="text-white">Processing...</p>
    </button>
  </div>
</template>
