<template>
    <app-layout>
        <template #header>
            Liste des formations
        </template>
        <div class="py-6" v-for="course in this.courseList" v-bind:key="course.id">
            <div class="mx-8 bg-white rounded shadow p-3">
                <div class="flex justify-between items-center">
                    <div class="text-4xl">{{ course.title }}</div>
                    <div class="text-sm text-gray-400">25 épisodes</div>
                </div>
                <div class="text-sm text-gray-500">{{ course.description }}</div>
                <a href="#" class="bg-indigo-500 text-white px-2 py-1 text-sm mt-3 rounded hover:bg-indigo-700 inline-block">Voir la formation</a>
            </div>
        </div>
    </app-layout>
</template>

<script>
    import AppLayout from './../../Layouts/AppLayout';

export default {
    components: {
        AppLayout
    },

    data() {
        return {
            courseList: this.courses
        }
    },
    
    props: ['courses'],

    mounted(){
        console.log(this.courseList);
    }
}
</script>