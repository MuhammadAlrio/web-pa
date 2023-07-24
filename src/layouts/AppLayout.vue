<script setup>
import { markRaw, ref, watch } from "vue";
import { useRoute } from "vue-router";
import DashboardLayout from "./themes/DashboardLayout.vue";
import EmptyLayout from "./themes/EmptyLayout.vue";

const layout = ref();
const route = useRoute();

watch(
	() => route.meta.layout,
	async (meta) => {

		switch (meta) {
			case "DashboardLayout":
                console.log(meta);
				layout.value = markRaw(DashboardLayout);
				break;
            default:
                layout.value = markRaw(EmptyLayout);
				break;
		}

	},
	{ immediate: true }
);
</script>

<template>
	<component :is="layout"> <router-view /> </component>
</template>