<template>
  <div>
    <HeaderBanner
      header-img="/img/header/project-list/header-project-list.jpeg"
    />
    <div class="container mx-auto px-4">
      <ProjectListHeading />
      <ProjectList />
    </div>
  </div>
</template>

<script>
import HeaderBanner from '@/components/HeaderBanner.vue'
import ProjectListHeading from '@/components/ProjectList/ProjectListHeading.vue'
import ProjectList from '@/components/ProjectList/ProjectList.vue'
export default {
  components: {
    HeaderBanner,
    ProjectListHeading,
    ProjectList,
  },
}
</script>
