<template>
  <v-ons-page>
    <v-ons-toolbar>
    <div class="left">
        <v-ons-back-button>
          
        </v-ons-back-button>
      </div>
      <div class="center" style="text-align:center">キャスコレ</div>

      <div class="right">
        <v-ons-toolbar-button>
          <v-ons-icon icon="ion-navicon, material: md-menu"></v-ons-icon>
        </v-ons-toolbar-button>
      </div>
     <div class="center selecter_tab">
        <ul class="selecter_list" style="list-style:none">
          <li class="talent default_sellect">タレント</li>
          <li class="contents">コンテンツ</li>
          <li class="jobs">お仕事</li>
        </ul>
      </div>
    </v-ons-toolbar>

    <v-ons-tabbar 
      position="bottom"
      :tabs="tabs"
      :visible="true"
      :index.sync="activeIndex"
      modifier="bottom_bar"
      
      >
    </v-ons-tabbar>
  </v-ons-page>
</template>

<script>
  import feed from 'feed';
  import home from 'Home';
  import add from 'add';
  import message from 'message';
  import mypage from 'mypage';

  export default {
    data() {
      return {
        activeIndex: 0,
        tabs: [
	  {
	    icon: this.md() ? 'ion-home' : 'ion-home',
      label:"ホーム",
	    page: home
	  },
	  {
	    icon: this.md() ? 'layer-group' : 'layer-group',
      label:"フィード",
	    page: feed
	  },
	  {
	    icon: this.md() ? 'fa-plus-circle' : 'fa-plus-circle',
      label:"投稿",
      page: add,
      modifier: "add_icon"
	  },
	  {
	    icon: this.md() ? 'user' : 'user',
	    label:"マイページ",
	    page: mypage
	  },
	  {
	    icon: this.md() ? 'comments' : 'comments',
      label:"メッセージ",
	    page: message,
      badge: 7
	  }
        ]
      };
    },
    methods: {
      md() {
        return this.$ons.platform.isAndroid();
      }
    },
    computed: {
      title() {
        return this.tabs[this.activeIndex].label;
      }
    },
    components: { home, message, feed ,add , mypage }
  }
</script>


<style>

ons-icon.ons-icon.fa-plus-circle.fa{font-size:50px
}
.tabbar.tabbar--bottom_bar.tabbar--material.ons-tabbar__footer.ons-swiper-tabbar{padding-bottom:5px;padding-top:5px
}
ons-tab.tabbar--material__item.tabbar__item.tabbar--bottom_bar__item{background:none
}
.tabbar.tabbar--bottom_bar.tabbar--material.ons-tabbar__footer.ons-swiper-tabbar{
}
.tabbar__icon,.tabbar__label,button.tabbar__button.tabbar--material__button.tabbar--bottom_bar__button,ons-ripple.ripple--material.ripple{background:none
}
.tabbar__label{padding-top:7px
}
.page__content.page--material__content{background:none
}
ons-toolbar.toolbar--material.toolbar{background:#000;color:#fff
}
.center.toolbar__center.toolbar__title.toolbar--material__center{color:#fff
}
span.back-button__icon.back-button--material__icon{fill:#fff
}
ons-icon.ons-icon.zmdi.zmdi-menu{color:#fff;fill:#fff
}
ons-tab.tabbar--material__item.tabbar__item.tabbar--add_icon__item.tabbar--bottom_bar__item .tabbar__label{padding-top:14px
}
ons-toolbar.toolbar{background:#000
}
.center.toolbar__center.toolbar__title,.left.toolbar__left,ons-back-button.back-button,ons-icon.ons-icon.ion-navicon.ons-icon--ion{color:#fff
}
span.back-button__icon{color:#fff;fill:#fff
}
ons-tabbar{overflow:auto
}
.tabbar.tabbar--bottom_bar.ons-tabbar__footer.ons-swiper-tabbar{height:75px;padding-bottom:5px;padding-top:5px
}
.tabbar__label{padding-top:15px
}
.tabbar__icon{display: block!important;
    font-size: 24px;
    height: 33px;
    line-height: 30px;
    margin: 0;
    padding: 0;
}
button.tabbar__button.tabbar--bottom_bar__button{height:90px
}


.center.selecter_tab {
    color: #fff;
    display: block;
    position: absolute;
    text-align: center;
    width: 100%;
    bottom: 5px;
    margin: 0;
}

ons-toolbar.toolbar {
    height: 100px;
}

.tabbar__content {
    bottom: 84px;
}

.toolbar+.page__background+.page__content {
    padding-top: 0;
    top: 83px;
}


ul.selecter_list li {
    float: left;
    width: 33%;
    text-align: center;
    font-size: 12px;
    background: white;
    color: black;
    line-height: 28px;
    border: 1px solid black;
    margin-left: -1px;
    font-weight:900;
}

ul.selecter_list {
    -webkit-margin-after: 0;
    -webkit-margin-before: 0;
    -webkit-margin-end: 0;
    -webkit-margin-start: 0;
    -webkit-padding-start: 0;
    left: 10%;
    margin: 0 auto!important;
    margin-block-end: 0;
    margin-block-start: 0;
    margin-inline-end: 0;
    margin-inline-start: 0;
    padding-inline-start: 0;
    position: absolute;
    width: 80%;
    bottom: 0;
}

li.default_sellect {
    color: white !important;
    background: #d80000 !important;
}

.page__content {
    top: 50px !important;
}



</style>
