<template>
  <!--内容-->

  <div class="row my-index-center">
    <div class="top"><Nav :islogin="islogin"></Nav></div>
    <!--内容左空白-->
    <div class="col-md-2"></div>
    <!--内容左空白end-->
    <!--中间内容-->
    <div class="col-md-8">
      <div class="row panel panel-info">
        <div class="panel-heading">
          <div class="jumbotron">
            <h1>聘多多团队</h1>
            <p>项目简介：聘多多招聘网站为正在求职的求职者提供找工作，招聘，岗位推荐等服务，可以让正在求职的或者正在迷茫的人找到出路，并且可以从各种评价当中了解到各个公司的文化，福利等等。可以解决求职者不了解公司文化，公司不了解求职者价值观这一主要问题。当然我们的面向的用户主要就是应届生和还在学校上课的学生们，这类人群现阶段主要就是迷茫对于未来的不确定，我们的推荐功能则可以让这类人对于自己更好的评价，找到自己的定位。</p>
            <p class="col-md-10"></p>
            <p class="col-md-1"><a class="btn btn-warning btn-lg" href="#our" role="button">关于我们</a></p>
          </div>
        </div>
        <div class="panel-body text-center" id="our">
          <div class="row">
            <div class="col-md-4 text-center">
              <div class="panel panel-info">
                <div class="panel-heading">
                  <h4>我们的宗旨是!</h4>
                </div>
                <div class="panel-body">
                  <p>为个人提供一个企业招聘信息的平台，通过该平台，为个人寻找合适的工作提供便捷的途径!</p>
                </div>
              </div>
            </div>
            <div class="col-md-8 our-img">
              <img src="/static/images/image/logo.jpg" alt="">
            </div>
          </div>
          <div class="row">
            <div class="col-md-3">
              <div class=" panel panel-info word">
                <div class="panel-heading">高明</div>
                <div class="panel-body img">
                </div>
                <p>专业：信息管理与信息系统</p>
                <p>学校：东北石油大学</p>
              </div>
            </div>
            <div class="col-md-3">
              <div class=" panel panel-info word">
                <div class="panel-heading">储小琴</div>
                <div class="panel-body img">
                </div>
                <p>专业：网络工程</p>
                <p>学校：淮南师范学院</p>
              </div>
            </div>
            <div class="col-md-3">
              <div class=" panel panel-info word">
                <div class="panel-heading">方君</div>
                <div class="panel-body img">
                </div>
                <p>专业：网络工程</p>
                <p>学校：淮南师范学院</p>
              </div>
            </div>
            <div class="col-md-3">
              <div class=" panel panel-info word">
                <div class="panel-heading">韩旭</div>
                <div class="panel-body img">
                </div>
                <p>专业：计算机科学技术</p>
                <p>学校：大庆师范学院</p>
              </div>
            </div>
          </div>
        </div>
      </div>

    </div>
    <!--中间内容end-->

  </div>


</template>

<script>
  import Nav from '../components/generic_components/Nav'
  import axios from 'axios'
  export default {
    name: 'developer',
    data(){
      return{
        islogin:false
      }
    },
    mounted:function(){
      this.isLogin();
    },

    watch:{
      islogin:function (newvalue,oldvalue) {
        console.log(newvalue);
        console.log(oldvalue);
        return newvalue}
    },
    components:{
      Nav,
    },
    methods:{

      isLogin: function () {
        let token=sessionStorage.getItem('token');
        // console.log( token);
        if(token){
          let vm=this;
          axios.post('http://127.0.0.1:8000/user/verify/',
            {
              token:token
            }
          ).then(function (response) {
            let res=response.data;
            console.log(res);
            vm.islogin= res.user


          }).catch(function (error) {
            vm.islogin= false;
            console.log(error);

          })
        }
        // axios.get()
      },

    },

    watch:{
      islogin:function () {
        return this.isLogin
      },
    }
  }

</script>

<style scoped>
  .my-nav-img img {
    height: 65px;
  }

  .my-nav a{
    color: white;
  }

  .my-every-btn button {
    color: white;
    width: 80px;
    height: 80px;
    border: solid 0px black;
    border-radius: 50%;
    box-shadow: #7b8099 2px 2px 2px;
  }

  .my-index-center {
    /*padding-top: 20px;*/
    min-height: 600px;
  }
  .img img{
    /*width: 100px;*/
    /*height: 100px;*/
    border-radius: 50%;
  }
  .jumbotron{
    color: white;
    /*background-image: url("../assets/images/our.png");*/
  }
  .jumbotron {
    text-shadow: #000000 2px 2px 2px;
  }
  .word h4{
    color: orange;
  }
  .our-img img{
    margin-left: 400px;
    /*width: 500px;*/
    /*height: 200px;*/
    border-radius: 5px;
  }
</style>
