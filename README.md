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

-   **Facebook:** please download JSON format data from [http://facebook.com/your_information](http://facebook.com/your_information). The categories used are:
    -   Likes and reactions (the `facebook-analysis.ipynb` code looks for this in `{FACEBOOK_ARCHIVE_DIR}/likes_and_reactions/posts_and_comments.json`)
    -   Messages (looks for individual JSON files under `{FACEBOOK_ARCHIVE_DIR}/messages/{conversation_name}/message.json`)
-   **Twitter:** please download the `tweets.csv` file from [https://twitter.com/settings/your_twitter_data](https://twitter.com/settings/your_twitter_data)
    -   There's also an advertisers_list available from that menu - not looking at it at the moment but it looks fun.

## Setup

Download the archives from various websites into a subdirectory of this folder and unzip them if necessary.

I used a folder called `archive_dir/` with subdirectories for Facebook and
Twitter, including a date tag for when it was downloaded. Paths to your
directories can be specified in the first code block of each Jupyter Notebook.

Example directory layout:

-   Git repository: `social-media-data/`
    -   Jupyter notebooks: `facebook-analysis.ipynb`, `twitter.ipynb`
    -   Archives directory: `archive_dir/`
        -   Particular archive directories: `facebook-caitelatte-20180528/`, `twitter-caitelatte-20180528/`

## Running the code!

The way that I was running this code was by running a Jupyter server from the repository directory. *It's important that the working directory of the Jupyter server is correct as the notebooks use relative paths to the archive directories. Remember that you can customise the paths yourself!*

1.  From a terminal, run the following:

    ```bash
    cd (path to social-media-data repository)
    pwd
    # confirm that you are currently in the social-media-data repository
    jupyter-notebook
    ```
2.  This command should open a browser tab with the Jupyter Notebook's home directory. Open the `facebook-analysis.ipynb` or `twitter.ipynb` files.
    -   Customise the variables in the first code block to point to the correct directories (a relative path from the Jupyter server's working directory).
    -   Run the code blocks in order!
    -   Have fun, change things, hopefully share what you've found :D
