# Experiments Template

Template project for statically generated documents, for web experiments in a particular domain.

[Hosted by Github Pages](https://moddyz.github.io/ExperimentsTemplate/).

## Usage

Run `generateContent.py` to generate web documents based on the [templates](./templates) and 
context provided by each experiment under [experiments](./experiments).

## Requirements

The jinja2 python template engine is required.

## Project Structure

- [templates](./templates): hosts the jinja2 html templates.
- [static](./static): shared, support files including style, fonts, and scripts.
- [experiments](./experiments): each web experiment.  

Each _experiment_ consists of the per-experiment documents which contribute to the output, statically generated HTML document `index.html`:
- `context.json`: metadata imparting high-level descriptions about the experiment.
- `content.html`: static html body, which is inserted into the generated `index.html`.
- `script.js`: javascript which is referenced in `index.html`. 
- `style.css`: stylesheet which is referenced in `index.html`.

`generateContent.py` should be run to re-generate the output `index.html`, if `context.json` or `content.html` are modified.
