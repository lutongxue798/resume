<script setup lang='ts'>
import zhenghedao from '~/static/zhenghedao.png'
import baoliwei from '~/static/baoliwei.png'
import yangfan from '~/static/yangfan.png'
import jixing from '~/static/jixing.png'
import waiguoyu from '~/static/waiguoyu.png'
import boming from '~/static/boming.png'

const project = [
  {
    projeceName: '博明小管家',
    previewImg: boming,
    projectDesc: '面向社会用户的第三方官方售药平台',
  },
  {
    projeceName: '极星Polestar',
    previewImg: jixing,
    projectDesc: '沃尔沃汽车集团和浙江吉利控股集团共同拥有的全球高性能电动汽车品牌,提供汽车在线查询选购。',
  },
  {
    projeceName: '保利威律师官网',
    link: 'http://www.polywelllaw.cn/',
    previewImg: baoliwei,
    projectDesc: '保利威律师致力于为客户提供专业律师服务。',
  },

  {
    projeceName: '福建扬帆计划',

    previewImg: yangfan,
    projectDesc: '福建在线求职平台',
  },

  {
    projeceName: '海外少年宫',
    previewImg: waiguoyu,
    projectDesc: '海外少年宫隶属于海淀外国语教育集团，在周末，寒暑假【面向社会开放】，充分调动集团教育资源为社会服务。',
  },

  {
    projeceName: '正和岛',
    link: 'http://mp.zhisland.com/router/conference/',
    previewImg: zhenghedao,
    projectDesc: '正和岛企业家签到，活动流程展示平台。',
  },

]
</script>

<template>
  <div mt15>
    <div grid cols-1 gap-6 md:cols-3>
      <div v-for="(item, index) in project" :key="index" rd-2 p-4 class="bg-[#373738]">
        <img :src="item.previewImg" m-auto block rd-2 style="object-fit: contain;">
        <div>
          <p my4 text-center text-lg>
            {{ item.projeceName }}
          </p>
          <p mt2 text-center text-sm op50>
            {{ item.projectDesc }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
