<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>持续学习</template>
    在我们的应用中，我们不只是创造一个产品;我们点燃了一种持续学习的文化。从激发创造力到实现想法，我们始终如一地推动用户超越自我，以独特的方式整合学习体验。这不仅仅是一个应用程序;这是一个不断发展的智慧阶段，引导你走向永恒的知识之旅。
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>应用程序开发</template>
    在浩瀚的创意海洋中，我们利用专注的力量，将每一个独特的想法精心制作成创新的App产品。我们不仅激发灵感，而且优先考虑实现，用技术奇迹点燃梦想。我们的团队专注于每一个细节，努力将创意转化为现实，让您的概念在数字领域扬帆起航，不断超越界限。
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>量化交易</template>
    ＂创新算法，回报最大化!我们的量化交易团队致力于为客户制定卓越的交易策略。通过复杂的算法和市场分析，我们帮助您实现回报最大化。加入我们，迎接未来金融市场的挑战，做出准确的决策，实现财富增长!”
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>专利产品</template>
    “我们的专利产品以创新、质量和卓越而自豪。通过严格的质量控制和前瞻性的设计，我们致力于为客户提供独特的体验。每一款专有产品都代表着我们对高标准的承诺，为您带来无与伦比的价值和满意度。”
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>个人偏好</template>
    你有创意和想法，我们帮你实现.
  </WelcomeItem>
</template>