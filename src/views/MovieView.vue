<template>
  <h1>MOVIES HEREE</h1>
  <div class="home">
    <div class="feature-card">
      <router-link class="diff" to="/movie/goku">
        <img
          src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTJC5p9LOKNQ1_iqkjCrcj2tcU-7b6MIXWGFKloNQoT4_P6KWT4rcq8BcuS8QPgLY2VSLk&usqp=CAU"
          alt="SSG best"
          class="featured-img"
        />
        <div class="details">
          <h3>Dragon Ball Z</h3>
          <p>
            Goku, from planet Earth tries to save the Universe from the bad
            Supersaiyans that invaded Earth's planetary System
          </p>
        </div>
      </router-link>
      <router-link class="diff" to="/movie/naruto">
        <img
          src="https://cdn.givemesport.com/wp-content/uploads/2022/06/FortnitexNaruto-.jpg"
          alt="naruto best"
          class="featured-img"
        />
        <div class="details">
            <h3>Dragon Ball Z</h3>
          <p>
            Goku, from planet Earth tries to save the Universe from the bad
            Supersaiyans that invaded Earth's planetary System
          </p>
        </div>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.diff {
  margin: 5px;
}
.home {
  .feature-card {
    position: relative;
    .featured-img {
      display: block;
      width: 100%;
      height: 300px;
      object-fit: cover;
      position: relative;
      z-index: 0;
    }
  }
}
.details {
      position: relative;
      left: 0;
      right: 0;
      bottom: 0;
      background-color: rgba(132, 52, 52, 0.6);
      padding: 16px;
      z-index: 1;

      h3 {
        color: #fff;
        margin-bottom: 16px;
      }

      p {
        color: #fff;
      }
    }
</style>
