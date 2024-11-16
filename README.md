# 前端学习案例 2——新闻页面制作

## 学习过程

主要根据黑马学习


## 难题处理过程

### 1. `<li>`标签前的小点

问题：  
如下图所示，新闻左端的标志不美观，且超出范围

![Q1Q1](https://github.com/user-attachments/assets/a2a78393-d25b-4916-a9dd-3d3e1fd2c871)


解决方案：  
通过对新浪新闻的网页进行研究，发现其并不使用列表自带的样式，而是选择在每个`<li>`标签中添加背景图。如下图所示：

<img width="428" alt="Q1A1" src="https://github.com/user-attachments/assets/fa1f948e-4406-4acc-865f-a2f8d4bad05f">


同样地，在本案例中也对每个`<li>`标签使用背景图，即可实现与新浪新闻相同的效果，如下图所示：

<img width="288" alt="Q1A2" src="https://github.com/user-attachments/assets/c96749a3-c520-4c18-831c-41f557a5d5f6">


所涉及到的代码如下：

```css
    .news .body li {
        background: url(./imgs/news_m_04.png) no-repeat -475px -616px;
        padding-left: 12px;
    }
```

### 2. 图片两端对齐

问题：  
在新闻内容中加入两张图片，两张图片的间距过小，且无法分别对其两侧，如下图所示：

![Q2Q1](https://github.com/user-attachments/assets/497bd766-ac23-4f62-861d-3357e11be8f4)

解决方法：  
通过询问 GPT，得知可以使用 flex 布局。修改后可实现目标效果。

<img width="280" alt="Q2A1" src="https://github.com/user-attachments/assets/249f6b1b-6cc9-4e40-8860-f2ff9b4258f8">


所涉及到的代码如下：

```css
    .news .images {
        display: flex;
        justify-content: space-between;
    }
```


## 遗留问题

### 1. 标题上方黑线及下方横线

如下图所示，放大网页后发现，标题上方黑线仍存在填充不满及下方横线问题。

![Q3Q1](https://github.com/user-attachments/assets/61576738-98d5-481b-9480-293eb7635da9)

