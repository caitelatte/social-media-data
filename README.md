# Social Media Data Analysis

This is a project for analysing archives of your own personal data as provided
by social media sites. I ([Caitlin Macleod](http://caitelatte.com)) made this code for a talk at PyConAU 2018 called ["Accessing and analysing your own social media data"](https://2018.pycon-au.org/talks/45252-accessing-and-analysing-your-own-social-media-data/).

If you want to find out more about the talk, here are some links:

-   [Google slides for Accessing and analysing your own social media data](https://docs.google.com/presentation/d/1xScnw2Ij4elMvbK7CMxs7ffkZRZH4N2mYPszAKKB3ag/edit?usp=sharing)
-   [Twitter thread about the talk and submitting the proposal!](https://twitter.com/caitelatte/status/1033592792549810177)
-   [Youtube recording of Accessing and analysing your own social media data](https://www.youtube.com/watch?v=JNZH95aXNXo)

The talk explored what personal data is, how we can download it from social media sites (in particular Facebook and Twitter), and how I learnt some basic data analysis tools in Python to look into the information I received.

***WARNING: Please share this data responsibly!*** While this project is about downloading and analysing your own personal data, the basic premise of social media sites is that you are interacting with other people. Other people may not appreciate it if you share their own personal data as a result of this project. You may have private or sensitive information that others have shared with you in your archive.

Please take this into account when storing and sharing your social media personal data 😎

## Requirements

This project uses various aspects of the [Anaconda distribution](https://www.anaconda.com/download).
Anaconda is a collection of Python + R and tools for data science and machine learning. The key tools that this project currently has a dependency on are:

-   Python Version 3 or above - `facebook-analysis.ipynb` uses some features of Python that don't exist in Python 2 (eg `os.path` tools)
-   `numpy`
-   `matplotlib`
-   `pandas`
-   (not yet used) `nltk` - this is included in Anaconda but the dataset needs to be downloaded manually and will take up a few GB of space. See [NLTK 3.3 Documentation: Installing NLTK Data](https://www.nltk.org/data.html)

### Personal data archives

This project requires data to look at.
*your OWN accouts*

-   **Facebook:** please download JSON format data from [http://facebook.com/your_information](http://facebook.com/your_information). The categories used are:
    -   Likes and reactions (the `facebook-analysis.ipynb` code looks for this in `{FACEBOOK_ARCHIVE_DIR}/likes_and_reactions/posts_and_comments.json`)
    -   Messages (looks for individual JSON files under `{FACEBOOK_ARCHIVE_DIR}/messages/{conversation_name}/message.json`)
-   **Twitter:** please download the `tweets.csv` file from [https://twitter.com/settings/your_twitter_data](https://twitter.com/settings/your_twitter_data)
    -   There's also an advertisers_list available from that menu - not looking at it at the moment but it looks fun.

## Setup

Download the archives from the desired social media websites into a subdirectory of this folder and unzip them if necessary.

I used a folder called `archive_dir/` with subdirectories for Facebook and
Twitter, including a date tag for when it was downloaded. Paths to your
directories can be specified in the first code block of each Jupyter Notebook.

Example directory layout:

-   Git repository folder: `social-media-data/`
    -   Jupyter notebook files: `facebook-analysis.ipynb`, `twitter.ipynb`
    -   Archives folder: `archive_dir/`
        -   Customised archive folders: `facebook-caitelatte-20180528/`, `twitter-caitelatte-20180528/`

## Running the code!

I was running this code using a Jupyter server. The Jupyter server needs to be started from the repository folder.

*It's important that the Jupyter server is started from the correct folder as the notebooks use relative paths to the archive directories. Remember that you can customise the paths yourself inside the notebooks!*

1.  Open a terminal or command prompt and run the following commands:

    ```bash
    cd (path to this social-media-data git repository)
    pwd
    # confirm that you are currently in the social-media-data repository
    jupyter-notebook
    ```
2.  The `jupyter-notebook` command should open a browser tab with the Jupyter Notebook's home directory. Open the `facebook-analysis.ipynb` or `twitter.ipynb` files.
    -   Customise the variables in the first code block to point to the correct directories (starting from the Jupyter server's working directory).
    -   Run the code blocks in order!
    -   Have fun, change things, hopefully responsibly share cool fun stats about what you've found :D
        - **ALSO PLEASE TELL ME IF YOU FOUND A PRIDE REACT IN YOUR FACEBOOK DATA 🏳️‍🌈**
