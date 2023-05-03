<template>
  <div>
    <div style="font:16px Arial, Serif; scrollbar-color: rebeccapurple green; overflow:auto; width:100%; height:650px ">
      <div class="mt-10 grid lg:grid-cols-4 items-center">
        <div
          class="group group-hover:bg-opacity-60 transition duration-500 relative bg-white dark:bg-gray-800 dark:hover:bg-gray-700 sm:p-10  flex justify-center items-center"
          v-for="post in posts">
          <img class="group-hover:opacity-60 transition duration-500" id="tourCardImg"
            v-if="checktype(post.media_url) === 'img'" :src="post.media_url" alt="İnstagram İmage Gallery" />

          <video width="500px" height="450px" autoplay controls class="group-hover:opacity-60 transition duration-500"
            id="tourCardImg" v-if="checktype(post.media_url) === 'video'">
            <source :src="post.media_url" type="video/mp4" />
          </video>

        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      posts: [] // Instagram Basic Display API'den alınan post verilerini saklayacağımız data özelliği
    };
  },
  async created() {
    await this.getPosts(); // Bileşen oluşturulduğunda getPosts metodunu çağırın
  },
  methods: {
    async getPosts() {
      // Instagram Basic Display API isteği için API anahtarınızı ve diğer parametreleri ayarlayın
      const token = `IGQVJWXzNMSllrN05lbFJCdFl3dGk3SXkyUWV6R3M3UHVBNGxwYVNiRV9oNEh6bTB5ZA0VMcTVPNHBlQ3NOVllOM0wyNlRBN1BPMkU3VXlYZAnIxTjJhaWJXYlEzWDN4aFBfYjRtN1liNEpoQ1ZA6WE5uNQZDZD`;
      const url = `https://graph.instagram.com/me/media?fields=id,image,caption,media_url,like_count,comments_count&access_token=${token}`;

      try {
        const response = await fetch(url);
        const data = await response.json();
        this.posts = data.data; // API'den alınan post verilerini bileşenin data özelliğine atayın
      } catch (error) {
        console.error(error);

      }
    },
    checktype(string) {
      let type = null;
      if (string.match(/.png/g)) {
        //png
        type = 'img';
      } else if (string.match(/.jpg/g)) {
        //jpg
        type = 'img';
      } else if (string.match(/.JPG/g)) {
        //JPG
        type = 'img';
      } else if (string.match(/.jpeg/g)) {
        //jpeg
        type = 'img';
      } else if (string.match(/.JPEG/g)) {
        //JPEG
        type = 'img';
      } else if (string.match(/.gif/g)) {
        //gif
        type = 'img';
      } else {
        //video
        type = 'video';
      }
      return type;
    }
  }
};
</script>

<style scoped>
#tourCardImg {
  width: 25vw;
  height: 45vh;
  border-radius: 5%;
}



/* Masaüstü */
@media screen and (min-width: 1200px) {
  #tourCardImg {
    width: 25vw;
    height: 45vh;
    border-radius: 5%;
  }
}

/* Laptop */
@media screen and (min-width: 992px) and (max-width: 1199px) {
  #tourCardImg {
    width: 25vw;
    height: 45vh;
    border-radius: 5%;
  }
}

/* Tablet */
@media screen and (min-width: 768px) and (max-width: 991px) {

  #tourCardImg {
    width: 25vw;
    height: 45vh;
    border-radius: 5%;
  }
}

@media screen and (max-width:415px) and (min-height:375px) {
  #tourCardImg {
    flex-direction: column;
    width: 125vw;
    height: 45vh;

  }
}

/* Mobil */
@media screen and (max-width: 391px) and (min-height:375px) {
  #tourCardImg {
    flex-direction: column;
    width: 125vw;
    height: 45vh;

  }
}

/* width */
::-webkit-scrollbar {
  width: 20px;
}

/* Track */
::-webkit-scrollbar-track {
  box-shadow: inset 0 0 5px grey;
  border-radius: 10px;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: rgb(68, 178, 206);
  border-radius: 10px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #b30000;
}
</style>


