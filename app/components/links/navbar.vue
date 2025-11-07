<script setup>
import { computed, ref } from 'vue';
const route = useRoute()
const isHome = computed(() => route.path === '/')
const isAbout = computed(() => route.path === '/about')
const isMenuOpen = ref(false);
watch(
    () => route.path,
    () => {
        isMenuOpen.value = false
    }
)
</script>

<template>
    <div class="text-[15pt] flex justify-between items-center"
        :class="isHome && 'lg:px-[5em] px-[1em] lg:mt-[1em] h-[4em] ', !isHome && 'lg:h-[6em] h-[4em] lg:px-[10em] md:px-[2em] px-[1em]', isAbout && 'text-[#1e1e1e] bg-[#F0F8FF]'">
        <NuxtLink class="font-[600] hover:text-[#34A0A4]" active-class="text-[#34A0A4] font-[800]" exact to="/">
            Muhammed Suhail
        </NuxtLink>
        <div class="lg:hidden flex items-center">
            <button class="hover:fill-[#34A0A4]" @click="isMenuOpen = true" aria-label="Open menu">
                <svg xmlns="http://www.w3.org/2000/svg"  viewBox="0 -960 960 960" height="25px" width="25px"
                    fill="currentcolor">
                    <path d="M120-240v-80h720v80H120Zm0-200v-80h720v80H120Zm0-200v-80h720v80H120Z" />
                </svg>
            </button>
        </div>
        <div class="lg:flex gap-10 hidden">
            <NuxtLink to="/about" active-class="text-[#34A0A4] font-[800]" exact>About</NuxtLink>
            <NuxtLink to="/work" active-class="text-[#34A0A4] font-[800]" exact>Work</NuxtLink>
            <NuxtLink to="/contact" active-class="text-[#34A0A4] font-[800]" exact>Contact</NuxtLink>
        </div>
        <ClientOnly>
            <HelpersDrawer v-if="isMenuOpen" :class="isAbout ? 'bg-[#F0F8FF]' : 'bg-[#0f0f0f]'" :is-menu-open="isMenuOpen" @close="isMenuOpen = false" />
        </ClientOnly>
    </div>
</template>