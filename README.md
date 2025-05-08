# Multi Downloader with Video Compressor and File Management Capabilities

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1w_W4STwn4tXqAk_cwao9jFlSgFGAx1vN#scrollTo=X3gbdM02VdNt)

This project provides a suite of tools within a Google Colab environment for downloading various types of media, compressing videos, and managing files.

## Features

* **Universal Downloader**: Supports downloading files using:
    * `wget` (general purpose) 
    * A custom Bunkr.ru downloader (for albums and individual files) 
    * `m3u8` stream downloader 
    * `yt-dlp` for Bunkr (alternative Bunkr download method) 
* **Video Compressor**: Compress videos using `ffmpeg` with adjustable Constant Rate Factor (CRF) for quality control. 
* **File Manager**: Perform operations like move, copy, or delete files and folders within your Google Drive or Colab environment. 

## How to Use

1.  **Open in Colab**: Click the "Open In Colab" badge above to open the notebook in Google Colaboratory.
2.  **Setup**:
    * Run the first cell titled "**Setup: Mount Drive, Install Dependencies & Import Libraries**". 
    * This will mount your Google Drive (if you choose to use it for output), install necessary Linux packages (`ffmpeg`, `aria2`, `wget`), and install required Python libraries (`yt-dlp`, `ipywidgets`, `requests`, `beautifulsoup4`, `python-magic`, `m3u8downloader`). 
3.  **Choose a Tool**: Navigate to the section of the notebook corresponding to the task you want to perform.

    * **Compress Video**:
        * Go to the "**Compress Video**" section. 
        * Set the `video_path` to the location of your input video file. 
        * Set the `output_path` for the compressed video. 
        * Adjust the `crf` value (lower means better quality and larger file size, default is "23"). 
        * Run the cell. A progress bar will show the compression status. 

    * **File Manager**:
        * Go to the "**File Manager**" section.
        * Choose the `operation`: "move", "delete", or "copy".
        * Specify the `source_path`.
        * If moving or copying, specify the `dest_path`.
        * Run the cell. A progress bar will indicate the progress of the file operations. 

    * **Universal Downloader**:
        * Go to the "**Universal Downloader**" section, specifically the first cell under it ("**Run to Download**").
        * Enter the `url` of the content you want to download. 
        * Select the `download_type`:
            * `a`: `wget` Downloader (for direct links) 
            * `b`: Custom Bunkr Downloader (for Bunkr.ru links - albums/files) 
            * `c`: `m3u8` Downloader (for HLS streams) 
            * `d`: Bunkr Downloader (using `yt-dlp` - for Bunkr.ru video links) 
        * Set the `output_path` (directory where files will be saved). 
        * Run this cell to set the parameters.
        * Then, run the next cell ("**Run Cell to Start Download**) to initiate the download process using the chosen method. 

## Dependencies

* `ffmpeg`
* `aria2`
* `wget`
* `yt-dlp`
* `ipywidgets`
* `requests`
* `beautifulsoup4`
* `python-magic`
* `m3u8downloader`

These are automatically installed by the setup cell in the Colab notebook. 

---

Save this content as `README.md` in the root of your GitHub repository.
