<template>
<div class="popup">
  <button @click="openModal">Open</button>
  <div v-if="modalActive" class="modal">
    <div class="modal-content">
        <p>{{this.modalMessage}}</p>
        <button class="btn_popup" @click="closeModal">Close</button>
    </div>
  </div>
</div>
</template>

<script>
export default {
    data() {
        return {
            modalActive: null,
            modalMessage: 'Content popup',
        }
    },
    methods: {
        openModal() {
            this.modalActive = !this.modalActive;
        },     
         closeModal() {
            this.modalActive = !this.modalActive;
        },
    },
}
</script>

<style>
.modal{
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 101;
    width: 100%;
    position: absolute;
    text-align: center;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba(0, 0, 0, 0.3);
}
.modal-content{
    display: flex;
    flex-direction: column;
    justify-content: center;
    border-radius: 8px;
    width: 300px;
    padding: 40px 30px;
    background-color:#fff;
    color: #121212;
}


.btn_popup{
    align-self: center;
}
</style>