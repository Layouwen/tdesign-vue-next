<template>
  <t-space>
    <t-dropdown :options="options" @click="clickHandler">
      <t-space>
        <t-button variant="text">
          更多
          <template #suffix> <t-icon name="chevron-down" size="16" /></template>
        </t-button>
      </t-space>
    </t-dropdown>
  </t-space>
</template>
<script setup>
import { MessagePlugin } from 'tdesign-vue-next';

const options = [
  { content: '操作一', value: 1 },
  { content: '操作二', value: 2 },
  { content: '操作三', value: 3 },
  { content: '操作四', value: 4 },
];

const clickHandler = (data) => {
  MessagePlugin.success(`选中【${data.content}】`);
};
</script>
