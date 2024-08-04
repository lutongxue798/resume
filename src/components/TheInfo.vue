<script lang="ts" setup>
const personalInformation = [{
  // icon: 'i-carbon:id-management',
  label: 'Name',
  value: 'luwenrui',
}, {
  label: 'Wechat',
  value: 'vat_xl',
}, {
  // icon: 'i-carbon:email',
  label: 'Mail',
  value: 'luwenruishiwo@163.com',
}, {
  // icon: 'i-carbon:location',
  label: 'Address',
  value: 'No. 18 Shuangta East Street',
}]
</script>

<template>
  <div mt15>
    <div class="rd-2 bg-[#212121] py4">
      <div
        v-for="(item, index) in personalInformation" :key="index"
        class="relative flex items-center border-b-1 border-b-solid py4 text-base dark:border-[#262626FF]"
      >
        <p mr5 w-100px>
          {{ item.label }}
        </p>
        <p font-normal op50>
          {{ item.value }}
        </p>
      </div>
    </div>
  </div>
</template>

<style>
a {
  background: #262626;
}
</style>
