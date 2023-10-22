<script>
export default {
  data() {
    return {
      events: [
        {
          title: 'Event 1',
          image: 'img/Nisi-ut-aliquid-ex-ea-com-1400x878_t.jpg',
          date: 'Jan 18, 2021',
          comments: 0,
          description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Iste, inventore.',
        },
        {
          title: 'Event 2',
          image: 'img/Illo-inventore-veritatis-quasi-1400x878_t.jpg',
          date: 'May 30, 2021',
          comments: 0,
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Blanditiis commodi neque eaque! Quasi.',
        },
        {
          title: 'Event 3',
          image: 'img/Consequunt-magni-dolores-1400x878_t.jpg',
          date: 'Apr 13, 2021',
          comments: 0,
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Incidunt, dolor impedit atque repellat ut similique?',
        }
      ],
    };
  },
};
</script>

<template>
  <div class="container">
    <div v-for="(event, index) in events" :key="index" class="card">
      <img :src="event.image" :alt="event.title">
      <div class="data-coments">
        <div class="data">
          <i class="fa-regular fa-calendar-days"></i>
          <span>{{ event.date }}</span>
        </div>
        <div class="coments">
          <i class="fa-regular fa-comments"></i>
          <span>{{ event.comments }} comments</span>
        </div>
      </div>
      <p>{{ event.description }}</p>
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