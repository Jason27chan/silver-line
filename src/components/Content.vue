<template>
    <div id="content-container">
        <div class="therapist-card" v-for="(therapist, index) in therapists" v-bind:key="index">
            <img :src="therapist.imgLink" alt="therapist picture" class="propic" />
            <div> 
                <p>Name: {{therapist.name}}</p>
                <p>Valid Insurance: {{therapist.insurance}}</p>
                <p>Accepting appointments?: {{therapist.good}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            therapists: [
                {
                    name: "Drew",
                    insurance: "blue shield",
                    good: "yes",
                    imgLink: "http://www.newdesignfile.com/postpic/2013/07/shutterstock-stock-photography_376128.jpg"
                },
                {
                    name: "Angelina",
                    insurance: "green shield",
                    good: "yes",
                    imgLink: "http://www.newdesignfile.com/postpic/2013/07/free-stock-photos-people_376135.jpg"
                },
                {
                    name: "Frank",
                    insurance: "purple shield",
                    good: "yes",
                    imgLink: "https://101clipart.com/wp-content/uploads/02/Reading%20Child%20Clipart%2002.gif"
                }
            ]
        }
    }
}
</script>

<style scoped>
#content-container {
    background-color: #f1fafd;
    text-align:center;
}

.therapist-card {
    margin-top: 20px;
}

.propic {
    max-width:100px;
}
</style>