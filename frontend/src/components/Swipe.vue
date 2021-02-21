<template>
    <div class="main">
        <div class="left-col"><div class="content-box">
            <h3>Rating</h3>
            <h4>{{movies[count].rating}} </h4>
            <img src="../assets/images/rating.png" class="rating">
            <h3>Description</h3>
            <p>{{movies[count].synopsis}}</p>
            <button v-on:click="count += 1">Preview clips from this film<img src="../assets/images/arrow.png"></button>
        </div>  
    </div>
    <div class="right-col">
      <div class="cast">
            <h3>Cast</h3>
            <ul>
            <li>{{this.cast[0]}}</li>
            <li>{{this.cast[1]}}</li>
            <li>{{this.cast[2]}}</li>
            </ul>
        </div>
    </div>
    <button v-on:click="count += 1"><img src="../assets/images/yes.png" class="accept"> </button>
    <button v-on:click="count += 1"><img src="../assets/images/no.png" class="reject"> </button>
    <img :src="movies[count].largeimage" class="main-img">
    <div class="movie-box">
        <h1>{{movies[count].title}}</h1>
    </div>
    <button v-on:click="count -= 1"><img src="../assets/images/maybe.png" class="save"> </button>
  </div>
</template>

<script>
import axios from 'axios';

export default {
    name: 'Swipe',
    data(){
        return{
            movies:[],
            count: 0,
            title: '',
            cast: '',
            rating: '',
            desc: '',
            image: '',
        }
    },
    created(){
        this.getMovies();
    },
    methods :{
        async getMovies(){
            let tempMovies= [];
            const options = {
                method: 'GET',
                url: 'https://unogs-unogs-v1.p.rapidapi.com/aaapi.cgi',
                params: {
                    q: 'get:new7-!1900,2018-!0,5-!0,10-!0-!Any-!Any-!Any-!gt100-!{downloadable}',
                    t: 'ns',
                    cl: 'all',
                    st: 'adv',
                    ob: 'Relevance',
                    p: '1',
                    sa: 'and'
                },
                headers: {
                    'x-rapidapi-key': '6f81e272b7mshb1b9a24a32c2189p19fd2ajsn8314bbf4903c',
                    'x-rapidapi-host': 'unogs-unogs-v1.p.rapidapi.com'
                }
            };
            
            await axios.request(options).then(function (response) {
                console.log("start");
                console.log(response.data);
                tempMovies = response.data.ITEMS;
            }).catch(function (error) {
                console.error(error);
            });
            this.movies = tempMovies;

        }
    }
}

</script>

<style scoped>
.main{
    width: 100%;
    height: 100vh;
    display: flex;
    overflow: hidden;
}
.left-col{
    flex-basis: 50%;
    background: #b8b8d4;
    position: relative;
}

.right-col{
    flex-basis: 50%;
    background: #9797b8;
    position: relative;
}
.content-box{
    width: 290px;
    position: absolute;
    top: 95px;
    left: 200px;
}
.rating{
    width: 90px;
    margin-bottom:15px;
}
.movie-box h1{
    font-size: 48px;
    margin: 15px 15px 15px;
    bottom:5%;
}
.content-box h3{
    font-size: 28px;
    margin-bottom: 10px;
    color: white;
}
.content-box p{
    font-size: 18px;
    color: #e9e3e3;
    line-height: 1.3em;
    margin-bottom: 80px;
}

.content-box button{
    background: #3434ad;
    color: #fff;
    display: flex;
    align-items: center;
    border: 0;
    outline: none;
    border-radius: 4px;
    padding: 13px 25px;
    cursor: pointer;
}
.content-box button img{
    width: 25px;
    margin-left: 20px;
}
.reject{
    width: 85px;
    position: absolute;
    top:90%;
    left: 770px;
}
.cast{
    width: 220px;
    display: block;
    position: absolute;
    top: 60px;
    right: 250px;
    flex-direction: column;
    
}
.cast h3{
    font-size: 28px;
    margin-bottom: 5px;
    color: white;
}
.cast-img{
    width: 175px;
    margin: 10px 0;
}

.accept{
    width: 85px;
    position: absolute;
    top:90%;
    right: 770px;
}

.save{
    width: 95px;
    position: absolute;
    top: 95%;
    left: 50%;
    transform: translate(-50%,-50%);
}
.movie-box{
    width: 435px;
    position: absolute;
    top:86%;
    left: 50%;
    transform: translate(-50%,-50%);
}
.main-img{
    width: 400px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
}
</style>