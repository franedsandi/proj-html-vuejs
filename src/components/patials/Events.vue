<script>
export default {

}
</script>

<template>
  <div class="container">
    <div class="card">
      <img src="img/Nisi-ut-aliquid-ex-ea-com-1400x878_t.jpg" alt="play">
      <div class="data-coments">
        <div class="data">
          <i class="fa-regular fa-calendar-days"></i>
          <span>Jan 18, 2021</span>
        </div>
        <div class="coments">
          <i class="fa-regular fa-comments"></i>
          <span>0 coments</span>
        </div>
      </div>
      <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Iste, inventore.</p>
    </div>
    <div class="card">
      <img src="img/Illo-inventore-veritatis-quasi-1400x878_t.jpg" alt="controller">
      <div class="data-coments">
        <div class="data">
          <i class="fa-regular fa-calendar-days"></i>
          <span>May 30, 2021</span>
        </div>
        <div class="coments">
          <i class="fa-regular fa-comments"></i>
          <span>0 coments</span>
        </div>
      </div>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Blanditiis commodi neque eaque! Quasi.</p>
    </div>
    <div class="card">
      <img src="img/Consequunt-magni-dolores-1400x878_t.jpg" alt="ocullus">
      <div class="data-coments">
        <div class="data">
          <i class="fa-regular fa-calendar-days"></i>
          <span>Apr 13, 2021</span>
        </div>
        <div class="coments">
          <i class="fa-regular fa-comments"></i>
          <span>0 coments</span>
        </div>
      </div>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Incidunt, dolor impedit atque repellat ut similique?</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '../../scss/partials/vars';
.container{
  display: flex;
  justify-content: space-between;
  margin-top: 40px;

  flex-wrap: wrap;
  .card{
    width: calc(100% / 3 - 15px);
    border-radius: 0;
    border: none;
    background: none;
    color: white;
    font-size: 13px;
    margin-bottom: 70px;
    &:hover{
      cursor: pointer;
    }
    .data-coments{
      padding: 15px 0px;
      display: flex;
      gap: 20px;
      i{
        margin-right: 7px;
        color: $yellow-color;
      }
    }
    
  }&::after{
      content: '';
      width: 100%;
      height: 1px;
      background-color: $yellow-color;
    }
}
</style>