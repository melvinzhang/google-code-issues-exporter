This is a simple script to export issues from Google Code as JSON.

### Required Python libraries ###

Run `pip install -r requirements.txt` to install all required libraries.

### Usage ###

    export-issues.py [options] <google project name>

      google_project_name       The project name (from the URL) from google code

    Options:
      -h, --help                Show this help message and exit
      -c, --google-code-cookie  Supply cookies to use for scraping Google Code
      --skip-closed             Skip all closed bugs

`--google-code-cookie` takes a HTTP header encoded cookie to use when fetching
pages from Google Code. Google Code normally mangles names for spam prevention,
and getting the raw names requires being logged in and having filled out a
CAPTCHA.

`--skip-closed` will skip migrating issues that were closed.

Output is one JSON object per line, one for each issue on Google Code.
