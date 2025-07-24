<script setup lang="">
import { SidebarProvider, SidebarTrigger } from "@/components/ui/sidebar";
import DashboardLayout from "@/layout/DashboardLayout.vue";
import Dashboard from "@/pages/Dashboard.vue";
import { Button } from "@/components/ui/button";
import Sidebar from "@/layout/Sidebar.vue";
</script>

<template>
  <DashboardLayout>
    <Dashboard />
  </DashboardLayout>
</template>