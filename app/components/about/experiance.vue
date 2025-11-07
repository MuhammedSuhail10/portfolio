<script setup>
import { ref } from 'vue'
import Framework, { Languages, CSSFramework, Databases, Platforms } from './skills.jsx';

const skills = Framework()
const skillsList = skills.map((skill, index) => ({
    ...skill,
    id: index
}))

const langs = Languages()
const langList = langs.map((lang, index) => ({
    ...lang,
    id: index
}))

const css = CSSFramework()
const cssList = css.map((lang, index) => ({
    ...lang,
    id: index
}))

const dbs = Databases()
const dbList = dbs.map((db, index) => ({
    ...db,
    id: index
}))

const platforms = Platforms()
const platformList = platforms.map((platform, index) => ({
    ...platform,
    id: index
}))
</script>

<template>
    <div class="my-[2em] lg:px-[13em] md:px-[2em] px-[1em] ">
        <div class='text-center font-[Poppins] md:text-[5em] text-[3em] mb-[0]'>Experiance</div>
        <div class="text-center italic mt-[-0.8em] lg:text-[1.2em] text-[1em] lg:px-[] px-[1em] ">
            "A story still unfolding."
        </div>
        <!-- <LazyHelpersWorkInfo title="Full-Stack Engineer" desc="Bagheera Carrom OPC Pvt Ltd" show-year year="April 2025 - Present" /> -->
        <LazyHelpersWorkInfo title="Associate Python Developer" desc="Emergio Games Pvt Ltd" show-year
            year="January 2024 - Present" />
        <div class="my-[3em]">
            <p class="italic lg:text-[2em] text-[1em] text-[#34A0A4] my-[1em] ">Frameworks </p>
            <div class="flex flex-wrap w-[100%] gap-[2em]  ">
                <div v-for="item in skillsList" :key="item.id">
                    <LazyHelpersBtn :text="item.name">
                        <template #icon>
                            <component :is="item.svg" />
                        </template>
                    </LazyHelpersBtn>
                </div>
            </div>
        </div>
        <div class="my-[3em]">
            <p class="italic lg:text-[2em] text-[1em] text-[#34A0A4] my-[1em] ">Languages</p>
            <div class="flex flex-wrap gap-[2em]  ">
                <div v-for="item in langList" :key="item.id">
                    <LazyHelpersBtn :text="item.name">
                        <template #icon>
                            <component :is="item.svg" />
                        </template>
                    </LazyHelpersBtn>
                </div>
            </div>
        </div>
        <div class="my-[3em]">
            <p class="italic lg:text-[2em] text-[1em] text-[#34A0A4] my-[1em] ">Databases</p>
            <div class="flex flex-wrap gap-[2em]  ">
                <div v-for="item in dbList" :key="item.id">
                    <LazyHelpersBtn :text="item.name">
                        <template #icon>
                            <component :is="item.svg" />
                        </template>
                    </LazyHelpersBtn>
                </div>
            </div>
        </div>
        <div class="my-[3em]">
            <p class="italic lg:text-[2em] text-[1em] text-[#34A0A4] my-[1em] ">Platforms</p>
            <div class="flex flex-wrap gap-[2em]  ">
                <div v-for="item in platformList" :key="item.id">
                    <LazyHelpersBtn :text="item.name">
                        <template #icon>
                            <component :is="item.svg" />
                        </template>
                    </LazyHelpersBtn>
                </div>
            </div>
        </div>
        <div class="my-[3em]">
            <p class="italic lg:text-[2em] text-[1em] text-[#34A0A4] my-[1em] ">CSS Helpers</p>
            <div class="flex flex-wrap gap-[2em]  ">
                <div v-for="item in cssList" :key="item.id">
                    <LazyHelpersBtn :text="item.name">
                        <template #icon>
                            <component :is="item.svg" />
                        </template>
                    </LazyHelpersBtn>
                </div>
            </div>
        </div>
    </div>
</template>