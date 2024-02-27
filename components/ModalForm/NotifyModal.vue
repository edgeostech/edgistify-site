<template>
    <div class="modal-overlay">
        <div class="modal">
            <p>Your Inquiry is registered with us, we will get back to you shortly!</p>
            <button @click="$emit('close-notify-modal')">Close</button>
        </div>
    </div>
</template>
  
<script>
export default {}
</script>

<style lang="scss" scoped>
.modal-overlay {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    display: flex;
    justify-content: center;
    background-color: #000000da;
}

.modal {
    background-color: white;
    height: 15vh;
    width: 30vw;
    margin-top: 10%;
    border-radius: 20px;
    color: black;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    flex-direction: column;
    z-index: 99;

    @media (max-width: 800px) {

        height: 22vh;
        width: 85vw;
    }
}

button {
    background-color: #00a699;
    width: 150px;
    height: 40px;
    color: white;
    font-size: 14px;
    border-radius: 16px;
}
</style>