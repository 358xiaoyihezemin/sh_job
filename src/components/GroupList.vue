/**
* Created by 鬼谷中妖 on 2017/7/26.
* QQ: 562550212
* PC端用于显示各群群号
* updated by 王冬 2017/08/01 删除了中高级群及管理群群号，把开发者添加进来
*/
<template>
  <div class="sh-sidebar groups">
    <h2>前端各群及群号</h2>
    <table>
      <tr v-for="group in groups" v-bind:key="group.id">
        <td>{{group.groupName}}</td><td>{{group.groupID}}</td>
      </tr>
    </table>
  </div>
</template>

<style lang="less" scoped type="text/less">
  .sh-sidebar {
    position: fixed;
    top: 155px;
    right: 40px;
    h2 {
      font-size: 24px;
      text-align: center;
      line-height: 1.8;
    }
  }
  table {
    border: 2px solid rgb(238, 238, 238);
    background-color: #fff;
    tr:nth-child(odd) td{
      background-color: #fafafa;
    }
    td {
      padding: 10px;
      border: 2px solid rgb(238, 238, 238);
    }
  }
  @media screen and (max-width: 1700px) {
    .sh-sidebar {
      display: none;
    }
  }
  @media screen and (max-width: 1820px) {
    .sh-sidebar {
      right: 0;
    }
  }
</style>

<script>
  export default {
    data () {
      return {
        groups: [
          {
            'groupID': '492107297',
            'groupName': 'JS前端开发跳板群'
          },
          {
            'groupID': '389875212',
            'groupName': 'JS初级前端开发群'
          },
          {
            'groupID': '327388215',
            'groupName': 'JS初级前端开发2群'
          },
          {
            'groupID': '请先加入跳板群',
            'groupName': 'JS中级前端开发群'
          },
          {
            'groupID': '请先加入跳板群',
            'groupName': 'JS高级前端开发群'
          }
        ],
        developer: '鬼谷中妖(woden0415@163.com)'
      }
    }
  }
</script>
