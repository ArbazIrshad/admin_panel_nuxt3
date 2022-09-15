<script lang="ts" setup></script>

<template>
  <div>
    <div class="drawer drawer-mobile">
      <input id="my-drawer-2" type="checkbox" class="drawer-toggle" />
      <div class="drawer-content flex flex-col items-center justify-center">
        <!-- Page content here -->
        <p class="text-6xl">This is the content of the drawer</p>
        <label for="my-drawer-2" class="btn btn-primary drawer-button lg:hidden">Open drawer</label>

      </div>
      <div class="drawer-side">
        <label for="my-drawer-2" class="drawer-overlay"></label>
        <aside class="bg-base-200 w-80">

          <ul class="menu p-4 overflow-y-auto  text-base-content">
            <!-- Sidebar content here -->
            <li><a>Sidebar Item 1</a></li>
            <li><a>Sidebar Item 2</a></li>
          </ul>
        </aside>

      </div>
    </div>
  </div>
</template>

<style scoped>

</style>
