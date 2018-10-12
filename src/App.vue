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
        <button type="button" class="btn btn-primary btn-sm">发布</button>
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
  }
}
</script>
