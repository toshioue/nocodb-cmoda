<script lang="ts" setup>
const isBaseListModalOpen = ref(false)
</script>

<template>
  <div class="nc-mini-sidebar-btn-full-width">
    <div
      data-testid="nc-workspace-menu"
      class="nc-workspace-menu nc-mini-sidebar-ws-item nc-small-shadow"
      @click="isBaseListModalOpen = true"
    >
      <GeneralWorkspaceIcon
        :workspace="{
          id: 'nc',
          meta: {},
        }"
        show-nocodb-icon
        class="flex-none border-1 border-nc-border-gray-medium"
        size="mini-sidebar"
      />
    </div>
  </div>

  <WorkspaceBaseListModal v-model:visible="isBaseListModalOpen" />
<!-- </template>

  <div class="flex flex-row flex-grow pl-0.5 pr-1 py-0.5 rounded-md w-full" style="max-width: calc(100% - 2.5rem)">
    <div class="flex-grow min-w-20">
      <div
        data-testid="nc-workspace-menu"
        class="flex items-center nc-workspace-menu overflow-hidden py-1.25 pr-0.25 justify-center w-full ml-2"
      >
        <a
          class="transition-all duration-200 transform w-24 min-w-10" 
          href="#"
          target="_blank"
          rel="noopener noreferrer"
        >
          <NcTooltip :disabled="!appInfo?.version || isEeUI">
            <template #title>{{ appInfo?.version }}</template>
            <img alt="NocoDB" src="~/assets/img/brand/nocodb.png" />
          </NcTooltip>
        </a>
        <div class="flex flex-grow"></div>
      </div> -->