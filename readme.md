# google-img-downloader
google-img-downloader is a Python library that allow to download automatically image from google-image

## Installation
Before you install make sure you have installed the latest version of Google chrome, Firefox or Safari
Use the package manager [pip](https://pip.pypa.io/en/stable/) to install google-img-downloader.

```bash
pip install google_img_downloader==0.5
```

## Usage

```python
from google_img_downloader.downloader import ImageQuality, Downloader

downloader = Downloader("home")

# Update query
downloader.set_query("house")
# Update sleep time by default 0.25s [Waiting while loading page(s)]
downloader.set_sleep_time(0.25)

# Image Quality available :

# ImageQuality.default
# ImageQuality.large
# ImageQuality.medium
# ImageQuality.icon
downloader.set_quality(ImageQuality.large)

# Number of image you wish to download[save]
downloader.set_number_of_request(10)

# Target folder where image(s) will be saved
downloader.set_folder_path("downloaded/")

# start the process
downloader.start()

```
## Note
During the process running your browser will be open and will operate automatically, we advise to do nothing while the script is running

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)