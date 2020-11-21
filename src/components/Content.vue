<template>
    <div id="content-container">
        <div class="therapist-card" v-for="(therapist, index) in therapists" v-bind:key="index">
            {{ therapist.name }}
            {{ therapist.insurance }}
            {{ therapist.good }}
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            therapists: [
                {
                    name: "angelina",
                    insurance: "blue",
                    good: "yes"
                },
                {
                    name: "angelina",
                    insurance: "blue",
                    good: "yes"
                },
                {
                    name: "angelina",
                    insurance: "blue",
                    good: "yes"
                }
            ]
        }
    }
}
</script>

<style scoped>
#content-container {
    background-color: #a0c4ff;
}
</style>