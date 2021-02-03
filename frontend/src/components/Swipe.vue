<template>
    <div class="main">
        <div class="left-col"><div class="content-box">
            <h3>Rating</h3>
            <img src="../assets/images/rating.png" class="rating">
            <h3>Description</h3>
            <p>Midwest native Nick Carraway (Tobey Maguire) arrives in 1922 New York in search of the American dream. Nick, a would-be writer, moves in next-door to millionaire Jay Gatsby (Leonardo DiCaprio) and across the bay from his cousin Daisy (Carey Mulligan) and her philandering husband, Tom (Joel Edgerton). Thus, Nick becomes drawn into the captivating world of the wealthy and -- as he bears witness to their illusions and deceits -- pens a tale of impossible love, dreams, and tragedy.</p>
            <button type="button">Preview clips from this film<img src="../assets/images/arrow.png"></button>
        </div>  
    </div>
    <div class="right-col">
      <div class="cast">
            <h3>Cast</h3>
            <img src="../assets/images/leo.jpg" class="cast-img">
            <img src="../assets/images/tobey.jpg" class="cast-img">
            <img src="../assets/images/carey.jpg" class="cast-img">
        </div>
    </div>
    <img src="../assets/images/yes.png" class="accept">
    <img src="../assets/images/no.png" class="reject">
    <img src="../assets/images/movie.jpg" class="main-img">
    <div class="movie-box">
        <h1>The Great Gatsby</h1>
    </div>
    <img src="../assets/images/maybe.png" class="save">
  </div>
</template>
<script>
export default {
    
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