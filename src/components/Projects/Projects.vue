<script lang="ts" setup>
import Heading from "../../components/Headings/Heading.vue";
import Section from "../../components/Section.vue";
import ProjectCard from "./ProjectCard/ProjectCard.vue";
import { projects } from "../../data/projects.js"
</script>

<template>
  <!--
  <Section id="projects">
    <Heading :level="2" :size="1" text="Projekte" :cursor="true" />

    <div class="grid grid-auto-fit-xl gap-8 my-16 place-items-center">
      <ProjectCard v-for="project in projects" :key="project.id" :project="project" />
    </div>

    TODO: Implement dedicated projects overview page
            <div class="flex justify-center mb-20">
                <PrimaryButton text="Alle Projekte" href="/projects" icon="diagram-project" />
            </div>
  </Section>
    -->
</template>
