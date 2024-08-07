<template>
  <div class="main-page">
    <div class="header">
      <button class="rules-btn">قواعد المكافات</button>

      <Timer />
    </div>
    <div class="btn-wrapper">
      <button
        @click="changeType('receiver')"
        :class="{ active: selectedType == 'receiver' }"
        class=""
      >
        قائمه الاستلام
      </button>
      <button
        @click="changeType('senders')"
        :class="{ active: selectedType == 'senders' }"
      >
        قائمه الارسال
      </button>
    </div>
    <div class="rank-wrapper">
      <RankingBox />
      <RankingName />
    </div>
  </div>
</template>


<script>
import Timer from "@/components/Timer.vue";
import RankingBox from "./RankingBox.vue";
import RankingName from "./RankingName.vue";
export default {
  components: {
    Timer,
    RankingBox,
    RankingName,
  },
  data: function () {
    return {
      selectedType: "",
    };
  },
  methods: {
    changeType(type) {
      this.selectedType = type;
    },
  },
};
</script>



<style lang="scss" scoped>
.rank-wrapper {
  width: 90%;
  min-height: 104vw;
  background: url("@/assets/imgs/rank-bg.png") center no-repeat;
  background-size: contain;
  margin: 60px auto;
  position: relative;
  &::before {
    width: 105%;
    height: 44vw;
    background: url("@/assets/imgs/rank-before-bg.png") center no-repeat;
    background-size: contain;
    position: absolute;
    top: -10px;
    left: -10px;
    content: "";
  }
  &::after {
    content: "";
    width: 104%;
    height: 34vw;
    background: url("@/assets/imgs/rank-after-bg.png") center no-repeat;
    background-size: contain;
    position: absolute;
    bottom: -10px;
    left: -9px;
  }
}
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
    background: url("@/assets/imgs/uncheck-btn.png") center no-repeat;
    background-size: contain;
    border: none;
    outline: none;
    padding-top: 20px;
    color: rgb(250, 217, 150);
    &.active {
      background: url("@/assets/imgs/check-btn.png") center no-repeat;
      background-size: contain;
    }
  }
}

.header {
  width: 100%;
  height: 144vw;
  background: url("@/assets/imgs/header-bg.png") no-repeat center;
  background-size: contain;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-top: 370px;

  .rules-btn {
    width: 50%;
    height: 18vw;
    background: url("@/assets/imgs/rules-bg.png") no-repeat center;
    background-size: contain;
    border: none;
    outline: none;
    color: rgb(250, 217, 150);
    font-weight: bold;
    font-size: 15px;
  }
}
</style>