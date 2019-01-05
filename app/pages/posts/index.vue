<template>
  <section class="container posts-page">
    <el-card style="flex: 1">
      <div slot="header" class="clearfix">
        <span>新着投稿</span>
      </div>
      <el-table
        :data="showPosts"
        style="width: 100%"
        class="table"
      >
        <el-table-column
          prop="title"
          label="タイトル">
        </el-table-column>
        <el-table-column
          prop="user.id"
          label="投稿者"
          width="180">
        </el-table-column>
        <el-table-column
          prop="created_at"
          label="投稿日時"
          width="240">
        </el-table-column>
      </el-table>
    </el-card>
  </section>
</template>

<script>
export default {
  computed: {
    showPosts() {
      return [
        {
          id: '001',
          title: 'Signalize!',
          body: 'Hi, signalize! 答はもっと高い空の彼方 いいえ違うよ 僕の目にも見えた地の果て',
          created_at: '2018/08/10 12:00:00',
          user: {
            id: 'xKxAxKx'
          }
        },
        {
          id: '002',
          title: 'Trap of Love',
          body: 'コドモだっていうには 複雑すぎるこの胸は切なくて はじけてしまいそう「何処かへ 連れ出して?」',
          created_at: '2018/08/10 12:00:00',
          user: {
            id: 'xKxAxKx'
          }
        },
      ]
    }
  }
}
</script>
