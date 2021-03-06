# CV
## Description
This repository comprehends my personal CV, implemented as a R project. It was created with the R package [pagedown](https://github.com/rstudio/pagedown) and deployed with GitHub Pages (web version) and GitHub (PDF version).

Up-to-date versions are available for [web](https://giuseppett.github.io/CV/CV) and [PDF](https://github.com/GiuseppeTT/CV/raw/print/CV.pdf).

## How to run
### Locally
If your OS is linux based, you can render (convert .Rmd to .html) and print (convert .html to .pdf) the CV locally by running the following commands in your terminal:

```
git clone https://github.com/GiuseppeTT/CV.git
cd CV

make install_dependencies
make render_CV
make print_CV
```

This will:
- Clone the repository to your machine.
- Access the project folder.
- Install R dependencies.
- Render the CV.
- Print the CV.

After that, the CV and resume (one-page CV) will be available at `output/` folder.

### Locally, but with steroids
Additionally, if you have VSCode and docker installed, you can can reproduce my development environment in your machine. To do so, install the VSCode extension [ms-vscode-remote.remote-containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) and follow the steps in the [extension tutorial](https://code.visualstudio.com/docs/remote/containers#_quick-start-open-an-existing-folder-in-a-container) before running the following commands in your terminal:

```
make render_CV
make print_CV
```

### GitHub Actions
You don't have to do nothing. I set up a workflow, so every time I push to the `main` branch, GitHub Actions will deploy the last version to `github-pages` (.html files) and `print` (.pdf files) branches. From the `github-pages` branch, GitHub Pages will also update the associated web version.

## Structure
The project structure is the following:
- `.devcontainer/`: Contains devcontainer files. Used to reproduce my development environment in your machine with VSCode and docker.
- `.github/workflows/`: Contains GitHub Actions workflow. Mainly used to deploy CV.
- `css/`: Contains .css (style) files.
- `output/`: Contains .html and .pdf (output) files.
- `rmarkdown/`: Contains .Rmd (source) files.
- `.gitignore`: List of files that git should ignore.
- `DESCRIPTION`: Meta information for R projects/packages. Mainly used to install dependencies with `remotes::install_deps`.
- `LICENSE`: License file. Complements MIT license.
- `makefile`: List of useful commands.
- `README.md`: This very file you are reading.
