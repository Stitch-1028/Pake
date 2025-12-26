#### Pake.json

```json
{
  "windows": [
    {
      "url": "https://192.168.110.130:8030/",
      "url_type": "web",
      "hide_title_bar": true,
      "fullscreen": false,
      "width": 600,
      "height": 780,
      "resizable": true,
      "always_on_top": false,
      "dark_mode": true,
      "activation_shortcut": "",
      "disabled_web_shortcuts": false,
      "hide_on_close": true,
      "incognito": false,
      "enable_wasm": false,
      "enable_drag_drop": false,
      "maximize": false,
      "start_to_tray": false,
      "force_internal_navigation": false
    }
  ],
  "user_agent": {
    "macos": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/18.2 Safari/605.1.15",
    "linux": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/133.0.0.0 Safari/537.36",
    "windows": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/133.0.0.0 Safari/537.36"
  },
  "system_tray": {
    "macos": false,
    "linux": true,
    "windows": true
  },
  "system_tray_path": "images/logo.png", // 当软件最小化后,以该图片显示在系统托盘(右下角的软件图标)
  "inject": [],
  "proxy_url": "",
  "multi_instance": false
}
```

#### tauri.window.conf.json

```json
{
  "bundle": {
    // 该图片应用在可执行文件本身 以及窗口图标
    "icon": ["images/logo_256.ico", "images/logo_32.ico"],
    "active": true,
    // 安装包资源路径
    "resources": ["images/logo_32.ico"],
    "targets": ["msi"],
    "windows": {
      "digestAlgorithm": "sha256",
      "wix": {
        "language": ["en-US"],
        "template": "assets/main.wxs"
      }
    }
  }
}
```
