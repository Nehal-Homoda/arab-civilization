<template>
  <div class="rank-box-wrap">
    <div class="rank-item" v-for="(item, index) in 3" :key="index">
      <div class="top-img">
        <img src="@/assets/imgs/avatar.jpg" alt="" />
        <img
          class="img-frame"
          v-if="index == 0"
          src="@/assets/imgs/top_frame_1.png"
          alt=""
        />
        <img
          class="item-frame"
          v-if="index == 0"
          src="@/assets/imgs/top1-bg.png"
          alt=""
        />
        <img
          class="img-frame"
          v-if="index == 1"
          src="@/assets/imgs/top_frame_2.png"
          alt=""
        />
        <img
          class="item-frame"
          v-if="index == 1"
          src="@/assets/imgs/top2-bg.png"
          alt=""
        />
        <img
          class="img-frame"
          v-if="index == 2"
          src="@/assets/imgs/top_frame_3.png"
          alt=""
        />
        <img
          class="item-frame"
          v-if="index == 2"
          src="@/assets/imgs/top3-bg.png"
          alt=""
        />
      </div>
      <span>refref</span>
      <span>rferf</span>
      <span>frerfer</span>
    </div>
  </div>
</template>



<script>
</script>



<style scoped lang="scss">
.rank-box-wrap {
  display: flex;
  padding: 40% 5% 5% 5%;
  gap: 5%;
  .rank-item {
    width: 30%;
    display: flex;
    flex-direction: column;
    align-items: center;
    color: white;
    .top-img {
      width: 15vw;
      height: 15vw;
      position: relative;
      img {
        width: 100%;
        height: 100%;
        border-radius: 50%;
        object-fit: cover;
        z-index: 999;
       
      }
      .img-frame {
        width: 130%;
        height: 146%;
        position: absolute;
        left: 50%;
        top: 39%;
        transform: translate(-50%, -50%);
        z-index: 2;
        
      }
      .item-frame{
        width: 130%;
        height: 146%;
        position: absolute;
        left: 50%;
        top: 39%;
        transform: translate(-50%, -50%);
        z-index: 1;
      }
    }
  }
}
</style>






