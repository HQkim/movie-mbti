<template>
  <div class="">
    <div class="blog block">
        <div id="post-custom" class="post-content bg-light">
            <div class="post-meta">
                <p class="text-sm"><i class="far fa-user text-primary mr-1"></i> {{ article.user.username }} <i class="far fa-bookmark text-primary ml-3 mr-1"></i> {{ article.user.mbti }} <i class="far fa-clock text-primary ml-3 mr-1"></i> {{$moment(article.updated_at).format('YYYY-MM-DD')}} </p>
            </div><!-- / post-meta -->
            <h4 class="post-title"><a @click="moveToDetail" href="">{{ article.title }}</a></h4>
            <h5 class="mb-3">{{ article.movie_title }}</h5>
            <!-- <p class="mb-3">{{ article.content }}</p> -->
            <p class="comments-info text-sm mt-1 mb-2"><i class="far fa-comment text-primary mr-1"></i> ({{ article.comments.length }}) COMMENTS</p>
        </div><!-- / post-content -->
    </div><!-- / blog-block -->

    <div class="spacer">&nbsp;</div>    
  </div>
</template>

<script>
export default {
  name: 'ArticleListItem',
  props: {
    article: {
      type: Object,
    }
  },
  methods: {
    moveToDetail: function (event) {
      event.preventDefault()
      // this.$router.push({ name: 'ArticleDetail', params: { articleId: this.article.id, article: this.article} })]
      // console.log(typeof(this.article.id))
      this.$router.push({ name: 'ArticleDetail', params: { articleId: this.article.id } })
    }
  }
}
</script>

<style>
#post-custom {
  background-color: #E4E4E4 !important;
}
</style>