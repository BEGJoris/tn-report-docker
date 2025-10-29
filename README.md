# 🐳 Build tn-report Latex templates with Docker 

The goal of this fork is to provide a simple, ready-to-use way to compile the LaTeX templates from [cholezth/tn-report](https://github.com/cholezth/tn-report)__without installing LaTeX locally__, using __Docker__.

## Start

__⭐️ Don’t forget to give the project a star if you find it useful! 😉__

> [!IMPORTANT]
> Make sure you have [Docker](https://www.docker.com/) installed on your machine before running the commands below.

### __1️⃣ Start the Docker container__

``` bash
docker compose up -d
```
> 💡 The `-d` flag runs the container in detached mode. You can remove it if you want to see the build logs directly in your terminal.

Once it’s running, you should see a new `/dist` folder containing your generated __PDF file__ 🎉
(Don’t worry about the other files in there — they’re required by the LaTeX compiler.)

__The container runs in hot-reload mode__, so you don’t need to rebuild it every time you make changes — just save your .tex file, and it will automatically recompile. ⚡️

### __2️⃣ Custom configuration__

You can configure the build behavior by editing the `.env` file:

```bash
TEX_FILE=example-report-1A.tex   # name of the main .tex file
BUILD_DIR=dist                   # output directory
# BIB_FILE=example.bib           # name of the bibliography file (optional)
# BIB_PATH=./                    # path to the .bib file (optional)
```

So you can easily change and configure compile commands behavior.

## 🤝 Contributing

Contributions are welcome!
If you’d like to improve the Docker setup or fix something, feel free to open a __pull request__.

If you run into any issues or have questions, don’t hesitate to open an issue on GitHub.

⬇️ The rest of the original README from [cholezth/tn-report](https://github.com/cholezth/tn-report) follows below 😘 ⬇️

# TELECOM Nancy Master Thesis/Project Report Template for LaTeX

This is a very basic LaTeX template provided by [TELECOM Nancy](http://www.telecomnancy.eu) for Master thesis, internship and project report.

## Usage

Make a copy of the provided sample latex document called `example-report.tex` or`example-report-1A.tex`.
Edit the different properties (author, title, figures, etc.). Add your references in the provided `example.bib` file (or add your own file).

The document class provides few options:
- `english` for report/thesis written in english
- `stage1a` and `stage2a` for a first and second year internship report
- `confidential` for confidential report (a watermark is added on every page)
- `pidr` for interdisciplinary project - **`[DEPRECATED]`** since these reports should not comply anymore to this template -


## Contributing

In order to contribute to this template, you just have to submit a pull request.

1. Fork it.
2. Create a branch (`git checkout -b my_template`)
3. Commit your changes (`git commit -am "[+] english support"`)
4. Push to the branch (`git push origin my_template`)
5. Open a [Merge Request]
6. Thanks a lot!

