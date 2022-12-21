<script setup>
  import ProfileCard from './components/profileCard.vue'
  import ProfileCardSkeleton from './components/profileCardSkeleton.vue'
</script>

<template>
  <Suspense>
    <template #default >
      <ProfileCard />
    </template>
    <template #fallback>
      <ProfileCardSkeleton />
    </template>
  </Suspense>
</template>

<style scoped>

</style>
