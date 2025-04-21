<template>
  <div v-if="onlyPrice" class="flex flex-col items-end justify-start">
    <div class="text-xs text-nowrap">{{ `${remainingData.priceUnit}${remainingData.remainingPrice}` }}
    </div>
  </div>
  <div v-else-if="onlyDate" class="flex flex-col items-end justify-start">
    <div class="text-xs text-nowrap">{{ remainingData.date || '-' }}</div>
  </div>
  <div v-else class="flex flex-col items-end justify-start">
    <div class="text-xs text-nowrap">{{ remainingData.date || '-' }}</div>
    <Progress v-if="remainingData.date" :class="cn(
    'h-0.5 rounded-none',
    percentageFormat >= 80 && '[&_[data-state=loading]]:bg-red-500',
    (percentageFormat >= 50 && percentageFormat < 80) && '[&_[data-state=loading]]:bg-yellow-500',
    (percentageFormat > 0 && percentageFormat < 50) && '[&_[data-state=loading]]:bg-green-500',
  )" :model-value="percentageFormat" data-state="loading" />
  </div>
</template>
<script setup>
import { Progress } from '@/components/shadcn/ui/progress';
import { parseRemainingData } from '@/lib/function';
import { cn } from '@/lib/utils';
import { computed } from 'vue';

const props = defineProps({
  showIcon: {
    type: Boolean,
    default: false
  },
  onlyDate: {
    type: Boolean,
    default: false
  },
  onlyPrice: {
    type: Boolean,
    default: false
  },
  data: {
    type: Object,
    default() {
      return {
        amount: '0.00',
        startDate: '',
        endDate: '',
        cycle: '年',
        autoRenewal: '0',
        remainingPrice: 0.00,
        priceUnit: '',
        priceValue: '',
      }
    }
  },
})

const percentageFormat = computed(() => {
  return parseFloat(remainingData.value.percent);
})

const remainingData = computed(() => {
  return parseRemainingData(props.data);
});
</script>

<style scoped>
:global(.el-progress .el-progress-bar .el-progress-bar__outer) {
  border-radius: unset;
}

:global(.el-progress .el-progress-bar .el-progress-bar__inner) {
  border-radius: unset;
}
</style>
