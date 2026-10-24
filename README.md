# MP3 粒子播放器 · GitHub Pages

把本文件夹里面的文件上传到 GitHub 仓库根目录：`index.html` 和 `assets/`。这份发布包不包含 Nova 对话后台、密钥或私人数据库。

请把你要发布的素材放入 assets，并使用以下文件名（注意大小写）：

- `assets/audio.mp3`：你的音频。
- `assets/subtitles.srt`：带时间轴、UTF-8 编码的字幕。也可使用 LRC/VTT/TXT，但要同步修改 HTML 末尾的 PLAYER_ASSETS.subtitles 路径。普通 TXT 没有时间轴，会使用每句时长轮播。
- `assets/background.jpg`：你的背景。PNG/WebP 等也可以，同步修改 PLAYER_ASSETS.background 路径即可。

默认路径集中在 index.html 里的 `PLAYER_ASSETS`，使用相对路径，适合 GitHub Pages 的仓库子路径。不要给路径开头加 `/`。不需要某项时把对应值改为 `''`。

素材没有包含在这个文件夹：此前在浏览器选择的 MP3 和背景不会自动变成服务器文件，需要你放入上述位置再上传。

GitHub 仓库 Settings → Pages → Deploy from a branch → 选择 main 和 /(root)，保存后打开 GitHub 给出的 Pages 网址。普通 GitHub 文件浏览地址不是播放器网址。公开仓库的素材也会公开，请只上传可公开的内容。超过 GitHub 单文件大小限制的音频需压缩或改用合适的文件托管。

页面会自动加载音频、字幕和背景，但不会强制自动出声；手机通常要点一次播放。第一次加载时进度条等待音频元数据，之后可用鼠标或手指拖到任意位置；拖动时字幕同步预览。键盘聚焦进度条后，也可用左右方向键调整。

右下角划线眼睛按钮隐藏所有操作界面，仅保留粒子、字幕与背景。点击画面或按 Esc 恢复，也可按 H 隐藏/恢复。它与设置中的“自动隐藏操作按钮”相互独立。

缺少某项素材时，设置里会显示原因，并保留手动上传功能。双击本地 HTML 时，浏览器可能阻止自动读取字幕；请使用 GitHub Pages 或本机 HTTP 服务测试。音频识别仍在本机执行，仅首次下载识别程序与模型。
