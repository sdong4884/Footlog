<template>
  <div id="fl-list">
    <v-app>
      <v-container>
        <v-card>
          <v-carousel 
            :show-arrows="false"
            :height="200"
          >
            <v-carousel-item
              v-for="(image, i) in images"
              :key="i"
              :src="image.src"
            ></v-carousel-item>
          </v-carousel>
          <div class="fl-card-text">
            <div class="fl-info">
              <span>
                <v-icon>mdi-map-marker</v-icon>
                마포구 서교동
              </span>
              <span>22.03.14</span>
            </div>
            <div class="fl-tit">해피 화이트데이</div>
            <ul class="fl-tags">
              <li>#기념일</li>
              <li>#화이트데이</li>
              <li>#맛집</li>
              <li>#합정</li>
            </ul>
          </div>
        </v-card>
      </v-container>
    </v-app>
  </div>
</template>

<script>
export default {
  name: 'List',
  data() {
    return {
      images: [
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
        },
      ],
    }
  }
}
</script>

<style lang="scss">
.fl-card-text {
  padding: 16px;
  .fl-info {
    display: flex;
    justify-content: space-between;
    font-size: 12px;
    .v-icon {
      font-size: 16px;
    }
  }
  .fl-tit {
    margin-top: 4px;
    font-size: 16px;
    font-weight: 700;
  }
  .fl-tags {
    margin-top: 4px;
    list-style: none;
    padding-left: 0;
    display: flex;
    font-size: 12px;
    color: rgba(0,0,0,.6);
    li + li {
      margin-left: 4px;
    }
  }
}
</style>