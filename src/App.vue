<template>
  <div id="app">
    <full-page :options="options" id="fullpage" ref="fullpage">
      <div class="section" id="section1">
        <img src="https://bj.bcebos.com/szbwg/tmp/test_a/lm/Text.svg" id="wyzc">
        <img src="https://bj.bcebos.com/szbwg/tmp/test_a/lm/向上滑动查看.svg" id="xshd">
      </div>
      <div class="section" id="section2">
        <p id="new_in_cuc" class="base_text">
          {{ p.admission_time }}，<br>
          你从 <span class="emphasis">{{ p.province }}</span> 来到中传，<br>
          推开了 <span class="emphasis">{{ p.dormitory }}</span> 的大门。<br>
          <span class="emphasis">{{ p.earliest_course_time }}，{{ p.earliest_course_loc }}</span> <br>
          是你大学生涯的第一门课——<br>
          <span class="emphasis">{{ p.earliest_course }}</span><br>
          <!--          除此之外还有-->
          <!--          <span class="emphasis" id="courses_list">-->
          <!--          西方社会与文化、英语语音与诵读艺术（1）、逆向工程与软件安全、网络安全、高级数据库技术、自然语言处理、操作系统、编译原理、人工智能、新闻理论、密码学应用实践、数字内容安全应用实践、思想政治理论课综合实践、毛泽东思想和中共党史、大学英语（4）、大学物理（1）、大学物理实验（1）、大学数学（1）、大学数学实验（1）、大学计算机基础、大学计算机基础实验、大学英语（3）、大学物理（2）、大学物理实验（2）、大学数学（2）、大学数学实验（2）、大学计算机基础（2）、大学计算机基础实验（2）、大学英语（2）、大学物理（3）、大学物理实验（3）、大学数学（3）、大学数学实验（3）、大学计算机基础（3）、大学计算机基础实验（3）、大学英语（1）、大学物理（4）、大学物理实验（4）、大学数学（4）、大学数学实验（4）、大学计算机基础（4）、大学计算机基础实验（4）。-->
          <!--          </span>-->
        </p>
      </div>
      <div class="section" id="section3">
        <p id="new_in_cuc" class="base_text">
          你在🚢上了 <span class="emphasis">{{ p.course_num }}</span>门课<br>
          在课堂上度过了<span class="emphasis">{{ p.credit_hours }}</span>小时<br>
          <!--          相当于<span class="emphasis">{{ p.time_second }}</span>秒<br>-->
          相当于<span class="emphasis">{{ p.time_day }}</span>天<br>
          在<span class="emphasis">{{ p.required_num }}</span>门必修和<span class="emphasis">{{ p.elective_num }}</span>门选修中<br>
          你学得最好的课程是<br>
          <span class="emphasis">{{ p.highest_score_course }}</span><br>
          考过最差的课程是<br>
          <span class="emphasis">{{ p.lowest_score_course }}</span><br>
          仅仅<span class="emphasis">{{ p.lowest_score }}</span>分<br>
          陪伴你最多的是<span class="emphasis">{{ p.teacher_name }}</span>老师<br>
          你们一起度过了<span class="emphasis">{{ p.teacher_time }}</span>学时
        </p>
      </div>
      <div class="section" id="section4">
        <p id="new_in_cuc" class="base_text">
          最近一年，<br>
          你对<span class="emphasis">{{ p.highest_spender }}</span>情有独钟<br>
          总消费高达<span class="emphasis">{{ p.highest_spender_money }}</span>元<br>
          人送外号“<span class="emphasis">{{ p.nickname }}</span>”

        </p>
      </div>
      <div class="section" id="section5">
        <img src="https://bj.bcebos.com/szbwg/tmp/xwu/Group 178.svg" id="bykl"
             @click="feedback">
      </div>
    </full-page>
  </div>
</template>


<style>


#section1 {
  background: url(https://bj.bcebos.com/szbwg/tmp/test_a/lm/51s.svg) no-repeat bottom center;
  background-size: cover;
}

#section2 {
  background: url(https://bj.bcebos.com/szbwg/tmp/test_a/41.svg) no-repeat bottom center;
  background-size: cover;
}

#section3 {
  background: url(https://bj.bcebos.com/szbwg/tmp/test_a/4s2.svg) no-repeat bottom center;
  background-size: cover;
}

#section4 {
  background: url(https://bj.bcebos.com/szbwg/tmp/test_a/52.svg) no-repeat bottom center;
  background-size: cover;
}

#section5 {
  background: url(https://bj.bcebos.com/szbwg/tmp/test_a/11.svg) no-repeat bottom center;
  background-size: cover;
}

#wyzc {
  /*宽度为最大宽度的40%，高度缩放，绝对定位，top为最大高度的10%*/
  width: 40%;
  height: auto;
  position: absolute;
  top: 20%;
  left: 50%;
  transform: translateX(-50%);
}

#xshd {
  /*宽度为最大宽度的40%，高度缩放，绝对定位，top为最大高度的10%*/
  width: 20%;
  height: auto;
  position: absolute;
  bottom: 2%;
  left: 50%;
  transform: translateX(-50%);
}

#bykl {
  /*宽度为最大宽度的40%，高度缩放，绝对定位，top为最大高度的10%*/
  width: 382/414;
  height: auto;
  position: absolute;
  top: 20%;
  left: 50%;
  transform: translateX(-50%);
}


.base_text {
  color: #fff;
  position: absolute;
  left: 10%;
  top: 10%;
  font-size: 1.2rem;
  /*宋体、行间距1.5*/
  font-family: SimSun, serif;
  line-height: 1.5;
  will-change: opacity, transform;
  overflow: hidden;
}

#section4 .base_text {
  color: #000000 !important;
}

/*设置强调文字样式*/

.emphasis {
  color: #FAFF00;
  font-weight: bold;
  font-size: 1.5rem;
}

/*#courses_list {*/
/*  !*自动换行，最长为5行，多余的行隐藏*!*/
/*  word-wrap: break-word;*/
/*  word-break: break-all;*/
/*  -webkit-line-clamp: 5;*/
/*  display: -webkit-box;*/
/*  -webkit-box-orient: vertical;*/
/*  overflow: hidden;*/
/*  font-size: 1.5rem;*/
/*  width: 80%;*/

/*}*/

</style>


<script>
import gsap from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'
import {onMounted} from "vue";


gsap.registerPlugin(ScrollTrigger);

export default {

  name: 'app',
  data() {
    return {
      p: {},
      options: {
        licenseKey: 'YOUR_KEY_HERE',
        onLeave: this.onLeave,
        afterRender: this.afterRender,
        scrollOverflow: true,
        scrollBar: false,
        menu: '#menu',
        navigation: false,
        anchors: ['page1', 'page2', 'page3'],
        normalScrollElements: ['courses_list'],
        sectionsColor: ['#fff', '#ff5f45', '#0798ec', '#fec401', '#1bcee6', '#ee1a59', '#2c3e4f', '#ba5be9', '#b4b8ab']
      }
    }
  },
  methods: {
    afterRender() {
      // #wyzc渐入效果，从上方滑出，透明度从0到1，只显示一次。
      gsap.from("#wyzc", {duration: 0.5, y: -50, opacity: 0})
      // #xshd闪动效果，持续闪烁，从左到右闪烁
      gsap.from("#xshd", {duration: 0.8, opacity: 0, repeat: -1, yoyo: true, delay: 2})
    },

    onLeave(current, next) {
      let index = next.index
      if (index == 1) {
        gsap.from("#new_in_cuc", {duration: 1, y: -50, opacity: 0, delay: 1})
        console.log("111")
        console.log(this.p)
        //设置#courses_list从左向右滑动，直到最最右停下，先慢后快后慢。
        // let tl = gsap.timeline({repeat: 0, delay: 10})
        // let element_width = window.getComputedStyle(document.querySelector('#courses_list'), null).width
        // let length = element_width.slice(0, -2)
        // tl.to("#courses_list", {duration: 20, x: -length, ease: 'power2.inOut'})
      }


    },

    feedback() {
      window.location.href = 'https://neixiangde.ren/contact-form'
    }
  },
  mounted() {

    //  获取url参数 username 和 password
    let json_key = new URLSearchParams(window.location.search).get('key');
    const json_url = "https://cuc.neixiangde.ren/2023grads/" + json_key
    console.log("data url:" + json_url)
    // 从获取的url中获取json，放置到this.p
    fetch(json_url)
        .then(response => response.json())
        .then(data => {
          this.p = data
        });

  }
}
</script>

