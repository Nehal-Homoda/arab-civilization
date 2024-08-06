<template>
    <div class="main-page">
        <div class="header">
            <!-- <div class="btn-wrapper"> -->
            <button class="rules-btn">قواعد المكافات</button>
            <!-- </div> -->

            <Timer />
        </div>
        <div class="btn-wrapper">
            <button @click="changeType('receiver')" :class="{ 'active': selectedType == 'receiver' }" class="">قائمه
                الاستلام</button>
            <button @click="changeType('senders')" :class="{ 'active': selectedType == 'senders' }">قائمه الارسال</button>

        </div>
    </div>
</template>


<script>
import Timer from '@/components/Timer.vue'
export default {
    components: {
        Timer
    },
    data: function () {

        return {
            selectedType: ''
        }
    },
    methods: {
        changeType(type) {
            this.selectedType = type

        }
    }
}


</script>



<style lang="scss" scoped>
.btn-wrapper {
    width: 100%;
    height: 20vw;
    display: flex;
    justify-content: space-between;
    margin: -60px auto;
    align-items: center;



    button {
        width: 45%;
        height: 100%;
        background: url('@/assets/imgs/uncheck-btn.png') center no-repeat;
        background-size: contain;
        border: none;
        outline: none;
        padding-top: 20px;
        color: rgb(250, 217, 150);
        &.active{
            background: url('@/assets/imgs/check-btn.png') center no-repeat;
            background-size: contain;
        }

    }

}

.header {
    width: 100%;
    height: 144vw;
    background: url('@/assets/imgs/header-bg.png') no-repeat;
    background-size: cover;
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 15px;
    align-items: center;
    padding-top: 370px;

    .rules-btn {
        width: 60vw;
        height: 14vw;
        background: url('@/assets/imgs/rules-bg.png') no-repeat;
        background-size: contain;
        border: none;
        outline: none;
        color: rgb(250, 217, 150);
        font-weight: bold;
    }

}
</style>