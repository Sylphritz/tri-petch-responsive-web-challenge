<template>
  <section>
    <div class="container mx-auto">
      <h1
        class="uppercase text-[#E7E7E7] text-[50px] leading-[58.59px] sm:text-[90px] sm:leading-[105.47px] px-[18px] sm:px-[30px] xl:p-0"
        :class="[titleClass]"
      >
        {{ title }}
      </h1>
    </div>
    <slot />
  </section>
</template>

<script lang="ts" setup>
defineProps({
  title: {
    type: String,
    required: true,
  },
  titleClass: {
    type: String,
  },
  titleRight: {
    type: Boolean,
  },
})
</script>
