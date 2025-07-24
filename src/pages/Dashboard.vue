<template>
  <h1 class="text-3xl font-semibold mb-4">Dashboard</h1>
  <div class="flex gap-4 mb-4">
    <Card class="flex-1">
      <CardContent>
        <div class="flex items-center justify-between">
          <p>Total Revenue</p>
          <DollarSign class="size-5" />
        </div>
        <p class="font-bold text-2xl my-2">$32,356.76</p>
        <p class="text-sm text-gray-400">+20.1% from last month</p>
      </CardContent>
    </Card>
    <Card class="flex-1">
      <CardContent>
        <div class="flex items-center justify-between">
          <p>Subscription</p>
          <Users class="size-5" />
        </div>
        <p class="font-bold text-2xl my-2">+1840</p>
        <p class="text-sm text-gray-400">+130% from last month</p>
      </CardContent>
    </Card>
    <Card class="flex-1">
      <CardContent>
        <div class="flex items-center justify-between">
          <p>Sales</p>
          <WalletMinimal class="size-5" />
        </div>
        <p class="font-bold text-2xl my-2">+9521</p>
        <p class="text-sm text-gray-400">+19% from last month</p>
      </CardContent>
    </Card>
    <Card class="flex-1">
      <CardContent>
        <div class="flex items-center justify-between">
          <p>Active Now</p>
          <ChartNoAxesColumnIncreasing class="size-5" />
        </div>
        <p class="font-bold text-2xl my-2">+489</p>
        <p class="text-sm text-gray-400">+261 from last month</p>
      </CardContent>
    </Card>
  </div>
  <div>
    <Card>
      <CardContent>
        <div class="flex items-center justify-between mb-4">
          <h3 class="text-2xl font-semibold">Users table</h3>
          <Button>
            <Plus/> New User
          </Button>
        </div>
        <div>
          <Table>
            <TableCaption>A list of users.</TableCaption>
            <TableHeader>
              <TableRow>
                <TableHead>
                  Name
                </TableHead>
                <TableHead>First Name</TableHead>
                <TableHead>Email</TableHead>
                <TableHead>Address</TableHead>
                <TableHead >Birth Date</TableHead>
                <TableHead>Gender</TableHead>
                <TableHead>Actions</TableHead>
              </TableRow>
            </TableHeader>
            <TableBody>
              <TableRow v-for="user in users" :key="user.email">
                <TableCell>{{ user.lastName }}</TableCell>
                <TableCell>{{ user.firstName }}</TableCell>
                <TableCell>{{ user.email }}</TableCell>
                <TableCell>{{ user.address }}</TableCell>
                <TableCell>{{ user.birthDate }}</TableCell>
                <TableCell>{{ user.gender }}</TableCell>
                <TableCell>
                  <Button size="sm">
                    <Pencil />
                  </Button>
                  <Button size="sm" variant="outline" class="ml-2">
                    <Trash />
                  </Button>
                </TableCell>
              </TableRow>
            </TableBody>
          </Table>
        </div>
      </CardContent>
    </Card>
  </div>
</template>
<script setup>
import { Card, CardHeader, CardTitle, CardDescription, CardContent, CardFooter } from '@/components/ui/card'
import { Button } from '@/components/ui/button'
import { Table, TableBody, TableCaption, TableCell, TableHead, TableHeader, TableRow } from '@/components/ui/table'
import { DollarSign, Users, WalletMinimal, ChartNoAxesColumnIncreasing, Plus, Pencil, Trash } from 'lucide-vue-next'

const users = [
  {
    "lastName": "Dupont",
    "firstName": "Marie",
    "email": "marie.dupont@email.com",
    "address": "12 Rue des Lilas, 75010 Paris",
    "gender": "Female",
    "birthDate": "1990-05-14"
  },
  {
    "lastName": "Martin",
    "firstName": "Julien",
    "email": "julien.martin@email.com",
    "address": "45 Avenue de Lyon, 69003 Lyon",
    "gender": "Male",
    "birthDate": "1988-11-23"
  },
  {
    "lastName": "Lefevre",
    "firstName": "Clara",
    "email": "clara.lefevre@email.com",
    "address": "8 Boulevard Gambetta, 06000 Nice",
    "gender": "Female",
    "birthDate": "1995-02-03"
  },
  {
    "lastName": "Moreau",
    "firstName": "Thomas",
    "email": "thomas.moreau@email.com",
    "address": "27 Rue Alsace, 67000 Strasbourg",
    "gender": "Male",
    "birthDate": "1992-08-17"
  },
  {
    "lastName": "Bernard",
    "firstName": "Sophie",
    "email": "sophie.bernard@email.com",
    "address": "34 Rue du Château, 33000 Bordeaux",
    "gender": "Female",
    "birthDate": "1985-12-01"
  }
]


</script>
<style>
  
</style>