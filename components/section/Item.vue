<template>
  <div
    class="flex flex-col justify-center p-[18px] sm:p-[30px] pt-[72px] sm:pt-[30px] xl:p-0"
  >
    <div class="container mx-auto">
      <div
        class="flex flex-col gap-[20px] sm:gap-[21px]"
        :class="[{ 'sm:ml-auto': alignRight }, innerClass]"
      >
        <div class="flex flex-row items-start">
          <div
            class="item-number flex-none relative mr-[10px] tracking-[1.5px] text-[14px] leading-[16.41px] sm:text-[18px] sm:leading-[21.09px] mt-[7px] sm:mt-[5px]"
            :class="[
              { 'white-underline': darkMode },
              numberColor ?? 'text-black',
            ]"
          >
            {{ number }}
          </div>
          <h2
            class="uppercase text-[#C2C2C2] tracking-[1.5px] text-[28px] leading-[32.81px] sm:text-[36px] sm:leading-[42.19px]"
          >
            {{ title }}
          </h2>
        </div>
        <p
          class="text-[15px] leading-[17.58px] sm:text-[18px] sm:leading-[28px] xl:text-[20px]"
          :class="{ 'text-white': darkMode }"
        >
          <slot />
        </p>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
defineProps({
  number: {
    type: String,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
  darkMode: {
    type: Boolean,
  },
  numberColor: {
    type: String,
  },
  alignRight: {
    type: Boolean,
  },
  innerClass: {
    type: String,
  },
})
</script>

<style lang="scss" scoped>
.item-number {
  &::after {
    @apply right-[0] sm:right-[2px] top-[100%] mt-[2px] sm:mt-[4px] h-[4px] sm:h-[5px];

    content: '';
    position: absolute;
    left: 1px;
    background-color: #603ebe;
    border-radius: 99999px;
  }

  &.white-underline::after {
    background-color: #ffffff;
  }
}
</style>
