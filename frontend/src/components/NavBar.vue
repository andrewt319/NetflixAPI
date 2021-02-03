<template>
<div class="topnav">
    <img class="logo" alt="Vue logo" src="../assets/images/netflix.png">
    <div class="topnav-right">
        <div class="search-box">
          <input type="text" placeholder="Find a movie">
          <img src="../assets/images/search.png" class="search-box img">
        </div>
        <ul>
            <li><a href=""><img src="../assets/images/fill-tag.png">Saves</a></li>
            <li><a href="">Sign Up</a></li>
        </ul>
    </div>
</div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
.logo{
    width: 80px;
    margin: 20px 60px;
}
.search-box{
    display: flex;
    align-items: center;
    background: rgba(255,255,255,0.3);
    padding: 7px 15px;
    border-radius: 20px;
    width:14em;
}
.search-box input{
    background: transparent;
    border: 0;
    outline: none;
    color: #fff;
}
::placeholder{
    color: #fff;
    font-size: 12px;
}
.search-box img{
    width: 13px;
    margin-left: 20px;
}
.topnav-right ul{
    display: flex;
}

.topnav-right ul li{
    list-style: none;
    margin-left: 50px;
}
.topnav-right ul li a{
    color: #fff;
    text-decoration: none;
    font-size: 14px;
    display: flex;
    align-items: center;
}
.topnav-right ul li img{
    width: 15px;
    margin-right: 15px;
}
.topnav{
    background-color: rgb(171, 171, 202);
    overflow:hidden;
    display:flex;
}
.topnav-right{
    width:80%;
    margin:40px auto;
    display:flex;
    align-items:center;
    justify-content: flex-end;
}
</style>
