<script lang="ts" setup>
import SecondaryButton from "../Buttons/SecondaryButton.vue";
import Section from "../Section.vue";
import Heading from "../Headings/Heading.vue";
import { ref } from "vue";
import { tools } from "../../data/tools.js";
tools.sort((a, b) => a.order - b.order);
let activeTools = tools.filter((t) => t.active);

const filtredTools = ref([]);
filtredTools.value = activeTools;
</script>
<template>
  <Section class="my-20" id="my-tools">
    <Heading :level=2 :size=3 text="Tools, die ich in meinem täglichen Arbeitsablauf verwende." :cursor=false />
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 lg:gap-8 xl:gap-12  mt-20 mb-20 transition-all">
      <div v-for="tool in activeTools" :key="tool.key"
        class="flex flex-col p-8 justify-center items-center bg-secondary shadow-lg shadow-default border border-default rounded-lg cursor-default hover:scale-110 hover:shadow-primary-color hover:shadow transition-transform ease-in-out duration-500">
        <div class="flex flex-col items-center">
          <img class="h-10 w-auto" :src="tool.icon.src" :alt="tool.icon.alt" />
          <h2 class="text-3xl mt-4">{{ tool.name }}</h2>
          <p class="text-md mt-4">{{ tool.description }}</p>
          <div class="flex justify-center w-full mt-8">
            <SecondaryButton :href="tool.link" target="_blank" text="Mehr lernen" icon="link" />
          </div>
        </div>
      </div>
    </div>
  </Section>
</template>
