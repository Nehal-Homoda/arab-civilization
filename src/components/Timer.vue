<template>
    <div class="timer-wrapper">
        
        <div class="date-item">
            <span>ثانيه</span>
            <div class="date-bg" >
           <span></span>
          </div>
        </div>

        <div class="date-item">
            <span>دقيقه</span>
            <div class="date-bg" >
           <span></span>
          </div>

          <div class="date-item">
              <span>ساعه</span>
              <div class="date-bg" >
             <span></span>
            </div>
  
          </div>
        </div>
        <div class="date-item">
            <span>يوم</span>
          <div class="date-bg" >
           <span></span>
          </div>

        </div>
        <span>وقت الحدث</span>

    </div>
</template>


<script>


</script>


<style lang="scss" scoped>
.timer-wrapper{
    display: flex;
    color: white;
    align-items: center;
     gap: 8px;
    
   
    .date-item{
        display: flex;
        align-items: center;
        gap: 5px;
       
        
        
        .date-bg{
            width: 7vw;
            height: 7vw;
            background: url('@/assets/imgs/timer-bg.png')  center no-repeat;
            background-size: contain; 

        }
    }
}

</style>