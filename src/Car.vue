<template>
    <div>
        <h3>
           Name : {{ carName }}
        </h3>
        <p>Year : {{ carYear }}</p>
        <button @click="changeName">Change Name</button>
        <button @click="updateCounter">Update counter</button>
    </div>

</template>

<script>
    export default {
        name: "Car",
        props: ['carName', 'carYear', 'counter'],
        methods: {
            changeName: function() {
                this.carName = "Mazda";
                this.$emit('nameChanged', this.carName);
            },
            updateCounter: function() {
                this.$emit('counterUpdated', this.counter++);
            }
        }
    }
</script>

<style scoped>

</style>
