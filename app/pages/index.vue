<script setup lang="ts">
useSeoMeta({
    title: 'Muhammed Suhail - Portfolio',
    ogTitle: 'Muhammed Suhail - Portfolio',
    description: 'Welcome to my personal portfolio website where I showcase my skills, projects, and experiences as a developer.',
    ogDescription: 'Welcome to my personal portfolio website where I showcase my skills, projects, and experiences as a developer.',
    ogImage: '/favion.ico',
})
</script>

<template>
    <div class="lg:px-[5em] md:px-[2em] px-[1em]">
        <div class="h-[100dvh] py-[2.5em] ">
            <div class="border-[1px] border-[#34A0A4] h-[100%] rounded-[2em] ">
                <LinksNavbar />
                <HomeHeader />
            </div>
        </div>
        <div class="lg:px-[8em] md:px-[2em] px-[1em]">
            <LazyHomeAbout />
            <LazyHomeExpertise />
        </div>
    </div>
    <LazyHomeSkills />
</template>