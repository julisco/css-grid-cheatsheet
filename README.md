CSS Grid Cheat Sheet
--------------------

### 1. Definitions

- Grid: the container which contains grid items
- Grid Lines: horizontal and vertical lines (indexed) composing the grid, can be named
- Grid Track: space between 2 Adjacent Grid Lines. We can separate the Grid Tracks with gutters
- Grid Cell: space resulting from the crossing of 2 adjacent vertical Grid Lines, and 2 adjacent Horizontal Grid Lines
- Grid Areas: combination of 1 or more cells


### 2. Grid Container properties

Display

    display: grid | inline-grid | subgrid

    grid-template-columns: <track-size (length, %, fr)> ... | <line-name> <track-size (length, %, fr)> ...;
    grid-template-rows: <track-size (length, %, fr)> ... | <line-name> <track-size (length, %, fr)> ...;


Name Grid Lines

    grid-template-columns: [line-name] <track-size> ...;

Repeat a pattern

    grid-template-columns: repeat(<times>, <pattern>) ...;

Grid Areas

    grid-template-areas:
        "<grid-area-name> | . | none | ..."
        "...";


Shortand syntax for grid-template-*

    grid-template: none | subgrid | <grid-template-rows> / <grid-template-columns>;

Gutters

    grid-column-gap: <line-size (lentgh)>:
    grid-row-gap: <line-size (length)>;

Shortand syntax for grid-*-gap

    grid-gap: <grid-row-gap> <grid-column-gap>;

Justify items

    justify-items: start | end | center | stretch;

Align items

    align-items: start | end | center | stretch;

Justify content

    justify-content: start | end | center | stretch | space-around | space-between | space-evenly;

Align content

    align-content: start | end | center | stretch | space-around | space-between | space-evenly;

Grid auto

    grid-auto-columns: <track-size (length, %, fr)> ...;
    grid-auto-rows: <track-size (length, %, fr)> ...;
    grid-auto-flow: row | column | row dense | column dense;

Shortand for all the container:

    grid: none | <grid-template-rows> / <grid-template-columns> | <grid-auto-flow> [<grid-auto-rows> [/ <grid-auto-columns>]];

### 3. Grid Item properties

Display

    grid-column-start: <number> | <name> | span <number> | span <name> | auto
    grid-column-end: <number> | <name> | span <number> | span <name> | auto
    grid-row-start: <number> | <name> | span <number> | span <name> | auto
    grid-row-end: <number> | <name> | span <number> | span <name> | auto

Shortand syntax for grid-column-*

    grid-column: <start-line> / <end-line> | <start-line> / span <value>;

Shortand syntax for grid-row-*

    grid-row: <start-line> / <end-line> | <start-line> / span <value>;

Grid area

    grid-area: <name> | <row-start> / <column-start> / <row-end> / <column-end>;

Justify - applied to its content

    justify-self: start | end | center | stretch;

Align - applied to its content

    align-self: start | end | center | stretch;
