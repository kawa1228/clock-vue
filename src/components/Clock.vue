<template>
    <div>
        <div class="container">
            <p class="date">{{ year }}/{{ month }}/{{ day }}</p>
            <div class="time">
                <p class="time-item">{{ hours }} : {{ minutes }} : {{ seconds }}</p>
            </div>
        </div>
    </div>
</template>


<script>
export default {
    data() {
        return {
            date: new Date(),
        }
    },
    computed: {
        year() {
            return this.date.getFullYear()
        },
        month() {
            return this.date.getMonth() + 1
       },
        day() {
            return this.date.getDate()
       },
        hours() {
            return this.date.getHours()
       },
        minutes() {
            return this.date.getMinutes()
       },
        seconds() {
            return this.date.getSeconds()
       },
    },
    mounted() {
        this.setDate()
        setInterval(() => this.setDate(), 1000)
    },
    methods: {
        setDate() {
            this.date = new Date()
        },
    },
}
</script>

<style scoped>
.container {
    padding: 2%;
    background-color: #f0f8ff;
    color: gray;
}
.date {
    text-align: right;
    font-size: 1.5rem;
}
.time-item {
    text-align: center;
    font-size: 3rem;
}
</style>

