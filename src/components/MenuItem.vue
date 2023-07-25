<script setup>
const props = defineProps(['data'])
let access = props.data
</script>

<template>
  <div class="flex gap-2 mt-8">
    <router-link to="/manage-leads" class="bg-gray-100 p-2 rounded flex gap-2">
      <span>Manage Leads</span>
      <div v-if="access.includes('manage.leads')">✅</div>
      <div v-else>❌</div>
    </router-link>
    <router-link to="/campaign-management" class="bg-gray-100 p-2 rounded flex gap-2">
      <span>Campaign Management</span>
      <div v-if="access.includes('campaign.management')">✅</div>
      <div v-else>❌</div>
    </router-link>
    <router-link to="/analytics-reports" class="bg-gray-100 p-2 rounded flex gap-2">
      <span>Analytics and Reports</span>
      <div v-if="access.includes('analytics.reports')">✅</div>
      <div v-else>❌</div>
    </router-link>
    <router-link to="/user-management" class="bg-gray-100 p-2 rounded flex gap-2">
      <span>User Management</span>
      <div v-if="access.includes('user.management')">✅</div>
      <div v-else>❌</div>
    </router-link>
  </div>
</template>