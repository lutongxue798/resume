<script setup lang="ts" generic="T extends any, O extends any">
defineOptions({
  name: 'IndexPage',
})

const tabs = [
  {

    icon: 'i-carbon:align-box-middle-left',
    name: 'Personal Information',
  },
  {
    icon: 'i-carbon:favorite',
    name: 'Technical Stack',
  },

  {
    icon: 'i-carbon:ibm-cloud-projects',
    name: 'Project Overview',
  },
]

const tabActive = ref(0)
</script>

<template>
  <div>
    <h1 font-Hubot text-6xl font-800 font-medium md:mt-10>
      <span>Hello,</span>
      <span mt4>I'm Lu. </span>
    </h1>
    <div mt10>
      <p> ·  Front-end developer</p>
      <p mt2>
        ·  Currently working at BoMing
      </p>
    </div>

    <div my6 flex flex-wrap items-center gap-4>
      <button
        v-for="(tab, index) in tabs" :key="index"
        class="rd-1 p-2 text-sm icon-btn dark:bg-[#373738] md:text-base"
        w-fit flex items-center @click="tabActive = index"
      >
        <p :class="tab.icon" mr2 h-6 w-6 />
        <p>{{ tab.name }}</p>
      </button>
    </div>

    <Transition name="fade">
      <TheInfo v-if="tabActive === 0" />
    </Transition>
    <Transition name="fade">
      <TheTechnology v-if="tabActive === 1" />
    </Transition>
    <Transition name="fade">
      <TheProjectView v-if="tabActive === 2" />
    </Transition>
  </div>
</template>
