# 自定义视频播放器项目

该项目实现了一个基于 HTML5 和原生 JavaScript 的自定义视频播放器，提供了灵活的控制方式和良好的用户体验。

## 核心组件

1. **播放器初始化**：通过传入视频元素和自定义配置选项，创建 `Player` 类实例。动态生成的控制界面与视频元素紧密结合，提供了灵活的控制选项。
   
2. **自定义控件**：完全自定义控件，控制播放器的外观和交互行为，例如播放/暂停按钮、音量调节、进度条等。
   
3. **事件监听器**：自动监听媒体播放相关的事件，如 `play`、`pause`、`timeupdate` 等，实时更新控件状态。

4. **全屏功能**：支持通过 `requestFullScreen` 和 `exitFullscreen` 方法自由切换全屏播放模式。

## 主要功能

- **自定义控制栏**：可定制的按钮和滑动条，控制视频播放、音量调节和进度。
- **全屏支持**：一键进入或退出全屏模式，提升观影体验。
- **音量控制**：滑动调节音量，可一键静音。
- **播放速度调整**：支持 1.0x 到 2.0x 的播放速度选择。
- **进度条控制**：支持拖动进度条快进或倒退，并实时显示播放进度。
- **事件处理**：播放器自动监听并处理媒体事件，确保控件与播放状态同步。

## 使用说明

### 第一步：引入播放器脚本

在 HTML 文件中引入 `player.js` 脚本：

```html
<script src="path/to/player.js"></script>
```

### 第二步：添加视频元素

在 HTML 中添加一个视频元素，并赋予唯一的 `id`：

```html
<video id="myVideo" width="640" height="360" src="path/to/video.mp4"></video>
```

### 第三步：初始化播放器

通过 JavaScript 初始化播放器，并传入自定义选项：

```javascript
var player = new Player('myVideo', {
    autoplay: false,
    muted: false,
    currentTime: 0,
    width: 640,
    height: 360
});
```

### 第四步：根据需要自定义

可以传入不同的选项来自定义播放器的行为，例如设置视频源、是否自动播放、是否静音等：

```javascript
var player = new Player('myVideo', {
    source: 'path/to/video.mp4',
    poster: 'path/to/poster.jpg',
    autoplay: true,
    muted: true
});
```

### 第五步：处理播放事件

使用 `on` 方法监听播放器事件，执行自定义逻辑：

```javascript
player.on('play', function() {
    console.log('视频开始播放');
});

player.on('pause', function() {
    console.log('视频已暂停');
});
```

---

这个 README 文件概述了如何使用项目中的自定义视频播放器组件，包括初始化、控件自定义、事件监听等关键功能。
