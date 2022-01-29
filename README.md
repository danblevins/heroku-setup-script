# ☁️ Heroku Bash Script for Python Flask Apps

## About this Script

This script is used to automate some of the Flask Python setup in Heroku.

Specifically, it will [define the Procfile](https://devcenter.heroku.com/articles/getting-started-with-python#define-a-procfile), [specify the runtime](https://devcenter.heroku.com/articles/python-runtimes), and [install Python dependencies](https://devcenter.heroku.com/articles/python-pip).

If you find this script helpful, consider adding it to your [terminal command aliases](https://github.com/danblevins/list-of-terminal-command-aliases).

## Installation & Usage

Ensure you have [pipreqs](https://pypi.org/project/pipreqs/) installed.
<br>
`$ pip install pipreqs`
<br>
<br>

Then, go to your projects root folder in your terminal/ command line.

Copy, paste, and run all of the following in your terminal/ command line:
```
echo 'web: gunicorn main:app' > Procfile && \
python3 --version | tr '[:upper:]' '[:lower:]' | tr ' ' '-' > runtime.txt && \
pipreqs --force > requirements.txt && \
echo 'gunicorn==20.0.4' >> requirements.txt
```

## Libraries Used:

- [echo](https://ss64.com/bash/echo.html)
- [tr](https://ss64.com/bash/tr.html)
- [pipreqs](https://pypi.org/project/pipreqs/)
