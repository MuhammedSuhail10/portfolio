<script setup>
import { ref } from 'vue'
import SkillsData from './skillData'

const skills = SkillsData()

const SkillMapping = () => {
    return skills.map((skill, index) => ({
        skill,
        key: index
    }))
}

const skillsList = SkillMapping()
</script>

<template>
    <section class="md:mt-[5em] mb-[2em] md:mb-[5em] overflow-hidden">
        <div class="flex overflow-hidden">
            <div class="flex scroll-line">
                <div v-for="item in skillsList" :key="item.key" class="px-[1em]">
                    <div class="bg-[#1e1e1e] hover:bg-[#34A0A4] transition duration-400 cursor-pointer md:py-[0.3em] md:px-[2em] py-[0.3em] px-[1.5em] text-[1.5em] rounded-full">
                        <p class="whitespace-nowrap">{{ item.skill }}</p>
                    </div>
                </div>
            </div>
            <div class="flex scroll-line">
                <div v-for="item in skillsList" :key="item.key" class="px-[1em]">
                    <div class="bg-[#1e1e1e] hover:bg-[#34A0A4] transition duration-400 cursor-pointer md:py-[0.3em] md:px-[2em] py-[0.3em] px-[1.5em] text-[1.5em] rounded-full">
                        <p class="whitespace-nowrap">{{ item.skill }}</p>
                    </div>
                </div>
            </div>
        </div>

        <div class="flex mt-[2em] overflow-hidden">
            <div class="flex scroll-line-rev">
                <div v-for="item in skillsList" :key="`rev-${item.key}`" class="px-[1em]">
                    <div class="bg-[#1e1e1e] hover:bg-[#34A0A4] transition duration-400 cursor-pointer md:py-[0.3em] md:px-[2em] py-[0.3em] px-[1.5em] text-[1.5em] rounded-full">
                        <p class="whitespace-nowrap">{{ item.skill }}</p>
                    </div>
                </div>
            </div>
            <div class="flex scroll-line-rev">
                <div v-for="item in skillsList" :key="`rev-second-${item.key}`" class="px-[1em]">
                    <div class="bg-[#1e1e1e] hover:bg-[#34A0A4] transition duration-400 cursor-pointer md:py-[0.3em] md:px-[2em] py-[0.3em] px-[1.5em] text-[1.5em] rounded-full">
                        <p class="whitespace-nowrap">{{ item.skill }}</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
.scroll-line {
    animation: scroll 30s linear infinite;
}

.scroll-line-rev {
    animation: scroll 30s linear infinite reverse;
}

@keyframes scroll {
    from {
        transform: translateX(0);
    }

    to {
        transform: translateX(-100%);
    }
}
</style>