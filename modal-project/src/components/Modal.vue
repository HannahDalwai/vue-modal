<template>
    <div class="backdrop" @click="closeModal">
        <div class="modal">
            <h1>Title of said modal</h1>
            <p>Modal content</p>
        </div>
    </div>
</template>


<script>
export default {
    methods: {
        closeModal(){
            this.$emit('close')
        }
    },
}
</script>


<style scoped>
    .modal{
        width: 400px;
        padding: 20px;
        margin: 100px auto;
        background: white;
        border-radius: 10px;
        }
        .backdrop{
            top: 0;
            position: fixed;
            background: rgb(0, 0, 0,0.5);
            width: 100%;
            height: 100%;
        }
         h1{
            color: blueviolet;
            border: none;
                        border-bottom: 1px solid rgb(191, 89, 250);

        }
</style>