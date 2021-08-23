<template>
  <div class="content-recharge">
    <div class="recharge-header">
      <div class="row">
        <div class="col-md-3 col-lg-3 header-left payment-header">
          <span><b>Lịch sử</b></span>
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
            <div class="row gr-transaction">
              <div class="col-lg-2 col-md-2 gr-item-ma">
                <div class="form-group grItem">
                  <label for="lblTransactionType">Loại giao dịch:</label>
                  <select
                    class="form-select"
                    aria-label="Default select example"
                  >
                    <option selected>--Tất cả--</option>
                    <option value="1">Giao dịch 1</option>
                    <option value="1">Giao dịch 2</option>
                    <option value="1">Giao dịch 3</option>
                    <option value="1">Giao dịch 4</option>
                  </select>
                </div>
              </div>
              <div class="col-lg-2 col-md-2 gr-item-ma">
                <div class="form-group grItem">
                  <label for="lblStatus">Trạng thái:</label>
                  <select
                    class="form-select"
                    aria-label="Default select example"
                  >
                    <option selected>--Tất cả--</option>
                    <option value="1">Trạng thái 1</option>
                    <option value="1">Trạng thái 2</option>
                    <option value="1">Trạng thái 3</option>
                    <option value="1">Trạng thái 4</option>
                  </select>
                </div>
              </div>
              <div class="col-lg-1 col-md-1 gr-item-ma">
                <div class="form-group grItem">
                  <label for="lblChannnelTransaction">Kênh giao dịch:</label>
                  <select
                    class="form-select"
                    aria-label="Default select example"
                  >
                    <option selected>--Tất cả--</option>
                    <option value="1">Kênh giao dịch 1</option>
                    <option value="1">Kênh giao dịch 2</option>
                    <option value="1">Kênh giao dịch 3</option>
                    <option value="1">Kênh giao dịch 4</option>
                  </select>
                </div>
              </div>
              <div class="col-lg-2 col-md-2 gr-time">
                <label for="lblChannnelTime">Thời gian:</label>
                <div class="row">
                    <div class="col-lg-5 col-md-5">
                        <date-picker ref="txtStartDate" v-model="startDateNow" :class="'data-input'" :editable="false" format="DD/MM/YYYY"></date-picker>
                    </div>
                    <div class="col-lg-1 col-md-1">
                      <i class='fas fa-angle-right arrow-date'></i>
                    </div>
                    <div class="col-lg-5 col-md-5">
                        <date-picker ref="txtEndDate" v-model="endDateNow" :class="'data-input'" :editable="false" format="DD/MM/YYYY"></date-picker>
                    </div>
                  </div>
              </div>
              <div class="col-lg-2 col-md-2 gr-time">
                <label for="lblEmployeeName">Nhân viên:</label>
                  <input
                        type="text"
                        class="form-control"
                        id="txtEmployeeName"
                        placeholder="Tên nhân viên giao dịch..."
                  />
              </div>
              <div class="col-lg-3 col-md-3 gr-time">
                <label for="lblAccount">Tài khoản:</label>
                  <div class="row">
                    <div class="col-lg-9 col-md-9">
                      <input
                        type="text"
                        class="form-control"
                        id="txtAccountNumber"
                        placeholder="Số tài khoản..."
                      />
                    </div>
                    <div class="col-lg-3 col-md-3">
                          <button class="search-button-top search-button btn btn-secondary" type="button">
                          <i class="fa fa-search"></i><span></span>
                        </button>
                    </div>
                  </div>
              </div>
            </div>
            <div class="row gr-download">
              <div class="col-lg-10 col-md-10">

              </div>
              <div class="col-lg-2 col-md-2 gr-download-btn">
                <button class="download-button btn btn-secondary" type="button">
                    <i class="fa fa-download" aria-hidden="true"></i><span>Tải Excel file</span>
                </button>
              </div>
            </div>
            
            <div class="form-group grItem">
              <div class="transaction-info-detail">
                <div class="row">
                  <div class="col-lg-12 col-md-12">
                    <div class="table-responsive">
                      <table class="table table-striped">
                        <thead>
                          <tr>
                            <th scope="col" class="header-invoice">STT</th>
                            <th scope="col" class="header-invoice">CH</th>
                            <th scope="col" class="header-invoice">Tên NV giao dịch</th>
                            <th scope="col" class="header-invoice">Số tài khoản</th>
                            <th scope="col" class="header-invoice">Ngày giao dịch</th>
                            <th scope="col" class="header-invoice">Loại giao dịch</th>
                            <th scope="col" class="header-invoice">Mã giao dịch</th>
                            <th scope="col" class="header-invoice">Số tiền</th>
                            <th scope="col" class="header-invoice">Phí</th>
                            <th scope="col" class="header-invoice">Nhà cung cấp</th>
                            <th scope="col" class="header-invoice">Kênh giao dịch</th>
                            <th scope="col" class="header-invoice">Trạng thái</th>
                            <th scope="col" class="header-invoice">Nội dung</th>
                            <th scope="col" class="header-invoice">Thao tác</th>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <td scope="row">1</td>
                            <td>PTO0307.353.Tân Thành</td>
                            <td>Phạm Thị Bích Ngọc</td>
                            <td>0987469090</td>
                            <td>18-08-2021 19:58:43</td>
                            <td>Nạp tiền</td>
                            <td>2108181957578731435</td>
                            <td><span class="monney">+500.000</span></td>
                            <td class="fee">0</td>
                            <td class="">NCC001</td>
                            <td class="">POS</td>
                            <td class=""><span class="alert alert-success status" role="alert">Thành công</span></td>
                            <td class="">1</td>
                            <td class="gr-button">
                              <button class="detail-button btn btn-secondary" type="button">
                                <i class="fa fa-search"></i><span>Chi tiết</span>
                              </button>
                              <button class="cancel-button btn btn-secondary" type="button">
                                <i class="fa fa-search"></i><span>Hủy</span>
                              </button>
                            </td>
                          </tr>
                        </tbody>
                      </table>
                    </div>
                  </div>
                </div>
                <div class="row pagination_area">
                  <div class="row">
                    <div class="col-lg-3 col-md-3">
                      <p>
                        Hiển thị <span class="numPage">1 - 10 </span>trong
                        <span class="numPage"> 56 </span>bản ghi
                      </p>
                    </div>
                    <div class="col-lg-3 col-md-3"></div>
                    <div class="col-lg-6 col-md-6 pag-group">
                      <ul class="pagination">
                        <li><a href="#" class="disabled" :disabled="true"><span class="firstPage">Trang đầu</span></a></li>
                        <li><a href="#"><i class='fas fa-angle-left'></i></a></li>
                        <li><a href="#">1</a></li>
                        <li><a class="active" href="#">2</a></li>
                        <li><a href="#">3</a></li>
                        <li><a href="#">4</a></li>
                        <li><a href="#">5</a></li>
                        <li><a href="#">6</a></li>
                        <li><a href="#">7</a></li>
                        <li><a href="#"><i class='fas fa-angle-right'></i></a></li>
                        <li><a href="#"><span class="lastPage">Trang cuối</span></a></li>
                      </ul>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </form>
          
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import DatePicker from 'vue2-datepicker';
import 'vue2-datepicker/index.css';

export default {
  name: "ReportTransaction",
  components: {DatePicker },
  props: {
    msg: String,
  },
  data() {
    return {
        startDateNow: new Date(),
        endDateNow: new Date(),
    };
  },
  methods: {
    
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../styles/color.scss";
@import "../styles/transaction.scss";

.menu-left ul li {
    margin-right: 20px;
}


</style>
<style>
.mx-datepicker .mx-input {
    height: 38px;
    text-align: center;
}
</style>