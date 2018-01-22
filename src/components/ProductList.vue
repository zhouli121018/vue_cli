<template>
  <div>
      <div class="right_col" role="main">
      <div class="row">
        <div class="col-xs-12 x_title">
          <h3>笔记本商品列表</h3>
        </div>
      </div>
      <div class="row">
        <div class="col-xs-3">
          <form class="form-inline">
            <div class="form-group">
              <label for="page-size">每页显示记录数：</label>
              <select class="form-control" id="page-size">
                <option value="10">10</option>
                <option value="20">20</option>
                <option value="40">40</option>
                <option value="60">60</option>
                <option value="80">80</option>
                <option value="100">100</option>
              </select>
            </div>
          </form>
        </div>
        <div class="col-xs-4 col-xs-offset-5">
          <div class="form-group has-feedback">
            <label for="product-kw" class="sr-only">搜索关键字：</label>
            <input class="form-control" type="text" id="product-kw" placeholder="请输入搜索关键字">
            <span class="glyphicon glyphicon-search form-control-feedback"></span>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-xs-12">
          <div class="table-responsive">
            <table class="table table-hover table-striped" id="table-laptop">
              <thead>
              <tr>
                <th>
                  <div class="checkbox" style="margin: 0;">
                    <label>
                      <input type="checkbox">全选
                    </label>
                  </div>
                </th>
                <th>编号</th>
                <th>图片</th>
                <th>型号</th>
                <th>主标题</th>
                <th>规格</th>
                <th>单价</th>
                <th>操作</th>
              </tr>
              </thead>
              <tbody>
              <tr>
                <td colspan="8">
                  <div class="loading">
                    <img src="../assets/img/loading.gif" alt="">
                  </div>
                </td>
              </tr>
              </tbody>
            </table>
          </div>
          <div class="row">
            <div class="col-xs-12">
              <ul class="pagination pull-right" id="pagination">
                <li><a href="#">上一页</a></li>
                <li><a href="#">1</a></li>
                <li><a href="#">2</a></li>
                <li class="active"><a href="#">3</a></li>
                <li><a href="#">4</a></li>
                <li><a href="#">5</a></li>
                <li><a href="#">下一页</a></li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <br>
    </div>
  </div>
</template>
<script>
export default {
  data:function(){
      return {
          msg:'Hello ProductList'
      }
  }
}
</script>
<style>

</style>


