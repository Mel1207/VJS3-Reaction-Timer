<template>
    <div>
        <h2>Reaction Time: {{ score }}ms</h2>
        <h3 class="rank">{{ rank }}</h3>
    </div>
</template>

<script>
export default {
    props: [ 'score' ],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if(this.score < 250) {
            this.rank = 'Star reflexes 😍'
        } else if (this.score < 400) {
            this.rank = 'Rapid reflexes 😎'
        } else {
            this.rank = 'Needs more pracice 😁'
        }
    }
}
</script>