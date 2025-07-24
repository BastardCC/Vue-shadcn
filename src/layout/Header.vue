<template>
  <div class="flex justify-between bg-white p-4 border-sidebar-border border-b items-center">
    <div class="relative w-full max-w-sm items-center">
      <Input id="search" type="text" placeholder="Search a patient..." class="pl-10" />
      <span class="absolute start-0 inset-y-0 flex items-center justify-center px-2">
        <Search class="size-5 text-muted-foreground" />
      </span>
    </div>
    <div class="flex items-center gap-4">
      <p class="mx-4 font-semibold">John Doe</p>
      <Menubar class="!bg-transparent border-none shadow-none">
        <MenubarMenu>
          <MenubarTrigger class="cursor-pointer">
            <Avatar>
              <AvatarImage src="https://github.com/unovue.png" alt="@unovue" />
              <AvatarFallback>CN</AvatarFallback>
            </Avatar>
          </MenubarTrigger>
          <MenubarContent>
            <MenubarItem>Profile</MenubarItem>
            <MenubarSeparator />
            <MenubarItem>Settings</MenubarItem>
            <MenubarSeparator />
            <MenubarItem>Logout</MenubarItem>
          </MenubarContent>
        </MenubarMenu>
      </Menubar>
    </div>
  </div>
</template>
<script setup>
import { Avatar, AvatarFallback, AvatarImage } from '@/components/ui/avatar'
import { Menubar, MenubarContent, MenubarItem, MenubarMenu, MenubarShortcut, MenubarTrigger } from '@/components/ui/menubar'
import { Input } from '@/components/ui/input'
import { Search } from 'lucide-vue-next'
</script>
<style>
  
</style>