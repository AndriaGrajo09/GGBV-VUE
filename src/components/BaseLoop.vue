<template>
    <div>
        <div v-for= "(course, index) in courses" :key="index" >
        {{course}}
        </div>
        <button @click= "addCourse">Add Course</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            courses: ['IT', 'IS', 'CS', 'BSA', 'BPA'],
        };
    },
    methods: {
        addCourse() {
            const newCourse = prompt('Enter a new course: ');
            if (newCourse) {
                this.courses.push(newCourse);
            }
        },
    },
};
</script>