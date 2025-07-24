<template>
  <SidebarProvider>
      <Sidebar />
    <main class="w-full">
      <div>
        <Header />
      </div>
      <div class="p-4">
        <slot />
      </div>
    </main>
  </SidebarProvider>
</template>

<script setup>
import Sidebar from '@/layout/Sidebar.vue'
import Header from '@/layout/Header.vue'
import { SidebarProvider, SidebarTrigger } from '@/components/ui/sidebar'

</script>

<style lang="scss">
  
</style>