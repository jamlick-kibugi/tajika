<template>
  <div id="downloadSection" class="mt-16">
    <h2 class="font-extrabold text-2xl">Download</h2>
    <div class="stepC mt-6">
      <p>Please complete the checklist to proceed,</p>
      <Check
        v-for="(item, index) in downloadCheckList"
        :downloadCheckList="downloadCheckList"
        :item="item"
        :key="index"
        :index="index"
      />
      <button
        ref="downloadPackage"
        @click="downloadPackage"
        class="inline-block bg-gray-700 leading-none text-2xl tracking-wide border-2 border-transparent font-extrabold p-6 rounded mt-12 select-none transition-colors duration-200 focus:outline-none"
        :title="
          downloadChecked
            ? ''
            : 'Complete the checklist to download the package'
        "
        :class="
          downloadChecked
            ? 'bg-emerald-600 cursor-pointer text-white focus:bg-emerald-500 hover:bg-emerald-500'
            : 'cursor-not-allowed text-black'
        "
      >
        GENERATE
      </button>
      <p class="mt-6 border p-4 rounded border-gray-700 text-gray-400">
        The business link has been generate on this link if you have subscribed
        <NuxtLink
          to="/hosting-guide"
          class="cursor-pointer underline font-extrabold text-emerald-600 hover:text-emerald-500 focus:text-emerald-500 transition-colors duration-200"
          >This&nbsp;Link</NuxtLink
        >
        to get your digital business card online.
        <br /><br />
        If you find this service valuable to you or your business, Subscribe to enjoy it.
        <br /><a
          class="inline-block font-extrabold tracking-wide leading-none shrink-0 p-3 text-white bg-gray-700 rounded hover:bg-gray-600 focus:bg-gray-600 transition-colors duration-200 mt-4"
          href="https://www.myeneza.co.ke/activate"
          rel="noreferrer"
          target="_blank"
          >Subscribe</a
        >
      </p>
    </div>
  </div>
</template>

<script>
import Check from '@/components/Check'
export default {
  props: ['downloadCheckList', 'downloadChecked', 'downloadPackage'],
  components: {
    Check,
  },
}
</script>