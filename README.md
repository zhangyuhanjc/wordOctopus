# wordOctopus

欢迎使用我们的背单词应用！我们的应用已包含四级词汇，后续还会更多！
这款应用将帮助您提高词汇量并轻松掌握英语。我们的应用程序提供了独特的背单词方式---单词卡，在单词卡中您将感受到短期多次记忆带来的快速学习体验！
我们的应用程序适用于学生和英语初学者！
快来下载我们的应用程序，开始学习英语吧！
https://apps.apple.com/app/wordoctopus/id6449214839

## 更新内容

2023.05.22
1.优化单词卡复习体验，为了更好的帮助用户整理单词卡，现在单词卡要录入6个词以上才能归档新建单词卡（不能一张纸只写一个词，要节约用纸啊）
2.优化抽卡体验，抽卡只抽取大于6个词的卡片（历史小于6个词的卡片将不会被复习）
3.添加首次启动App时的帮助引导， 帮助引导可在设置页重置 以重复观看
4.在设置页右下角增加app版本号



<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css" />

<!-- 使用Animate.css实现动态效果 -->
<h1 class="animate__animated animate__bounce">Hello, World!</h1>

<!-- 使用Canvas元素实现动态特效 -->
<canvas id="myCanvas"></canvas>

<script>
  const canvas = document.getElementById('myCanvas');
  const context = canvas.getContext('2d');
  let x = 0;
  let y = 0;
  let dx = 5;
  let dy = 5;

  function drawCircle() {
    context.clearRect(0, 0, canvas.width, canvas.height);
    context.beginPath();
    context.arc(x, y, 40, 0, 2 * Math.PI);
    context.fillStyle = 'blue';
    context.fill();

    if (x + dx > canvas.width || x + dx < 0) {
      dx = -dx;
    }

    if (y + dy > canvas.height || y + dy < 0) {
      dy = -dy;
    }

    x += dx;
    y += dy;
    
    // 递归绘制动画
    requestAnimationFrame(drawCircle);
  }

  drawCircle();
</script>
