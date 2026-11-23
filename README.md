# Web Calculators

Small calculators and viewers that run entirely in your browser. Each one is a single HTML file.

**Live site:** https://jwkunz.github.io/web_calculators/

## What is here

| Page | What it does |
|---|---|
| `plot_and_integrate.html` | Plot a function of x that you type in, and integrate it over a range |
| `discrete_time_fourier_transform_viewer.html` | Sample a function of time and view its discrete-time Fourier transform |

## Adding a new page

1. Put your new `.html` file in the root of this repository.
2. Commit and push to `main`.

That is all. The landing page lists every `.html` file in the repository automatically, in
alphabetical order. A page named `my_new_calculator.html` appears as "my new calculator".

For a nicer title and a short description, add an entry to [`_data/pages.yml`](_data/pages.yml). The
key is the file name without `.html`:

```yaml
my_new_calculator:
  title: My New Calculator
  description: One sentence on what it does.
```

To keep a file off the landing page, move it into a folder whose name starts with an underscore (for
example `_drafts/`), or add it to the `exclude` list in `_config.yml`.

## How the landing page works

The site is built by GitHub Pages with Jekyll. `index.html` uses Liquid to loop over the repository's
static `.html` files, so it never needs editing when pages are added. Each calculator is served
as it is.
