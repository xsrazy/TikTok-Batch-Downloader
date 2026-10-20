

# 🎬 TikTok Batch Downloader (No Watermark)

🌐 Available in other languages: [Bahasa Indonesia](README.id.md)

![Node.js](https://img.shields.io/badge/Node.js-12%2B-green)
![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![Status](https://img.shields.io/badge/status-active-brightgreen)
![GitHub stars](https://img.shields.io/github/stars/xsrazy/TikTok-Batch-Downloader?style=social)
![GitHub forks](https://img.shields.io/github/forks/xsrazy/TikTok-Batch-Downloader?style=social)
![GitHub last commit](https://img.shields.io/github/last-commit/xsrazy/TikTok-Batch-Downloader)

---

A simple Node.js CLI tool to download multiple TikTok videos without watermarks, complete with metadata export and automatic error handling.

**Prefer the web version?** Use [TikBulk](https://tikbulk.xsrazy.web.id): the same bulk downloader in your browser, no install needed.

![Screen Shot!](xsrazy.png)

---

## 🚀 Features

- 🎥 Download TikTok videos without watermarks
- ⏳ Batch process using `links.txt`
- 📊 Metadata export (in JSON format)
- 🚫 Automatic error logging
- 📁 Clean folder structure

## 💡 How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/xsrazy/TikTok-Batch-Downloader
   cd TikTok-Batch-Downloader
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Add all video links to the `links.txt` file.

4. Run the tool:
   ```bash
   node main.js
   ```

---

## 📁 Output Structure
```
downloads/
├── video_1/
│   ├── video.mp4
│   └── metadata.json
├── video_2/
│   ├── video.mp4
│   └── metadata.json
...
```

### 🔍 Contents of `metadata.json`
Each video will come with a `metadata.json` file containing detailed information:

| Field            | Description                                        |
|------------------|----------------------------------------------------|
| `id`             | Unique ID of the TikTok video                      |
| `url`            | Full URL of the video                              |
| `author`         | Username (e.g., `@xsrazy`)                         |
| `description`    | Caption or text content of the video               |
| `hashtags`       | List of hashtags in the video (`#tag`)             |
| `music`          | Title or source of the audio                       |
| `created_at`     | Upload date of the video (ISO format)              |
| `stats.plays`    | Number of views                                    |
| `stats.likes`    | Number of likes                                    |
| `stats.comments` | Number of comments                                 |
| `stats.shares`   | Number of shares                                   |
| `downloaded_at`  | Time when the video was downloaded using this tool |

---

## 📋 Example of `links.txt`
```
https://www.tiktok.com/@user/video/1234567890123456789
https://www.tiktok.com/@anotheruser/video/9876543210987654321
```

---

## 🧩 How to Grab Video Links Easily 

No need to code — just use this Chrome extension:

🔗 [Link Grabber (by Google)](https://chromewebstore.google.com/detail/link-grabber/caodelkhipncidmoebgbbeemedohcdma)

**Steps:**

1. Open any TikTok page (profile, hashtag, FYP, etc.)
2. Click the Link Grabber icon
3. Copy all the video links shown
4. Paste them into the links.txt file

## 🧠 Tips
- Make sure the links are valid and the videos are public (not private)
- Avoid downloading thousands of videos at once (limit the batch size)
- Use it for archiving, educational purposes, or personal backups
- You can use a Link Grabber extension or a custom scraper to gather video links

## 💻 Created by
**[@xsrazy](https://github.com/xsrazy)** — open-source enthusiast  
Feel free to fork, star ⭐, and contribute!

## 📣 Release
🎉 **First Release:** `v1.0.0`
- TikTok downloader CLI without watermarks
- Batch processing
- JSON metadata export
- Duplicate detection and error logging

> Ready to use for content creators, video backups, or personal analysis!

## 🧾 [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE.md)

MIT License – see the [LICENSE](LICENSE) file for details.

---

<a href="https://www.buymeacoffee.com/xsrazy" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>