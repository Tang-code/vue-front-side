<template>
  <div class="recovery">
    <van-row>
      <van-col span="24">
        <van-nav-bar
          title="社区动态"
          left-text="返回"
          right-text="发布"
          left-arrow
          @click-left="onClickLeft"
          @click-right="onClickRight"
          class="top_nav"
        />
      </van-col>
    </van-row>
    <van-row class="head">
      <van-col span="4">
        <div class="head_box">
          <van-image width="40" height="40" round src="https://img.yzcdn.cn/vant/cat.jpeg" />
        </div>
      </van-col>
      <van-col span="20" class="msg">
        <span class="name">王思聪</span>
        <span class="time">今天12:22</span>
      </van-col>
    </van-row>
    <van-row class="text">
      <van-col span="24">
        <p>Vant 提供了一套默认主题，CSS 命名采用 BEM 的风格，方便使用者覆盖样式。如果你想完全替换主题色或者其他样式，可以使用下面提供的方法</p>
        <div class="img_box">
          <van-image width="100%" height="100%" src="https://img.yzcdn.cn/vant/cat.jpeg" />
        </div>
      </van-col>
    </van-row>
    <van-row class="comment_box">
      <van-col span="24">
        <span class="comment"><van-icon name="good-job-o" /></span>
        <span class="thumbs-up"><van-icon name="chat-o" /></span>
      </van-col>
    </van-row>
  </div>
</template>

<script>
import {
  Row,
  Col,
  NavBar,
  Toast,
  Cell,
  CellGroup,
  Field,
  Area,
  Popup,
  DatetimePicker,
  Uploader,
  Button,
  Image,
  Icon
} from "vant";
export default {
  components: {
    [Row.name]: Row,
    [Col.name]: Col,
    [NavBar.name]: NavBar,
    [Toast.name]: Toast,
    [Cell.name]: Cell,
    [CellGroup.name]: CellGroup,
    [Field.name]: Field,
    [Area.name]: Area,
    [Popup.name]: Popup,
    [DatetimePicker.name]: DatetimePicker,
    [Uploader.name]: Uploader,
    [Button.name]: Button,
    [Image.name]: Image,
    [Icon.name]:Icon
  },
  methods: {
    onClickLeft() {
      Toast("返回");
    },
    onClickRight() {
      Toast("按钮");
    }
  },
  data() {
    return {};
  }
};
</script>

<style lang="less" scoped>
//导航
.top_nav {
  font-size: 32px;
}

.van-nav-bar__title,
.van-nav-bar {
  height: 88px;
  line-height: 88px;
}

//头像
.head {
  text-align: left;
  .head_box {
    margin: 24px 20px;
  }
}
.msg {
  line-height: 1.6;
  margin-top: 26px;
  span {
    font-size: 30px;
    display: block;
  }
  .time {
    font-size: 24px;
    color: rgb(177, 177, 177);
  }
}
.text {
  // margin: 20px 0;

  padding: 0 20px;
  p {
    font-size: 28px;
    text-align: justify;
    margin-bottom: 20px;
  }
}
//评论
.comment_box {
  
  padding: 0 20px;
  text-align: right;
  .comment {
    margin: 0 20px;
  }
  .van-col {
    padding: 20px 0;
    border-bottom: 1px solid #DDD;
  }
}
</style>