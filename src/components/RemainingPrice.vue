<template>
  <TooltipProvider>
    <Tooltip>
      <TooltipTrigger>
        <div class="flex flex-row text-primary/80 drop-shadow justify-start items-center">
          <span :class="cn(
            'font-money tracking-widest relative block -translate-y-2',
            `before:absolute before:block before:content-[''] before:-bottom-1 before:-left-1 before:-right-1 z-10 before:h-0 before:-z-10 before:border-primary before:border-b before:-rotate-183`,
            `after:absolute after:block after:content-[''] after:-bottom-2 after:-left-1 after:-right-1 z-10 after:h-0 after:-z-10 after:border-primary after:border-b after:-rotate-2`,
          )">{{ ramainingData.remainingPrice }}{{ ramainingData.priceUnit }}
          </span>
        </div>
      </TooltipTrigger>
      <TooltipContent side="right" class="ml-2 bg-muted/80 text-muted-foreground">
        <p>{{ $t('remaining') }}</p>
      </TooltipContent>
    </Tooltip>
  </TooltipProvider>
</template>
<script setup>
import {
  Tooltip,
  TooltipContent,
  TooltipProvider,
  TooltipTrigger
} from '@/components/shadcn/ui/tooltip';
import { parseRemainingData } from '@/lib/function';
import { cn } from '@/lib/utils';
import { computed } from 'vue';

const props = defineProps({
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

const ramainingData = computed(() => {
  return parseRemainingData(props.data);
})
</script>

<style scoped></style>
