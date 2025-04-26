<template>
  <!-- 其他内容... -->
  
  <!-- 今日诗词容器 -->
  <div class="more-content">
    <span id="jinrishici-sentence">正在加载今日诗词...</span>
  </div>
</template>

<script setup>
// 原脚本内容保持不变...
import { onMounted } from 'vue'

// 动态加载诗词脚本
onMounted(() => {
  const script = document.createElement('script')
  script.src = 'https://sdk.jinrishici.com/v2/browser/jinrishici.js'
  script.charset = 'utf-8'
  document.body.appendChild(script)
})
</script>

<style lang="scss" scoped>
.more-content {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 20px;
  width: 100%;
  height: 100%;
  min-height: 40px; /* 确保有最小高度 */
  
  /* 诗词样式 */
  #jinrishici-sentence {
    font-size: 19px;
    color: #ffffff;
    font-style: italic;
    transition: opacity 0.3s;
    
    &:hover {
      opacity: 0.8;
    }
  }
}
</style>
