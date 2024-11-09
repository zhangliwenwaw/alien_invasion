# 外星人入侵游戏
目录
1. 外星人入侵：使用 Python 开发游戏

2. 项目规划

3. pygame 模块常用函数

4. 设计流程

1. 外星人入侵：使用 Python 开发游戏
将使用 Pygame 包来开发一款 2D 游戏，它在玩家每消灭一群向下移动的外星人后，都将玩家提高一个等级；而等级越高，游戏的节奏越快，难度越大。完成这个项目后，你将获得自己动手使用 Pygame 开发 2D 游戏所需的技能。

2. 项目规划
在游戏《外星人入侵》中，玩家控制着一艘最初出现在屏幕底部中央的飞船。玩家可以使用箭头键左右移动飞船，还可使用空格键进行射击。游戏开始时，一群外星人出现在天空中，他们在屏幕中向下移动。玩家的任务是射杀这些外星人。玩家将所有外星人都消灭干净后，将出现一群新的外星人，他们移动的速度更快。只要有外星人撞到了玩家的飞船或到达了屏幕底部，玩家就损失一艘飞船。玩家损失三艘飞船后，游戏结束。

3. pygame 模块常用函数
函数名	作用
pygame.init()	初始化背景设置
screen = pygame.display.set_mode((1200, 600))	设置显示窗口大小
pygame.display.set_caption('Alien Invasion')	设置标题
pygame.event.get()	捕获键盘鼠标事件
screen.fill(bg_color)	设置背景色
pygame.display.flip()	刷新窗口，让最近绘制的屏幕可见
self.screen_rect = self.screen.get_rect()	获取对象外接矩形
self.image = pygame.image.load('images/ship.bmp')	加载图片
self.screen.blit(self.image, self.rect)	放置图像至指定的位置
4. 设计流程
4.1 基于Pygame 的基本框架
  pygame.init()
  pygame.display.set_caption('Alien Invasion')
  screen = pygame.display.set_mode((ai_setting.screen_height, ai_setting.screen_width))
4.2 设计实现飞船模块
link: ship.py

4.3 设计实现子弹模块
link: bullet.py

4.3 设计实现外星人模块
在该环节，我们将在游戏《外星人入侵》中添加外星人。

首先，我们在屏幕上边缘附近添加一个外星人，然后生成一群外星人。我们让这群外星人向两边和下面移动，并删除被子弹击中的外星人。
最后，我们将显示玩家拥有的飞船数量，并在玩家的飞船用完后结束游戏。
link: alien.py

4.4 记分系统
在本章中，我们将结束游戏《外星人入侵》的开发。我们将添加一个Play按钮，用于根据需要启动游戏以及在游戏结束后重启游戏。我们还将修改这个游戏，使其在玩家的等级提高时加快节奏，并实现一个记分系统。阅读本章后，你将掌握足够多的知识，能够开始编写随玩家等级提高而加大难度以及显示得分的游戏。
