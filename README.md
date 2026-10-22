# TikTok Batch Downloader

A simple Node.js CLI tool to download multiple TikTok videos without a watermark, complete with metadata export and automatic error handling.

**Prefer the web version?** Use [TikBulk](https://tikbulk.xsrazy.web.id), the same bulk downloader in your browser, no install needed.

![Screenshot](xsrazy.png)

## About

TikTok Batch Downloader reads a list of TikTok video links from a plain text file and downloads every video in one run. Each download lands in its own folder together with a metadata file, so the result stays organized and easy to archive, back up, or analyze later.

## Features

- Downloads TikTok videos without a watermark, in HD when available
- Batch processing from a simple `links.txt` file, one link per line
- Metadata export to JSON for every downloaded video
- Automatic error logging, so one failed link never stops the whole batch
- Clean output structure, one folder per video

## How it works

1. The tool reads every link from `links.txt`
2. For each link, video data is fetched from the tikwm.com API
3. The video file is downloaded into its own folder under `downloads/`
4. A `metadata.json` file is written next to each video
5. Any error is logged and the batch continues with the next link

## Setup

1. Clone the repository:

```bash
git clone https://github.com/xsrazy/TikTok-Batch-Downloader
cd TikTok-Batch-Downloader
```

2. Install the dependencies:

```bash
npm install
```

3. Add your video links to `links.txt`, one per line:

```
https://www.tiktok.com/@user/video/1234567890123456789
https://www.tiktok.com/@anotheruser/video/9876543210987654321
```

4. Run the tool:

```bash
node main.js
```

Requires Node.js 12 or newer.

## Output

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

### Contents of metadata.json

| Field | Description |
| --- | --- |
| `id` | Unique ID of the TikTok video |
| `description` | Caption or text content of the video |
| `createTime` | Upload date of the video |
| `author.username` | Author username, for example `@xsrazy` |
| `author.nickname` | Author display name |
| `stats.plays` | Number of views |
| `stats.likes` | Number of likes |
| `stats.comments` | Number of comments |
| `stats.shares` | Number of shares |
| `video.duration` | Video length in seconds |
| `video.width` / `video.height` | Video resolution |
| `video.hdUrl` | Direct HD video URL used for the download |
| `music.title` | Title of the audio used in the video |
| `music.author` | Author of the audio |
| `hashtags` | List of hashtags in the video |

## Collecting links

No coding needed: the [Link Grabber](https://chromewebstore.google.com/detail/link-grabber/caodelkhipncidmoebgbbeemedohcdma) Chrome extension can copy every video link from a TikTok page (profile, hashtag, or FYP). Paste the copied links into `links.txt` and run the tool.

## Notes

- Links must be valid and the videos public, not private
- Avoid downloading thousands of videos in a single batch; keep batch sizes reasonable
- Intended for archiving, educational purposes, and personal backups

## Credits

Created by [@xsrazy](https://github.com/xsrazy).

## License

MIT. See [LICENSE](LICENSE).

<a href="https://www.buymeacoffee.com/xsrazy" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>
