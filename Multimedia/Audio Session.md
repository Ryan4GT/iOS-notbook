### Audio Session默认行为

* 默认允许播放，不允许录制；
* 当用户讲响铃/静音开关移动到静音的位置时，你的音频也会静音。
* 当你的音频开始播放时，设备上的其他音频，比如正在播放的音乐应用的音频就会被静音

当你开始播放和录制音频的时候Audio Session自动开始；然而对于应用来说。然而依赖默认的状态，对应用来说有一定的风险。比如，如果iPhone响铃，用户忽略了来电，使你的应用继续运行，基于你所使用的播放技术，你的音频可能不再播放。

只有在以下情况，你才可以安全地忽略Audio Session:
* 当你在使用`System Sound Service` 或者 UIKit 的 `playInputClick`方法而不使用其他Audio API处理音频的时候，

* 你的应用不适用音频