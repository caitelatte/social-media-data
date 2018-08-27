# Social Media Data Analysis

This is a project for analysing archives of your own personal data as provided
by social media sites. [Caitlin Macleod](http://caitelatte.com) made this code for a talk at PyConAU 2018 called ["Accessing and analysing your own social media data"](https://2018.pycon-au.org/talks/45252-accessing-and-analysing-your-own-social-media-data/).

## Requirements

This project uses various aspects of the [Anaconda distribution](https://www.anaconda.com/download).
Anaconda is a distribution of Python + R and various tools for data science and machine learning. The key tools that this project currently has a dependency on are:

-   Python Version 3 or above - `facebook-analysis.ipynb` uses some features of Python that don't exist in Python 2 (eg `os.path` tools)
-   `numpy`
-   `matplotlib`
-   `pandas`
-   (not yet used) `nltk` - this is included in Anaconda but the dataset needs to be downloaded manually and will take up a few GB of space. See [NLTK 3.3 Documentation: Installing NLTK Data](https://www.nltk.org/data.html)

### Personal data archives

This project requires data to look at.

-   

## Setup

Download the archives from various websites into a subdirectory of this folder and unzip them if necessary.

I used a folder called `archive_dir/` with subdirectories for Facebook and
Twitter, including a date tag for when it was downloaded. Paths to your directories can be specified in the first code block of each Jupyter Notebook.

Example directory layout:

-   Git repository: `social-media-data/`
    -   Jupyter notebooks: `facebook-analysis.ipynb`, `twitter.ipynb`
    -   Archives directory: `archive_dir/`
        -   Particular archive directories: `facebook-caitelatte-20180528/`, `twitter-caitelatte-20180528/`

## Running
