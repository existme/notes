# Misc-Audible-Download.Md

## [how-to-listen-to-audible-files](https://askubuntu.com/questions/16918/how-to-listen-to-audible-files)

In your library, near the right top corner, you can select "Format 4" (instead of
.aax or .aax+). The download links will change to .aa files. From what I 
understand, they're a weird kind if mp3 which is easily converted using ffmpeg.
This option (to pick `Format 4`) is only available if your browser's user agent 
looks like a Linux system.

``` sh
ffmpeg -i downloaded_file.aa output.mp3
```

The -i option just specifies the input file. The output file apparently needs 
no -option. This is the simplest usage of ffmpeg, but it will re-encode the file 
(loses a little bit of quality, and it's slow).

It is better (10× faster) to use the 'stream copy' feature:

_stream copy_{.ct}
``` sh
ffmpeg -i downloaded_file.aa -codec copy output.mp3
```
## aax decoding

1. Download the chrome driver from [Downloads - ChromeDriver - WebDriver for Chrome](https://sites.google.com/a/chromium.org/chromedriver/downloads)
    1. You should download the version which matches to the version `/usr/bin/google-chrome`
    2. You might need to upgrade your `urllib3` using:
      ``` 
      python -m pip install --upgrade urllib3
      ```
2. Move the `chromedriver` executable to `/usr/local/bin`
3. Clone [nAudible-NG/audible-activator][GINAARYADAFASUHGCINTPIIR]
    ``` 
    pip install --user requests
    pip install --user selenium
    ```
4. Run it:
   ``` sh
   ./audible-activator.py --username=xxx --password=xxx
   ```
5. Then you will be prompted to press enter, after pressing enter you will get `activation_bytes`



-----------------------------------------
2018-02-13 06:54:05

[GINAARYADAFASUHGCINTPIIR]: https://github.com/inAudible-NG/audible-activator