<!-- <template>
  <div class="flex flex-col gap-3">
    <div>
      <UBadge class="mb-5 uppercase" color="white" size="lg" variant="solid"
        >Career</UBadge
      >
    </div>
    <h1 class="text-3xl md:text-5xl font-bold">Experience</h1>
    <p>My professional journey.</p>
    <Accordion />
  </div>
</template>

<script lang="ts" setup></script>

<style scoped></style> -->

<script setup lang="ts">
import {
  AccordionContent,
  AccordionHeader,
  AccordionItem,
  AccordionRoot,
  AccordionTrigger,
} from "radix-vue";
import { Icon } from "@iconify/vue";
</script>

<template>
  <div class="flex flex-col gap-3">
    <div>
      <UBadge class="mb-5 uppercase" color="white" size="lg" variant="solid"
        >Career</UBadge
      >
    </div>
    <h1 class="text-3xl md:text-5xl font-bold">Experience</h1>
    <p>My professional journey.</p>
    <AccordionRoot
      class="bg-mauve6 -[300px] rounded-md shadow-[0_2px_10px] shadow-black/5"
      default-value="item-1"
      type="single"
      :collapsible="true"
    >
      <template>
        <AccordionItem
          value="item-1"
          class="focus-within:shadow-mauve12 mt-px overflow-hidden first:mt-0 first:rounded-t last:rounded-b focus-within:relative focus-within:z-10 focus-within:shadow-[0_0_0_2px]"
        >
          <AccordionHeader class="flex">
            <AccordionTrigger
              class="text-primary-700 shadow-mauve6 bg-primary-50 hover:bg-mauve2 flex h-[45px] flex-1 cursor-default items-center justify-between px-5 text-[15px] leading-none shadow-[0_1px_0] outline-none group"
            >
              <div
                class="flex items-center gap-2 text-xl font-semibold opacity-60 text-primary-700"
              >
                <i class="i-heroicons-rectangle-stack"></i>
                <span>Product Manager - Giftawish</span>
              </div>
              <Icon
                icon="radix-icons:chevron-down"
                class="text-green10 ease-[cubic-bezier(0.87,_0,_0.13,_1)] transition-transform duration-300 group-data-[state=open]:rotate-180"
              />
            </AccordionTrigger>
          </AccordionHeader>
          <AccordionContent
            class="text-mauve11 bg-mauve2 data-[state=open]:animate-slideDown data-[state=closed]:animate-slideUp overflow-hidden text-[15px]"
          >
            <div class="px-5 py-4 opacity-50">
              <ul class="list-disc list-inside space-y-3">
                <li>
                  Responsible for planning sprint for the design and development
                  team
                </li>
                <li>
                  Responsible for writing User stories and user journeys to
                  improve the product team's understanding of required features
                  and functionalities
                </li>
                <li>
                  Work with cross functional teams to enhance a good user
                  experience for the customers. - Worked with the marketing team
                  to facilitate a great product marketing.
                </li>
                <li>
                  Assist the product lead to deliver good product services to
                  our customers to facilitate a good user experience
                </li>
              </ul>
            </div>
          </AccordionContent>
        </AccordionItem>
      </template>
    </AccordionRoot>
  </div>
</template>
