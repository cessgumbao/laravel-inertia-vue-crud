<script setup>
import BreezeAuthenticatedLayout from "@/Layouts/Authenticated.vue";
import { Head } from "@inertiajs/inertia-vue3";
</script>

<template>
  <Head title="Categories" />

  <BreezeAuthenticatedLayout>
    <template #header>
      <h2 class="font-semibold text-xl text-gray-800 leading-tight">
				Categories
      </h2>
    </template>

    <div class="flex min-h-screen h-full">
			<div class="mx-auto sm:px-6 lg:px-8 w-full py-8">
				<div
					class="bg-white overflow-hidden shadow-sm sm:rounded-lg"
				>
					<div class="p-8 bg-white border-b border-gray-200">
						<slot />
					</div>
				</div>
			</div>
			<div class="bg-gray-200 w-96 flex flex-col space-y-4 p-2">
				
			</div>
    </div>
  </BreezeAuthenticatedLayout>
</template>
