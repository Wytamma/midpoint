# Midpoint Rooting App

A lightweight, single-page web app for **midpoint rooting phylogenetic trees** in Newick format.
Built with [**PhyloJS**](https://clockor2.github.io/phylojs/) for tree manipulation and [**Phylocanvas.gl**](https://www.phylocanvas.gl/) for interactive visualization.

## Features

* Upload or drag-and-drop Newick files (`.nwk`, `.newick`)
* Paste Newick directly into the text box
* Automatic rendering on load or edit
* One-click **midpoint rooting** (implemented using PhyloJS primitives)
* Download the rooted tree as Newick
* Runs entirely in the browser, no backend required

## Usage

1. Open `index.html` in a modern browser.
2. Drop a Newick file into the page or paste a Newick string.
3. The tree renders automatically.
4. Click **Midpoint root** to reroot the tree.
5. Click **Download Newick** to save the rooted tree.

## Requirements

* A modern browser with WebGL support
* Trees must include **branch lengths** for midpoint rooting to be meaningful

## Implementation notes

* Midpoint rooting is computed by finding the tree diameter and rerooting at its midpoint using `tree.reroot(A, prop)`.
* Visualization uses a rectangular layout via Phylocanvas.gl.
* Styling is handled with Tailwind via CDN for simplicity.

## License

MIT 
