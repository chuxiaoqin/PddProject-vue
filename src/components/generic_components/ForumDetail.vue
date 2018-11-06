<template>
  <div class="body-container">
  <div class=" left_container">
    <div class="first">
      <div class="head_img">
      <div class="img">
        <img src="" alt="">
      </div>
        <p>树欲静</p>
        <p>上海仁度生物科技有限公司/总监/部门经理</p>
      </div>
      <div class="btn-ser">
        <span class="follow">
          + 关注</span>
        <span class="ask">向他提问</span>
      </div>
      <div class="first-boot">
        <div class="follow1">
          <p class="first-child">0</p>
          <p class="second-child">关注</p>
        </div>
        <div class="follow2">
          <p class="first-child">111</p>
          <p class="second-child">粉丝</p>
        </div>
      </div>
    </div>
    <div class="second">
      <div class="item">
        <div class="content">
          <div class="list-left">
              <span class="logo"></span>
            <img src="../../static/img/cat.svg" alt="">
          </div>
          <div class="list-right">
            <p class="breakcontent">大连外国语大学</p>
            <p class="">国际经济与贸易</p>
          </div>
        </div>
      </div>
      <div class="item">
        <div class="content">
          <div class="list-left">
            <span class="logo"></span>
            <img src="../../static/img/building.svg" alt="">
          </div>
          <div class="list-right">
            <p class="breakcontent">大连外国语大学</p>
            <p class="">国际经济与贸易</p>
          </div>
        </div>
      </div>
      <div class="item">
        <div class="content">
          <div class="list-left">
            <span class="logo"></span>
            <img src="../../static/img/lamp.svg" alt="">
          </div>
          <div class="list-right">
            <p class="breakcontent">大连外国语大学</p>
            <p class="">国际经济与贸易</p>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="nav-container">
    <div class="nav-content">
      <div class="nav-item">
        <a class="all">全部</a>
      </div>

      <div class="nav-item">
        <a class="ask1">提问</a>
      </div>

      <div class="nav-item">
        <a class="reply">回答</a>
      </div>

      <div class="nav-item">
        <a class="dynamic">动态</a>
      </div>

      <div class="nav-item">
        <a class="article">文章</a>
      </div>


    </div>
    </div>
  </div>
</template>
<script>

  export default {
    name: 'forumdetail',
    data () {
      return {
        msg: 'Practiailce make perfect'
      }
    }
  }
</script>
<style>
  .body-container{
    width: 100%;
    height: 600px;
    margin:80px 0px 0px 0px;
    background: #F6F6F6;
  }
  .left_container{
    float:left;
    width:306px ;
    height: 600px;
    margin: 20px 0px 0px 150px;

  }
  .first{
    width: 306px;
    background: white;

  }
  .first .head_img{
    text-align: center;
    height: 90px;
    background: #fff8ed;
  }
  .first .head_img .img{
    display: inline-block;
    width: 100px;
    height: 90px;
    border-radius: 50%;
    position: relative;
    left: 10px;
  }
  .first .btn-ser{
    width: 183px;
    margin: 80px auto;
  }
  .btn-ser .follow{
    display: inline-block;
    width: 81px;
    height: 31px;
    line-height: 31px;
    background: #0588ff;
    text-align: center;
    color: white;
    font-size: 14px;
    cursor: pointer;
  }
  .btn-ser .ask{
    display: inline-block;
    width: 81px;
    height: 31px;
    margin-left: 10px;
    line-height: 31px;
    background:#0588ff;
    text-align: center;
    color: white;
    cursor: pointer;
     }
  .first .first-boot{
    border-top: solid 1px #ecece4;
    margin-top: -50px;
    width: 100%;
    height: 58px;
  }
  .first-boot .follow1{
    float: left;
    width: 153px;
    height: 58px;
    background: white;
    border-right: solid 1px #ecece4;
  }
  .first-boot .follow2{
    float: right ;
    width: 153px;
    height: 58px;
    background: white;
  }
  /*.first-boot .follow2.follow1>.first-child{*/
    /*margin-top: 5px;*/
    /*font-size: 16px;*/
  /*}*/
  /*.first-boot .follow2.follow1>.second-child{*/
    /*margin-top: 3px;*/
    /*font-size: 16px;*/
    /*margin-bottom: 3px;*/
  /*}*/
.left_container .second{
  width: 306px;
  height: 183px;
  background: white;
  margin-top: -5px;
}
  .second .item{
    width: 100%;
    height: 32px;
    margin-top: 23px;
    /*height: 30px;*/
    /*background: #bfbdc0;*/
  }
  .second .item .content{
    width: 100%;
    height: 100%;
    margin-top: 5px;
    padding-top: 20px;
    /*height: 50px;*/
    /*background: #96d5d2;*/
    /*background: url("../../static/img/cat.svg") no-repeat;*/
  }
  .content .list-left{
    float: left;
    width: 47px;
    height: 24px;
    /*background: #4078c0;*/
  }
  .content .list-left .logo{
    width: 100%;
    height: 100%;
    /*background: url("../../static/img/cat.svg");*/
    /*position: relative;*/
    /*left: -130px;*/
    /*top: 20px;*/
  }
  .content .list-right{
    float: left;
    width: 240px;
    height:32px;
    background: white;
  }
  .list-right p{
    text-align: left;
    width: 240px;
    height: 6px;
  }
  .nav-container{
    width: 700px;
    height: 62px;
    background: white;
    position: relative;
    top: 20px;
    left: 500px;
  }
  .nav-container .nav-content{
    height: 62px;
    padding: 0 24px;
    box-sizing: border-box;
    background: #fff;
    text-align: left;
    position: relative;
    top: 10px;



    /*width: 500px;*/
    /*height: 62px;*/
    /*!*margin: auto;*!*/
    /*font-size: 16px;*/
    /*background:white;*/
    /*background: #00B38A;*/
  }
  .nav-content .nav-item{
    display: inline-block;
    font-size: 16px;
    text-align: center;
    width: 105px;
    position: relative;
    left: -440px;
    top: 10px;
  }
  .nav-content .all,.ask1,.reply,.dynamic,.article{
    display: inline-block;
    height: 52px;
    font-weight: 900;
    /*display: inline-block;}*/
  }
    /*!*width:80px;*!*/
    /*!*height: 62px;*!*/
    /*!*line-height: 62px;*!*/
    /*text-align: center;*/
    /*position: relative;*/
    /*left: -400px;*/
    /*color: #0588ff;*/
    /*!*background: #4078c0;*!*/
  /*}*/
  .nav-content a{
    text-decoration: none;
    color: black;
  }
  .all{
    color:#0588ff;
    border-bottom: solid 2px  #0588ff ;
    /*background: #ff18be;*/
  }
  .ask1{
    position: relative;
    left: -25px;

  }
  .reply{
    position: relative;
    top: -52px;
    left: 165px;
  }
  .dynamic{
    position: relative;
    top: -52px;
    left: 130px;
  }
  .article{
    position: relative;
    top: -102px;
    left: 320px;
  }

</style>
