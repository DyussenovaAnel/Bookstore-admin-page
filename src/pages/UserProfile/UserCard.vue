<template>
  <md-card class="md-card-profile ">
    <p>Загрузить изображения</p>
    <div class="row m-1">
      <div class="hello col-md-4">    
        <picture-input 
          ref="pictureInput"
          width="100" 
          height="150" 
          margin="1" 
          accept="image/jpeg,image/png" 
          size="10" 
          button-class="btn"
          :custom-strings="{
            upload: '<h1>Bummer!</h1>',
            drag: 'Drag a 😺 GIF or GTFO'
          }"
          @change="onChange">
        </picture-input>
      </div>
      <div class="hello  col-md-4">    
        <picture-input 
          ref="pictureInput"
          width="100" 
          height="150" 
          margin="1" 
          accept="image/jpeg,image/png" 
          size="10" 
          button-class="btn"
          :custom-strings="{
            upload: '<h1>Bummer!</h1>',
            drag: 'Drag a 😺 GIF or GTFO'
          }"
          @change="onChange">
        </picture-input>
      </div>
      <div class="hello  col-md-4">    
        <picture-input 
          ref="pictureInput"
          width="100" 
          height="150" 
          margin="1" 
          accept="image/jpeg,image/png" 
          size="10" 
          button-class="btn"
          :custom-strings="{
            upload: '<h1>Bummer!</h1>',
            drag: 'Drag a 😺 GIF or GTFO'
          }"
          @change="onChange">
        </picture-input>
      </div>
    </div>
    <!-- <md-card-content>
      <h6 class="category text-gray">CEO / Co-Founder</h6>
      <h4 class="card-title">Alec Thompson</h4>
      <p class="card-description">
        Don't be scared of the truth because we need to restart the human
        foundation in truth And I love you like Kanye loves Kanye I love Rick
        Owens’ bed design but the back is...
      </p>
      <md-button class="md-round md-success">Follow</md-button>
    </md-card-content> -->
  </md-card>
</template>
<script>
import PictureInput from 'vue-picture-input'

export default {
  name: 'user-card',
  data () {
    return {
    }
  },
  components: {
    PictureInput
  },
  methods: {
    onChange (image) {
      console.log('New picture selected!')
      if (image) {
        console.log('Picture loaded.')
        this.image = image
      } else {
        console.log('FileReader API not supported: use the <form>, Luke!')
      }
    }
  }
}
</script>
<style></style>
