<template>
  <div id="contentBox">
    <!-- header -->
    <div id="header">
      <div>
        <button type="button">오늘</button>
        <button type="button">Salesgram</button>
      </div>
    </div>
    <!-- //header -->
    <!-- content -->
    <div id="content">
      <div class="visual"
        :class="{'on' : visual}"
      >
        <div>
          <img class="img01" src="~@/assets/images/img_home_tit01.png" alt="">
          <img class="img02" src="~@/assets/images/img_home_tit02.png" alt="">
          <div>
            <img class="img0301" src="~@/assets/images/img_home_tit03_01.png" alt="">
            <img class="img0302" src="~@/assets/images/img_home_tit03_02.png" alt="">
          </div>
          <img class="img04" src="~@/assets/images/img_home_tit04.png" alt="">
        </div>
      </div>
      <div class="productPick"
        :class="{'on' : productPick}"
      >
        <div>
          <p>Aliqua quis commodo elit sint dolor mollit. Elit incididunt et proident excepteur pariatur eu consequat id ex. Mollit elit consectetur ullamco qui exercitation magna reprehenderit do sint pariatur qui laborum culpa. Qui amet esse deserunt ullamco deserunt adipisicing duis quis proident. Duis esse do nostrud occaecat.

Pariatur proident irure nisi labore aute incididunt sunt culpa. Id eu ullamco Lorem esse laboris pariatur nostrud ullamco amet aliqua ullamco sit commodo tempor. Nisi fugiat anim commodo consequat laborum ad excepteur ipsum reprehenderit amet enim.

Irure officia aute nostrud tempor pariatur et incididunt. Nulla magna aliqua ea dolor culpa. In irure sint quis anim duis fugiat mollit esse laboris proident nulla veniam ea. Consequat laborum elit reprehenderit culpa qui. Fugiat occaecat enim laboris dolore excepteur amet et labore ipsum labore ullamco occaecat. Incididunt laborum ad quis sint anim qui ex velit irure dolore cupidatat sint minim ex. Culpa excepteur consectetur laborum consequat ad id veniam exercitation pariatur incididunt Lorem duis tempor.

Duis eu enim cupidatat ad adipisicing ut aliqua anim ea do et velit proident. Sint occaecat ad laboris anim et exercitation et qui in reprehenderit cillum ea magna mollit. Est ut aliquip culpa ex nulla pariatur dolor. Duis aliquip commodo sint dolor consectetur commodo id. Voluptate laborum quis consequat Lorem id cupidatat.

Nulla aliquip consequat aliqua adipisicing in elit. Eu commodo fugiat magna adipisicing Lorem eiusmod culpa ut esse dolore proident aliqua commodo adipisicing. Ea cupidatat ad do cillum elit cupidatat aliqua ullamco amet incididunt et irure. Duis voluptate amet incididunt labore sunt dolor elit proident est do laborum magna.

Eiusmod nostrud Lorem velit sunt id incididunt proident minim mollit id sit fugiat proident. Nostrud excepteur occaecat consectetur et ut ullamco veniam elit labore. Id commodo elit voluptate reprehenderit anim minim esse aliqua amet aliqua exercitation. Qui voluptate anim adipisicing occaecat eiusmod qui veniam aliquip culpa mollit mollit reprehenderit. Cupidatat incididunt sint consectetur exercitation consectetur tempor ex Lorem aliquip exercitation nisi. Exercitation cillum enim ullamco proident ad pariatur nisi amet.

Voluptate deserunt ut esse laborum. Commodo ex adipisicing magna mollit tempor laboris ullamco eu incididunt fugiat ipsum. Sunt cillum aute et officia incididunt laborum reprehenderit cupidatat et sunt pariatur.

Elit qui est non sit incididunt pariatur et anim nisi deserunt ut incididunt consequat. Aute cillum ad quis incididunt mollit culpa consectetur. Labore exercitation elit do excepteur mollit labore consequat Lorem dolor elit laborum. Irure incididunt reprehenderit amet ut est quis ullamco amet commodo cillum exercitation labore et nostrud.

Proident tempor occaecat consequat amet. Aute esse anim laboris nisi enim dolor eiusmod mollit velit do duis ipsum est. Dolor aliquip minim ex sit Lorem laborum elit eu cupidatat. Est duis dolore consectetur culpa consequat sint. Nostrud adipisicing laborum exercitation velit quis cillum sint do occaecat cillum id occaecat qui cillum. Reprehenderit quis ullamco consectetur id in aliquip enim qui nisi nisi irure elit. Amet fugiat mollit nulla Lorem nostrud anim consequat ea Lorem nulla do eiusmod tempor dolor.

Exercitation in sint aute eiusmod nostrud est commodo. Mollit occaecat deserunt aliquip magna voluptate magna nulla adipisicing reprehenderit enim sunt. Anim laboris veniam in in excepteur pariatur sit esse nisi anim elit elit. Sint irure qui quis nulla.</p>
        </div>
      </div>
    </div>
    <!-- //content -->
    <!-- searchBox -->
    <div id="searchBox"
      :class="{'on' : toastPopupToggle}"
    >
      <!-- searchInput -->
      <div class="searchInput">
        <div>
          <button type="button" @click="popupToggle()"></button>
          <input type="text" placeholder="찾으시는 태그를 입력해주세요." />
          <button type="button"></button>
        </div>
      </div>
      <!-- //searchInput -->
      <!-- searchResult -->
      <div class="searchResult">
        <p>Amet consectetur adipisicing consequat dolore enim deserunt incididunt nisi tempor cupidatat quis. Exercitation pariatur nulla labore culpa amet occaecat quis. Do ullamco labore deserunt sint minim occaecat duis enim sit deserunt excepteur deserunt culpa. Cillum Lorem duis consequat nostrud officia occaecat aute. Mollit reprehenderit culpa incididunt culpa irure reprehenderit dolore officia enim amet proident tempor. Adipisicing consectetur magna sit tempor pariatur sit. Cupidatat commodo magna cupidatat reprehenderit.

Exercitation cupidatat labore deserunt veniam reprehenderit sit consequat minim. Ullamco magna Lorem ut sit nulla nulla anim eiusmod cillum amet officia eiusmod reprehenderit amet. Voluptate adipisicing ullamco Lorem ut esse ipsum aliqua dolore. Tempor deserunt pariatur tempor ut ea pariatur dolore eu ad ea nulla. Minim velit consectetur laboris eiusmod do non.

Proident sint reprehenderit anim ex id voluptate officia voluptate labore do Lorem sit. Consectetur laborum enim sunt sit officia irure ipsum nisi eiusmod. Proident ullamco eu eiusmod consectetur sit adipisicing. Veniam non ullamco commodo excepteur ipsum anim reprehenderit id ullamco incididunt nostrud dolor magna elit.

Aliquip dolor ullamco sint sint. Labore deserunt excepteur Lorem incididunt aute id ipsum voluptate ullamco cillum laboris. Fugiat irure eu laboris in ea do deserunt id. Fugiat nisi nulla dolore qui nostrud voluptate adipisicing velit elit minim. Nostrud et eiusmod id veniam ad veniam quis eiusmod.

Ullamco culpa enim eiusmod laborum occaecat ea amet. Pariatur anim elit dolore officia et proident. Adipisicing dolore anim aliqua cillum amet ut. Aute irure tempor velit sunt esse. Eu eiusmod cillum anim enim aute. Deserunt amet reprehenderit adipisicing adipisicing. Cillum voluptate dolore aliqua officia quis.

Elit ut reprehenderit excepteur duis dolore et reprehenderit in excepteur deserunt nulla amet. Ullamco cupidatat sit ullamco labore ullamco. Eiusmod incididunt nostrud enim cupidatat nisi ut eu deserunt irure duis laborum aute.

Consequat reprehenderit amet fugiat sint do quis dolore in pariatur ullamco eu commodo sit. Ut exercitation enim do anim et. Laboris aliquip minim incididunt consequat dolore dolor anim quis.

Duis et non et magna minim. Ex pariatur occaecat cupidatat labore eiusmod et pariatur ex est. Consectetur laboris est anim velit aliquip nulla dolore eu. Officia ipsum nisi nostrud culpa nostrud eiusmod commodo proident adipisicing magna commodo eu amet ullamco. Id in ad elit ad nulla qui. Deserunt tempor non elit reprehenderit reprehenderit amet exercitation.

Cillum elit ex duis cillum ut sint dolore pariatur. Voluptate anim in proident amet anim proident exercitation tempor occaecat occaecat sint sunt cillum incididunt. Sint non voluptate tempor minim cupidatat dolore ipsum sunt anim Lorem dolor aliquip.

Aliquip cupidatat ea fugiat dolor pariatur do duis velit tempor culpa ad. Et commodo reprehenderit aliquip dolor ipsum mollit laboris quis eiusmod et laborum. Laborum Lorem duis nulla enim quis fugiat duis minim.</p>
      </div>
      <!-- //searchResult -->
    </div>
    <!-- //searchBox -->
    <transition name="popupDimmed" mode="out-in">
      <div id="popupDimmed"
        v-show="popupDimmed"
      ></div>
    </transition>
  </div>
</template>

<script>
export default {
  data(){
    return {
      visual: false,
      productPick: false,
      toastPopupToggle : false,
      popupDimmed : false,
    }
  },
  mounted(){
    setTimeout(() => {
      this.visual = true
    }, 1000);
  },
  methods:{
    popupToggle(){
      this.toastPopupToggle = !this.toastPopupToggle;
      this.popupDimmed = !this.popupDimmed;
    }
  },
}
</script>