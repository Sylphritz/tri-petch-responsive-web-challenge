<template>
  <Section
    title="Athlets"
    title-class="sm:ml-auto sm:pl-0 sm:w-[58%] xl:w-[717px]"
    title-right
    class="relative"
  >
    <div
      class="sm:absolute relative container sm:h-full top-0 sm:left-1/2 sm:-translate-x-1/2 mt-[11px] sm:mt-0 mb-[-55px] sm:mb-0 pointer-events-none text-center z-10"
    >
      <div class="sm:absolute top-0 left-0 xl:left-[-64px] 2xl:left-0">
        <img
          src="/images/football-player-resized.png"
          class="hidden xl:inline-block"
        />
        <img
          src="/images/football-player-tablet-resized.png"
          class="hidden sm:inline-block xl:hidden mt-[14px]"
        />
        <img
          src="/images/football-player-mobile-resized.png"
          class="inline-block sm:hidden"
        />
      </div>
    </div>
    <div class="relative hidden sm:block">
      <AthletsConnection />
      <AthletsCollaboration />
      <AthletsGrowth />
    </div>
    <div class="relative block sm:hidden">
      <SliderCarousel :items-to-show="1" :items-to-scroll="1">
        <SliderSlide key="athletsConnection">
          <AthletsConnection />
        </SliderSlide>
        <SliderSlide key="athletsCollaboration">
          <AthletsCollaboration />
        </SliderSlide>
        <SliderSlide key="athletsGrowth">
          <AthletsGrowth />
        </SliderSlide>

        <template #addons>
          <SliderPagination />
        </template>
      </SliderCarousel>
    </div>
  </Section>
  <Section
    title="Players"
    class="relative pt-[19px] sm:pt-[52px] xl:pt-[124px]"
  >
    <div
      class="overflow-hidden xl:overflow-visible relative sm:absolute container sm:h-full top-0 sm:left-1/2 sm:-translate-x-1/2 mt-[22px] sm:mt-0 mb-[-35px] sm:mb-0 pointer-events-none text-center z-10"
    >
      <div
        class="sm:absolute top-0 right-0 sm:right-[-254px] xl:right-[-64px] 2xl:right-0"
      >
        <img
          src="/images/basketball-player-resized.png"
          width="991"
          height="815"
          class="inline-block w-auto ml-[-10px] sm:ml-0 h-[249px] sm:mt-[33px] sm:h-[568px] xl:h-auto xl:mt-0"
        />
      </div>
    </div>
    <div class="relative hidden sm:block">
      <PlayersConnection />
      <PlayersCollaboration />
      <PlayersGrowth />
    </div>
    <div class="relative block sm:hidden">
      <SliderCarousel :items-to-show="1" :items-to-scroll="1">
        <SliderSlide key="playerConnection">
          <PlayersConnection />
        </SliderSlide>
        <SliderSlide key="playerCollaboration">
          <PlayersCollaboration />
        </SliderSlide>
        <SliderSlide key="playerGrowth">
          <PlayersGrowth />
        </SliderSlide>

        <template #addons>
          <SliderPagination />
        </template>
      </SliderCarousel>
    </div>
  </Section>
</template>

<script lang="ts" setup></script>
