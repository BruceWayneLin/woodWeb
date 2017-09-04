<template>
  <div class="hello">
    <div class="row text-center">
      <div class="banner">
        <div class="logo">
        </div>
        <span class="logoSpan">林業試驗所   木材標本館</span>
      </div>
    </div>

    <div class="row">
      <div id="contentMaintain" class="container MenuContainer">
        <div class="col-xs-12 text-center">
          <ul class="nav nav-tabs">
            <li class="active"><a data-toggle="tab" href="#home">首頁</a></li>
            <li><a data-toggle="tab" href="#menu1">資料查詢</a></li>
            <li><a data-toggle="tab" href="#menu2">木材鑑定申請流程</a></li>
            <li><a data-toggle="tab" href="#menu3">聯絡我們</a></li>
          </ul>
          <div class="tab-content">
            <div id="home" class="tab-pane fade in active">
              <div class="col-xs-2">
                <ul class="leftMenu">
                  <li>menu1</li>
                  <li>menu2</li>
                  <li>menu3</li>
                  <li>menu4</li>
                </ul>
              </div>
              <div class="col-xs-10">
                <h3>林業試驗所   木材標本館</h3>
                <div class="content">
                  <img src="../../static/assets/css/img/wood.jpg" class="img-responsive" alt="">
                </div>
                <div class="content">
                  <p>
                    林業試驗所木材標本館之設立起源於民國34年存放之日據時代製作的30件大型木材標本，
                    民國73年大型木材標本典藏數增加至62件，為呈現木材不同切面的紋理而開始製作圓形的三切面標本207件，
                    並製作尺寸較小易於館藏之木材標本館藏於木材標本館中，供學術研究及教學使用，而大型標本、圓形三切面標本和54種竹材標本則在木材展示館展示，
                    提供國人認識木材之去處。
                  </p>
                </div>
                <div class="content">
                  <img src="../../static/assets/css/img/wood2.jpg" class="img-responsive" alt="">
                </div>
                <div class="content">
                  <p>
                    木材標本館目前館藏國產木材有58科134屬265種，其中針葉樹材有32種，4400片標本，闊葉樹材有233種，
                    27353片標本。蒐集國外產木材標本計含亞、美、歐、非及大洋洲等針葉樹材9科、40屬、218種，闊葉樹材163科、730屬、2,142種。
                  </p>
                </div>
              </div>
            </div>
            <div id="menu1" class="tab-pane fade">
              <div class="col-xs-2">
                <ul class="leftMenu">
                  <li>menu1</li>
                  <li>menu2</li>
                  <li>menu3</li>
                  <li>menu4</li>
                </ul>
              </div>
              <div class="col-xs-10">
                <h3>資料查詢</h3>
                <div class="marginTop">
                  <div class="form-group text-left">
                    <label for="subject">科名</label>
                    <input id="subject" type="text" class="form-control" placeholder="請輸入您要查詢的科名">
                  </div>
                  <div class="form-group text-left">
                    <label for="object">屬名</label>
                    <input id="object" type="text" class="form-control" placeholder="請輸入您要查詢的屬名">
                  </div>
                  <div class="form-group text-left">
                    <label for="kind">種名</label>
                    <input id="kind" type="text" class="form-control" placeholder="請輸入您要查詢的種名">
                  </div>
                  <div class="form-group text-left">
                    <button class="form-control btn-primary btn btn-sm">
                    <span class="glyphicon glyphicon-search" aria-hidden="true">
                      搜尋
                    </span>
                    </button>
                  </div>
                </div>
              </div>
            </div>
            <div id="menu2" class="tab-pane fade">
              <div class="col-xs-2">
                <ul class="leftMenu">
                  <li>menu1</li>
                  <li>menu2</li>
                  <li>menu3</li>
                  <li>menu4</li>
                </ul>
              </div>
              <div class="col-xs-10">
                <h3>木材鑑定申請流程</h3>
                <div>
                  <b-table striped hover
                           :items="items"
                           :current-page="currentPage"
                           :per-page="perPage"
                           :filter="filter"
                           :sort-by.sync="sortBy"
                           :sort-desc.sync="sortDesc"
                  ></b-table>
                </div>
                <div class="row">
                  <div class="col-xs-12 text-center">
                    <b-pagination :total-rows="totalRows" :per-page="perPage" v-model="currentPage" />
                  </div>
                </div>
              </div>
            </div>
            <div id="menu3" class="tab-pane fade">
              <div class="col-xs-2">
                <ul class="leftMenu">
                  <li>menu1</li>
                  <li>menu2</li>
                  <li>menu3</li>
                  <li>menu4</li>
                </ul>
              </div>
              <div class="col-xs-10">
                <h3>聯絡我們</h3>
                <div class="marginTop">
                  <div>
                    <div class="form-group text-left">
                      <label for="nameSub">名稱</label>
                      <input id="nameSub" type="text" class="form-control" placeholder="請輸入您的名稱">
                    </div>
                    <div class="form-group text-left">
                      <label for="tel">電話</label>
                      <input id="tel" type="text" class="form-control" placeholder="請輸入您的電話">
                    </div>
                    <div class="form-group text-left">
                      <label for="email">信箱</label>
                      <input id="email" type="text" class="form-control" placeholder="請輸入您的信箱">
                    </div>
                    <div class="form-group text-left">
                      <label for="comment">意見說明</label>
                      <textarea class="form-control" rows="5" id="comment"></textarea>
                    </div>
                    <div class="form-group text-left">
                      <button class="form-control btn-primary btn btn-sm">
                      <span class="glyphicon glyphicon-send" aria-hidden="true">
                        送出
                      </span>
                      </button>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import BootstrapVue from 'bootstrap-vue'
  import vue from 'vue'
  vue.use(BootstrapVue)
  const items = [
    { 申請者姓名: '申請者1',  申請狀態: '申請狀態', 申請日期: '2017-07-01'},
    { 申請者姓名: '申請者2',  申請狀態: '申請狀態', 申請日期: '2017-07-08'}
  ];
  export default {
  name: 'hello',
  components: {
  },
  data () {
    return {
      items: items,
      currentPage: 1,
      perPage: 5,
      totalRows: items.length,
      pageOptions: [{text:5,value:5},{text:10,value:10},{text:15,value:15}],
      sortBy: null,
      sortDesc: false,
      filter: null,
      modalDetails: { index:'', data:'' }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .banner {
    height: 310px;
    width: 100%;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
  }
  .logo {
    height: 70%;
    width: auto;
    background-repeat: no-repeat;
    background-position: left;
    position: relative;
    top: 60px;
    left: 30%;
    background-size: 10%;
  }
  .MenuContainer {
    margin-top: 30px;
    min-height: 800px;
  }
  #home p {
    text-align: left;
  }
  #home .content {
    margin: 0 auto;
    font-size: 16px;
    background-color: rgba(245, 245, 220, 0.73);
    padding: 10px 30px;
  }
  #home img {
    padding: 3% 10%;
    position: relative;
    top: 15px;
  }
  .table-hover {
    margin-top: 30px;
  }
  .marginTop {
    margin-top: 30px;
  }
  #contentMaintain {
  }
  .logoSpan {
    font-size: 40px;
    position: relative;
    top: -65px;
    left: 5%;
    border-bottom: 1px solid #334556;
  }
  .leftMenu {
    list-style-type: none;
    overflow: hidden;
    position: relative;
    top: 55px;
    font-size: 18px;
    line-height: 40px;
    background-color: rgba(245, 245, 220, 0.73);
    padding-left: 0px;
  }
  .leftMenu li {
    border-bottom: 1px solid white;
    font-weight: bold;
    cursor: pointer;
  }
  @media screen and (max-width: 1200px) {
    .logo {
      left: 20%!important;
    }
    .logoSpan {
      font-size: 30px;
    }
  }
</style>
