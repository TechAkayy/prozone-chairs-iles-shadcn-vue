<script setup lang="ts">
  import { format } from 'date-fns'
  import { Calendar as CalendarIcon } from 'lucide-vue-next'

  import { ref } from 'vue'
  import { cn } from '@/lib/utils'
  import { Button } from '@/components/ui/button'
  import { Calendar } from '@/components/ui/calendar'
  import {
    Popover,
    PopoverContent,
    PopoverTrigger,
  } from '@/components/ui/popover'

  const date = ref<Date>()

  const bookAppointment = () => {
    console.log(date.value)
  }
</script>

<template>
  <div id="appointment" class="p-6">
    <form>
      <div class="flex items-center justify-center">
        <div class="p-1">
          <Popover>
            <PopoverTrigger as-child>
              <Button
                :variant="'outline'"
                :class="
                  cn(
                    'w-[280px] justify-start text-left font-normal',
                    !date && 'text-muted-foreground',
                  )
                "
              >
                <CalendarIcon class="mr-2 h-4 w-4" />
                <span>{{ date ? format(date, 'PPP') : 'Pick a date' }}</span>
              </Button>
            </PopoverTrigger>
            <PopoverContent class="w-auto p-0">
              <Calendar v-model="date" />
            </PopoverContent>
          </Popover>
        </div>
        <div class="p-1">
          <button
            href="#"
            class="bg-primary-600 hover:bg-primary-700 inline-block px-6 py-2 rounded-full text-center text-white"
            type="button"
            @click="bookAppointment"
          >
            <span class="align-middle">Book An Appointment</span>
          </button>
        </div>
      </div>
    </form>
  </div>
</template>
