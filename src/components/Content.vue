<template>
    <div id="content-container">
        <div class="therapist-card col-xl-6 col-lg-9 col-md-12" v-for="(therapist, index) in therapists" v-bind:key="index">
            <img :src="therapist.imgLink" alt="therapist picture" class="propic" />
            <div class="therapist-info"> 
                <p>Name: {{therapist.name}}</p>
                <p>Valid Insurance: {{therapist.insurance}}</p>
                <p>Accepting appointments?: {{therapist.good}}</p>
            </div>
        </div>
    </div>
</template>

<script>
import superagent from 'superagent';

export default {
    data() {
        return {
            therapists: []
        }
    },
    async mounted() {
        let response = await superagent.get("http://localhost:3000/getTherapists");
        this.therapists = response.body;
        console.log(response);
    }
}
</script>

<style scoped>
#content-container {
    background-color: #f3efef;
    text-align:center;
}

.therapist-card {
    background-color: white;
    margin: 20px auto;
    display:flex;
}

.propic {
    margin-top:.5rem;
    width:100px;
    height: 100px;
    object-fit:cover;
    border-radius:50%;
}

.therapist-info {
    text-align:left;
    margin-left:30px;
}

.therapist-info p {
    margin-bottom: .5rem;
}

</style>