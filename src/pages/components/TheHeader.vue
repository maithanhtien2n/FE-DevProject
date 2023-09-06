<script setup>
import { ref } from "vue";

const visibleLeft = ref(false);

const items = [
  {
    label: "File",
    icon: "pi pi-fw pi-file",
    items: [
      {
        label: "New",
        icon: "pi pi-fw pi-plus",
        items: [
          {
            label: "Bookmark",
            icon: "pi pi-fw pi-bookmark",
          },
          {
            label: "Video",
            icon: "pi pi-fw pi-video",
          },
        ],
      },
    ],
  },
];
</script>

<template>
  <Sidebar v-model:visible="visibleLeft"> <PanelMenu :model="items" /></Sidebar>

  <div class="the-header flex align-items-center px-5">
    <Button
      icon="pi pi-bars"
      class="p-button-rounded p-button-outlined p-button-text"
      @click="visibleLeft = true"
    />
  </div>
</template>

<style>
.the-header {
  height: 4.3rem;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 1px 3px 0px,
    rgba(0, 0, 0, 0.06) 0px 1px 2px 0px;
}

.p-button.p-button-icon-only.p-button-rounded {
  height: 2.3rem !important;
}
.p-button.p-button-icon-only {
  width: 2.3rem !important;
}

.pi {
  font-size: 1.2rem !important;
  color: rgb(110, 110, 110) !important;
}
</style>
