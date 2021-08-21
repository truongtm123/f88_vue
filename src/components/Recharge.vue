<template>
  <div class="content-recharge">
    <div class="recharge-header">
      <div class="row">
        <div class="col-md-6 col-lg-6 header-left payment-header">
          <span><b>Nạp tiền tại quầy</b></span>
        </div>
        <div class="col-md-6 col-lg-6 header-right payment-header">
          <span
            >Tổng đài gọi ra &amp; tổng đài tự động(voice call):
            <strong>Hotline hỗ trợ đối tác: (028) 73000406</strong></span
          >
        </div>
      </div>
    </div>
    <div class="recharge-content">
      <div id="content">
        <!-- progressbar -->
        <ProgressBar msg="test" />
        <form class="formRecharge">
          <div class="form-group grItem">
            <label for="lblChoiceService">Chọn dịch vụ:</label>
            <select class="form-select" aria-label="Default select example">
              <option selected></option>
              <option value="1">Ví MoMo</option>
              <option value="1">Ví MoMo</option>
              <option value="1">Ví MoMo</option>
              <option value="1">Ví MoMo</option>
              <option value="1">Ví MoMo</option>
            </select>
          </div>
          <div class="form-group grItem">
            <label for="lblAccountNum">Số tài khoản:</label>
            <input
              type="text"
              class="form-control"
              id="txtAccount"
              placeholder="Nhập số tài khoản..."
            />
          </div>
          <div class="form-group grItem seachr-button-gr">
            <button class="btn btn-secondary search-button" type="button">
              <i class="fa fa-search"></i><span>Tìm kiếm</span>
            </button>
          </div>
          <div class="form-group grItem">
            <div class="row gr-momo">
              <div class="col-lg-3 col-md-3">
                <div class="image_list">
                  <img
                    src="../assets/images/momo_bng.png"
                    class="img-momo"
                    alt="Momo"
                  />
                </div>
              </div>
              <div class="col-lg-9 col-md-9 menu-left">
                <div class="menu">
                  <ul>
                    <li>
                      <p>
                        Tên tài khoản:<span class="history"
                          ><i class="fas fa-history"></i
                          ><span><a href="">Lịch sử</a></span></span
                        >
                      </p>
                    </li>
                    <li><p>Số tài khoản:</p></li>
                    <li><p>Số điện thoại:</p></li>
                    <li><p>Email:</p></li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
          <div class="form-group grItemMoney">
            <label for="lblRechargeMoney">Số tiền nạp:</label>
          </div>
          <div class="input-group grItem formMoneyRecharge">
            <input
              type="text"
              class="form-control"
              aria-label="Số tiền nạp"
              placeholder="0..."
            />
            <div class="input-group-append">
              <span class="input-group-text money-payment">VNĐ</span>
            </div>
          </div>
          <div class="form-group grItem">
            <label for="lblRechargeContent">Nội dung nạp tiền:</label>
            <textarea
              class="form-control"
              id="exampleFormControlTextarea1"
              rows="5"
            ></textarea>
          </div>
          <div class="form-group comment-group">
            <label for="lblRechargeContent"
              ><span class="comment">Còn lại 160 ký tự</span></label
            >
          </div>
        </form>
        <div class="row gr-button">
          <div class="col-lg-4 col-md-4"></div>
          <div class="col-lg-4 col-md-4">
            <button type="button" class="btn btn-primary reset">
              Nhập lại
            </button>
            <button class="btn btn-secondary recharge-button" type="submit">
              <i class="fas fa-arrow-right"></i><span>Nạp tiền</span>
            </button>
          </div>
          <div class="col-lg-4 col-md-4"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ProgressBar from './ProgressBar.vue'
export default {
  name: "Recharge",
  components: {
    ProgressBar
  },
  props: {
    msg: String,
  },
  data() {
    return {};
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped >
/*For header */
.formRecharge {
  margin: 50px 0 0 10px;
}
.recharge-header {
  height: 50px;
  background-color: #f5f5f5;
  padding-top: 13px;
}
.header-left span {
  text-transform: uppercase;
  margin: 10px 0 0 10px;
}
.header-right {
  text-align: right;
}
.header-right span {
  margin: 0 10px 0 0;
}
/*End header */
/* Begin form */
.formRecharge label {
  margin: 0;
}
.seachr-button-gr {
  text-align: left;
}
.grItem {
  margin: 20px -10px 0 -10px !important;
  text-align: left;
}
.grItemMoney {
  margin: 20px -10px -20px -10px !important;
  text-align: left;
}
.grItemSearch {
  margin: 120px 0 40px 0 !important;
}
.search-button,
.search-button:hover,
.search-button:active,
.search-button:focus {
  background-color: #6495ed;
}
.search-button span {
  margin: 0 0 0 5px;
}
/* End form */
/*For momo icon */
.gr-momo {
  background-color: #f5f5f5;
  height: 250px;
  margin-left: 0px;
  margin-right: 0px;
}
.image_list {
  margin: 20px 0 0 20px;
}
.image_list img {
  width: 100%;
  height: 100%;
}
.menu-left {
  text-align: left;
  margin: 20px 0 0 0;
}
.menu ul {
  list-style: none;
}
.menu ul li {
  padding: 10px 0 0 0;
  border-bottom: 1px solid #a9a9a9;
}
.menu ul li p {
  font-size: 12px;
  font-style: normal;
  font-weight: bold;
  opacity: 0.7;
}
/*End for momo icon */

.reset {
  margin: 0 20px 0 0;
}

.content-recharge {
  background-color: white;
}
#content {
  text-align: center;
  position: relative;
  padding-top: 50px;
  min-height: 820px;
  max-width: 810px;
  margin: 0 auto;
  background: #ffffff;
  z-index: 1;
}

.comment {
  font-size: 11px;
  font-style: italic;
  color: #d8d8d8;
  margin-left: -10px;
  font-weight: normal;
}
.comment-group {
  text-align: left;
}
.gr-button {
  background-color: #f5f5f5;
  height: 80px;
  margin: 40px -10px 20px 0;
  padding-top: 20px;
}
.gr-button .reset {
  background-color: #dcdcdc;
  border: 2px solid #f6f9fb;
  color: black;
  font-size: 12px;
  opacity: 0.6;
  font-weight: bold;
}


.recharge-button,
.recharge-button:hover,
.recharge-button:active,
.recharge-button:focus {
  background-color: #3cb371;
}

.recharge-button span {
  margin: 0 0 0 5px;
}
.recharge-content {
  padding-bottom: 10px;
}
.history {
  margin: 0 0 0 10px;
  font-size: 9px;
  font-weight: bold;
  font-style: normal;
  color: #4682b4;
}
.history span {
  margin-left: 5px;
}
.history span a {
  text-decoration: none;
  color: #4682b4;
}
.history span a:hover {
  text-decoration: none;
  color: #4682b4;
}

.formMoneyRecharge {
  width: 820px;
}
.money-payment {
  font-size: 12px;
  font-style: normal;
  font-weight: bold;
  padding: 10px;
}
.payment-header span {
  opacity: 0.6;
}
</style>
