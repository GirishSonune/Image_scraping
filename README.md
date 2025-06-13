# Image_scraping

A Python-based project for scraping images from the web. This tool allows users to automatically search for and download images based on given keywords, saving them to a specified directory. It's useful for building datasets, research, or gathering images for machine learning and computer vision projects.

## Features

- Search and scrape images based on keywords
- Download images from multiple sources (e.g., Google Images, Bing, etc.)
- Save images to a custom directory
- Configurable number of images per search
- Handles duplicate and broken image links
- CLI for easy usage
- Simple, modular, and easy-to-extend codebase

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/GirishSonune/Image_scraping.git
   cd Image_scraping
   ```

2. **Create and activate a virtual environment (optional but recommended)**
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## Usage

You can run the image scraper from the command line:

```bash
python main.py --query "cats" --limit 100 --output ./images/cats
```

**Arguments:**

- `--query`: The search keyword(s) for images.
- `--limit`: (Optional) Number of images to download (default: 50).
- `--output`: (Optional) Directory to save images (default: ./images).

**Example:**

Download 100 images of "sunsets" and save to `./images/sunsets`:

```bash
python main.py --query "sunsets" --limit 100 --output ./images/sunsets
```

## Project Structure

```
Image_scraping/
├── main.py
├── scraper/
│   ├── __init__.py
│   ├── google_scraper.py
│   └── bing_scraper.py
├── utils/
│   ├── __init__.py
│   └── helpers.py
├── requirements.txt
└── README.md
```

- `main.py`: Entry point for the application.
- `scraper/`: Contains modules for scraping images from different sources.
- `utils/`: Utility functions for downloading, saving images, and handling errors.

## Requirements

- Python 3.7+
- See `requirements.txt` for all dependencies (e.g., requests, beautifulsoup4, tqdm, Pillow).

## Customization

You can extend the project by adding new scraper modules in the `scraper/` directory for additional sources.

## Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a pull request

## License

This project is licensed under the MIT License.

## Disclaimer

This project is intended for educational and research purposes. Please respect the terms of service and copyright of the websites you scrape.

---

**Author:** [Girish Sonune](https://github.com/GirishSonune)
