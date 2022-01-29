<template>
    <div class="block" v-if="showBlock">
        click me
    </div>
</template>

<script>
export default {
    props: ['delay'],
    data() {
        return {
            showBlock: false
        }
    },
    mounted() {
        // console.log('component mounted inside')
        setTimeout(() => {
            this.showBlock = true
            // console.log(this.delay)
        }, this.delay)
    },
}
</script>