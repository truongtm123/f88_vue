<template>
  <div class="content-recharge">
    <div class="recharge-header">
      <div class="row">
        <div class="col-md-3 col-lg-3 header-left payment-header">
          <span><b>Thanh toán hóa đơn</b></span>
          <p>Số dư ví:<span class="vnd">+ VND</span></p>
        </div>
        <div class="col-md-9 col-lg-9 header-right payment-header">
          <span
            >Tổng đài gọi ra &amp; tổng đài tự động(voice call):
            <strong>Hotline hỗ trợ đối tác: (028) 73000406</strong></span
          >
        </div>
      </div>
    </div>
    <div class="recharge-content">
      <div class="row">
        <div class="col-lg-12 col-md-12">
            <form class="content">
                <div class="row">
                    <div class="col-lg-3 col-md-3">
                        <div class="form-group grItem">
                            <label for="lblChoiceService">Chọn dịch vụ:</label>
                            <select class="form-select" aria-label="Default select example">
                                <option selected>Lựa chọn...</option>
                                <option value="1">Dịch vụ 1</option>
                                <option value="1">Dịch vụ 2</option>
                                <option value="1">Dịch vụ 3</option>
                                <option value="1">Dịch vụ 4</option>
                            </select>
                        </div>
                    </div>
                    <div class="col-lg-4 col-md-4">
                        <div class="form-group grItem">
                            <label for="lblDivision">Đơn vị cung cấp:</label>
                            <select class="form-select" aria-label="Default select example">
                                <option selected>Lựa chọn...</option>
                                <option value="1">Đơn vị 1</option>
                                <option value="1">Đơn vị 2</option>
                                <option value="1">Đơn vị 3</option>
                                <option value="1">Đơn vị 4</option>
                            </select>
                        </div>
                    </div>
                    <div class="col-lg-5 col-md-5">
                        <div class="form-group grItem">
                            <label for="lblCustomerId">Mã khách hàng/ Hợp đồng</label>
                            <input
                            type="text"
                            class="form-control"
                            id="txtCustomerId"
                            placeholder="Nhập mã khách, số HĐ..."
                            />
                        </div>
                        <button class="search-button btn btn-secondary" type="button">
                            <i class="fa fa-search"></i><span></span>
                        </button>
                    </div>
                </div>

            </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PaymentInvoice",
  components: {
    
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
<style scoped lang="scss">
@import "../styles/color.scss";
@import "../styles/invoice.scss";
</style>
