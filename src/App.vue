<template>
  <div class="container" id="app">
    <div class="header">
      <ul class="nav nav-pills float-right">
        <li class="nav-item">
          Hi, 
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
        <textarea class="form-control" id="tweetContent"></textarea>
      </div>
      <hr class="my-4">
      <p>{{ msg }}</p>
      <p>
        <button type="button" class="btn btn-primary btn-sm">发布</button>
      </p>
    </div>

    <div class="row marketing">
      <div id="tweets">
        <h6>Title</h6>
        <p>Content</p>
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
      msg: 'Welcome to Pycon-Tweets'
    }
  }
}
</script>
