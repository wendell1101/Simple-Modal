<template>
    <div class="backdrop" @click.self="closeModal">
        
        <div class="modal">
            <h1>{{ header }}</h1>
            <p>{{ text }}</p>
        </div>
    </div>
</template>

<script>
export default {
    props: ['header','text', 'theme'],
    methods : {
        closeModal (){
            this.$emit('close')
        }
    }
}
</script>

<style>
    .modal{
        width: 400px;
        padding: 20px;
        margin: 100px auto;
        background: white;
        border-radius: 10px;
    }
    .backdrop {
        top:0;
        position: fixed;
        background: rgba(0,0,0,0.5);
        width: 100%;
        height: 100%;
    }
    .modal h1{
        color:rgb(92, 92, 93);
    }
    .modal p{
        font-style: normal;
    }
    .sale{
        background:crimson;
        color: #fff;
    }
    .sale h1{
        color: #fff;
    }
</style>



