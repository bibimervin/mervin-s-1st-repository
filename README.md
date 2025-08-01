<!DOCTYPE html>
<html lang="zh">
<head>
  <meta charset="UTF-8">
  <title>Mervin的小宇宙 ✨</title>
  <style>
    body {
      font-family: '微软雅黑', sans-serif;
      background-color: #fef7ff;
      margin: 0;
      padding: 20px;
      color: #333;
    }
    .container {
      max-width: 700px;
      margin: auto;
      background: white;
      border-radius: 15px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      padding: 30px;
    }
    img {
      width: 100%;
      border-radius: 10px;
    }
    .thought {
      margin-top: 20px;
      font-size: 1.2em;
    }
    .like-btn {
      margin-top: 20px;
      background: pink;
      border: none;
      padding: 10px 20px;
      font-size: 1em;
      border-radius: 20px;
      cursor: pointer;
    }
    .comments {
      margin-top: 30px;
    }
    textarea {
      width: 100%;
      height: 60px;
      font-size: 1em;
      padding: 10px;
      border-radius: 10px;
    }
    .submit {
      margin-top: 10px;
      background: lavender;
      border: none;
      padding: 8px 16px;
      border-radius: 10px;
      cursor: pointer;
    }
    .comment-list {
      margin-top: 20px;
      font-size: 0.95em;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>🌸 Mervin的小想法</h2>
    <img src="your-photo.jpg" alt="你的小照片">
    <div class="thought">今天的心情：喜欢棉花糖一样轻飘飘的晚风～🌬️</div>

    <button class="like-btn" onclick="likeIt()">❤️ 喜欢这条想法 (<span id="count">0</span>)</button>

    <div class="comments">
      <h3>🗨️ 留言板</h3>
      <textarea id="comment" placeholder="说点什么吧~"></textarea>
      <br>
      <button class="submit" onclick="submitComment()">发表</button>
      <div class="comment-list" id="commentList"></div>
    </div>
  </div>

  <script>
    let count = 0;
    function likeIt() {
      count++;
      document.getElementById("count").innerText = count;
    }

    function submitComment() {
      const comment = document.getElementById("comment").value;
      if (comment.trim() !== "") {
        const commentBox = document.createElement("div");
        commentBox.innerText = "🧸 访客留言：" + comment;
        document.getElementById("commentList").appendChild(commentBox);
        document.getElementById("comment").value = "";
      }
    }
  </script>
</body>
<div id="cusdis_thread"
  data-host="https://cusdis.com"
  data-app-id="a6fa5b39-702f-4e34-8d36-43e90eab2437"
  data-page-id="mervin-home"
  data-page-url="http://localhost:5500/index.html"
  data-page-title="Mervinbibo's home"
></div>
<script async defer src="https://cusdis.com/js/cusdis.es.js"></script>

</html>
