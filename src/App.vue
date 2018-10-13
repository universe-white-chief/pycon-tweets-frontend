<template>
  <div class="container" id="app">
    <div class="header">
      <ul class="nav nav-pills float-right">
        <li class="nav-item">
          <div class="text-muted">Hi, {{username}}</div> 
        </li>
        <li>
          <a class="nav-link" href="#">Sign in</a>
        </li>
        <li>
          <a class="nav-link" href="#">Sign Out</a>
        </li>
      </ul>
      <h3 class="text-muted">Pycon-Tweets-😳</h3>
    </div>

    <div class="jumbotron">
      <div class="input-group">
        <textarea class="form-control" v-model="content" placeholder="最多140字"></textarea>
      </div>
      <hr class="my-4">
      <p>{{ msg }}</p>
      <p>
        <button type="button" class="btn btn-primary btn-sm" v-on:click="publish()">发布</button>
      </p>
    </div>

    <div class="row marketing">
      <div id="tweets">
        <div class="row marketing" v-for="tweet in tweets">
          <p>{{ tweet.content }} - {{ tweet.created_at }}</p>
        </div>
      </div>
    </div>

    <div class="footer">
      <p>♥ from the Pycon</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Pycon-Tweets',
      username: 'sddtc',
      tweets: [{"content":"晚安", "created_at":"2018-10-02"}, {"content":"早安", "created_at":"2018-10-01"}],
      content: ''
    }
  },
  methods: {
    publish: function() {
      var _this = this;
      if(!this.content) {
        console.log('请输入内容');
        return;
      }
      console.log('向后端服务器发送数据...', this.content);

      // var url = 'http://127.0.0.1:5000/'+this.username+'/tweet';
      // fetch(url,
      // {
      //   headers: { "Content-Type": "application/x-www-form-urlencoded" },
      //   method: "POST",
      //   body: "tweet_content=" + this.content,
      //   mode: 'no-cors'
      // })
      // .then(function(res){ _this.myTweets(); })
      // .catch(e => console.log("Oops, error", e));
    }
  }
}
</script>
