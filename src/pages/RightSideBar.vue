<template>
      <div class="tt">
        <!-- 头部 -->
        <div class="tou">
         <div class="pair" v-text="title"></div>
         <div class="cof">
            <div class="friend">
                <div class="acof">
                    <span class="ps"> &nbsp;&nbsp;朋友圈</span>
                    <span style="float:right">
                        <span  class="pl"></span>
                    </span>                    
                </div>
            </div>
        </div>
        <!-- 选项卡点击部分 -->
        <div class="pd">
            <div class="db">
                <span class="pairing" @click="changeContent(index)" v-for="(t,index) in tabber" :key="index" v-text="t.title" :class="{
        'actived':tab===index}"></span>
            </div>
        </div>
        </div>
        <!-- 选项卡对应的内容1 -->
        <div class="spc">
          <div class="chactBox" v-for="(i,index) in arr" :key='index' v-show="tab===0">
            <div class="hp">
                <div class="hpImg"><img :src="i.img"></div>
            </div>
            <div class="contain">
                <div class="user" v-text="i.name"></div>
                <div class="dialogue" v-text="i.dialogue"></div>
            </div>
         </div>
        <!-- </div> -->
        <!-- 选项卡对应的内容2 -->
        <!-- <div class="spc"> -->
          <div class="chactBox" v-for="(i,index) in arr1" :key='index' v-show="tab===1">
            <div class="hp">
                <div class="hpImg"><img :src="i.img"></div>
            </div>
            <div class="contain">
                <div class="user" v-text="i.name"></div>
                <div class="dialogue" v-text="i.dialogue"></div>
            </div>
          </div>
        </div> 
      </div>     
</template>
<style scopde>
.spc{
  height: 13.973333rem;
  background: #292625;
}
 .db .actived {
  border-bottom: 0.053333rem solid #d34530;
  color: #fff;
}
.tt {
  width: 8.623188rem;
  float: right;
  overflow: hidden;
  background: #25211f;
  color: white;
  height: 19.626667rem;
}
.pair {
  width: 100%;
  height: 1.73913rem;
  line-height: 1.73913rem;
  margin-left: 0.389855rem;
  font-size: 0.59rem;
}
.cof {
  height: 1.811594rem;
  width: 100%;
  text-align: center;
  display: flex;
}
.friend {
  height: 1.328502rem;
  width: 7.971014rem;
  background: #33302e;
  border-radius: 0.241546rem;
  margin: auto;
}
.acof {
  height: 1.328502rem;
  width: 7.971014rem;
}
.ps {
  padding-left: 0.966184rem;
  height: 1.328502rem;
  font-size: .426667rem;
  float: left;
  line-height: 1.328502rem;
  background: url(../assets/p.png) no-repeat left;
  background-size: 0.724638rem;
  margin-left: 0.289855rem;
}
.pl {
  margin-top: 0.193237rem;
  height: 0.942029rem;
  width: 0.942029rem;
  line-height: 0.942029rem;
  float: left;
  border-radius: 50%;
  border: 0.024155rem solid #cccccc;
  background: url(../assets/tou.png);
  background-size: 0.942029rem;
  margin-right: .4rem;
}
.pr {
  height: 1.328502rem;
  margin-right: 0.289855rem;
  float: right;
  width: 0.362319rem;
  line-height: 1.328502rem;
  font-size: 0.531401rem;
}
.pd {
  height: 0.845411rem;
  padding-bottom: 0.193237rem;
  margin-top: .533333rem;
}

.db {
  width: 7.971014rem;
  height: 0.797101rem;
  margin: auto;
}
.db > span {
  display: inline-block;
  width: 3.961353rem;
  height: 1.013333rem;
  text-align: center;
  line-height: 1.013333rem;
  font-size: .4rem;
  color: #747474;
}
.db .pairing {
  border-right: none;
}
.chactBox,
.chactBox1 {
  height: 1.811594rem;
  width: 100%;
}
.hp {
  width: 2.05314rem;
  float: left;
  height: 1.811594rem;
}
.hpImg {
  height: 1.449275rem;
  width: 1.449275rem;
  border-radius: 50%;
  margin-top: 0.144928rem;
  margin-left: 0.289855rem;
  border: 0.024155rem solid #ccc;
  overflow: hidden;
}
.hpImg img {
  height: 1.449275rem;
}
.contain {
  float: right;
  margin-top: 0.289855rem;
  width: 6.521739rem;
  height: 1.449275rem;
  border-bottom: 0.024155rem solid #302d2b;
}
.user {
  font-size: .426667rem;
}
.dialogue {
  font-size: .4rem;
  line-height: 0.676329rem;
  color: #747474;
}
</style>
<script>
import img1 from "../assets/1.jpg";
import img2 from "../assets/2.jpg";
import img3 from "../assets/5.jpg";
import img4 from "../assets/4.jpg";
import img5 from "../assets/3.jpg";
export default {
  data() {
    return {
      pair: "999个匹配",
      arr: [
        {
          img: img1,
          name: "十八岁的老阿姨",
          dialogue: "配对于4月10号"
        },
        {
          name: "小猪家的胖胖",
          dialogue: "配对于4月12号",
          img: img2
        },
        {
          img: img3,
          name: "会打架的菠萝",
          dialogue: "配对于4月13号"
        },
        {
          name: "小猪家的胖胖",
          dialogue: "配对于4月14号",
          img: img4
        },
        {
          img: img5,
          name: "大番薯",
          dialogue: "配对于4月15号"
        }
      ],
      arr1: [
        {
          img: img1,
          name: "十",
          dialogue: "多喝热水"
        },
        {
          name: "小",
          dialogue: "我佛了",
          img: img2
        },
        {
          img: img3,
          name: "会打架的菠萝",
          dialogue: "好困好累"
        },
        {
          name: "小猪家的胖胖",
          dialogue: "好咯",
          img: img4
        },
        {
          img: img5,
          name: "大番薯",
          dialogue: "完犊子了"
        }
      ],
      tabber: [{ title: "所有配对" }, { title: "聊天" }],
      tab: 0,
      title: "所有配对"
    };
  },
  methods: {
    // 切换底部选项卡
    changeContent(tab) {
      this.tab = tab;
      this.title = this.tabber[tab].title;
    }
  }
};
</script>


