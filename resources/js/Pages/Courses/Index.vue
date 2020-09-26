<template>
    <app-layout>
        <template #header>
            Liste des formations
        </template>
        <div v-for="course in this.courseList" v-bind:key="course.id">
            <div>{{ course.title }}</div>
            <div>{{ course.description }}</div>
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