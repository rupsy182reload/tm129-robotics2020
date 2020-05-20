## 1.6 Activity: The RoboLab Notebook Editable Text Environment


In this short activity I will show you how to organise your RoboLab work environment. You won’t run any robot programs until the next activity.

---
<div class='alert-danger'>TO DO - this is a 101 in using the environment. We're in an md doc running in notebook, so can use this part of the doc interactively. The workflow / layout may change, but that needs front-end js/ts/css dev and debug skills I donlt have (atm...). I'm working on MVP workflow atm, which may suck, but should work.</div>


If you clicked on the the link to this document from a Jupyter notebook server homepage in the RoboLab environment, it will have opened within the notebook user interface as an interactive notebook document.


### A first look

To start RoboLab, launch the ContainDS application.

If RoboLab is running, you should see it in the side bar, with its status indicator highlighted green. 

![ContainDS showing a running container with a green status indicator](../images/00_01_ContainDS_robolab_running.png)

If it is not running, the status indicator will be greyed out. Click on the `START` button to start the container running.

If you cannot see the container in the sidebar, click on the `+NEW` button and following the instructions for *Running the RoboLab Environment from a Local Docker Image*.

If you cannot see a local copy of the image, follow the instructions for `Using ContainDS to Install the Prebuilt RoboLab Container Image`.

With the container running, click on the `WEB` button to open the notebook server homepage in your browser.

When RobotLab starts, the notebook server homepage will look something like the following (the actual file listing may differ).

![Example of the notebook server homepage, including Files, Running and NBextensions tabs and a file listing.](../images/00_01_jupyter_nb_homepage.png)


If you click on a folder link, you will be presented with a list of the files contained in that folder, as you might expect. Click on the directory path links to navigate your way back up the directory listing tree.

The top of the directory listing is the directory that you shared in to the container using ContainDS. If you started the container from the command line, the top level is the `/home/jovyan` directory in the container and files should be mounted into that directory, either directly on on the path (for example, `/home/directory/mySharedDirectory`).


## Working With Notebook Files Interactively

If you are reading this document in a live Jupyter notebook environment, you will be able to interact with it directly.


For example, you can correct the speling mistake in this sentence by editing it directly. Double click on this paragraph, and the cell will become editable. Correct the spelling mistake, then "run" the markdown cell to redisplay it as formatted text.

You can do this in two ways. Either click on the `Run` button in the toolbar, or use a keyboard shortcut: `shift-enter` (that is, the shift key and the enter key at the same time).

Remember, to look up keyboard shortcuts, you can use the `ESC-h` keyboard shortcut (press the escape key and then, quickly after, the `h` key, or the escape key and the `h` at the same time): in the "Edit mode" area, look for "run selected cell".


### Previewing Formatted Markdown

Markdown text is a simple *mark-up* language in which you can write styled text using simple (hopefully intuitive) text elements. For example, to *emphasise* a word using italics, write it as follows: \*emphasis\*.

You may notice my "starred" text is not itself italicised. If you double click on this markdown cell to see its editable view, you will see I have "escaped" the * characters around the word \*emphasis\* with a backslash character — \ — as if to say: *do not process this*. Note that if you have a space between a * and a letter at the start of a word, then the styling is similarly not applied; likewise, to "close" the styling, you need to place the second * right next to the final character in the emphasised text.

*When you have finished looking at the editable text, hit `shift-enter` to return the cell to the rendered view.*

That may all sound complicated, but hopefully it will become natural to you. You may find you use similar techniques anyway when writing emails or social media messages or posts. You may even find that your editor in those environments is actually treating your text markup as markdown anyway.

The next paragraph contains several examples of other forms of mark up. Double click on the cell to make it editable so you can see how the styling was generated.

<!-- #region -->
### Markdown Examples

Double click on this cell to see how markdown is used to create particular styling effects.

We can *italicise text* by wrapping it with single asterisk `*...*` or `_..._` underscore elements.

Use a backslash character to disable the text processing effect, eg if you which to italicise a *\** character.

Strong (__bold__) emphasis can be introduced by wrapping text doubling up the number of * or _ elements.

Unnumbered list items:

- are prefixed by a `-` or single `*` character, followed by a space;
* are clearer in their text for if you precede the first list item with a blank line
  - sublists are indented, and are identified by prefixing the - or * marker by two spaces.
  
Numbered lists:

1. are identified by prefixing the line with `1.` followed by a space.
1. some flavours of markdown may offer the ability to use alternative numbering schemes (letters, or Roman numerals, for example).


Headings are identified by starting the header line with one or more `#` characters, followed by a space and then the title or (sub) heading. The number of `#` characters identifies the level of heading required.

You can also identify a heading by placing two or more equals signs (`==`) on the line immediately below it, or a subheading by placing two or more dashes (`--`) at the start of the following line.

Dividing lines can also be added: just start a line with three or more dashes (`---`) prefixed by an empty line.

---

Inline `code` can be identified by wrapping the code item within backticks: \`...\`. 

Blocks of code can identified by marking out an area using three or more backticks to start and end the block:

```
# comment
def hello(msg):
    print(msg)

hello("my friend")
```

Syntax highlighting for a particular language can be enabled by declaring the language required immediately after the opening set of backtcicks (although rendereing backticks in backticks can be tricky!). For example, starting a code block with ```` ```python ```` will cause it to be rendered using Python language syntax highlighting:


```python
# comment
def hello(msg):
    print(msg)

hello("my friend")
```

You can also add links you your markdown text, using constructions of the form: `[my link text](https://example.com)`.
<!-- #endregion -->

<!-- #region -->
## Taking Ownership of Your Notebooks

One of the difficulties in working with electronic texts is that they can often be hard to annotate. Interactive notebook style interfaces offer a different way of working, in that you can annotate or edit the text directly. 

One way of annotating the markdown text materials is to use the highlighter pen from notebook toolbar.

![Notebook toolbar showing highlight pen buttons.](../images/00_01_highlighter.png)


<span class="mark">Simply select the text you want to highlight in its rendered view, and then click on the appropriate highlighter pen colour.</span>

Another way is to just start clicking on the markdown cells, adding your own notes, commentary or reflection, or your own questions, explanations and examples, to the text.

There are risks associated with this of course - like accidentally deleting a chunk of module materials, or changing a working example to a broken one. But there are also many advantages - like making the materials meaningful *to you*. And if you want to distinguish your content from the provided materials, you can always highlight them, or put them in a markdown cell of their own, with a heading that identifies the text in that cell as your own work. 
<!-- #endregion -->

<!-- #raw -->
Alternatively, from the notebook toolbar, change your own markdown cells to cells of type `Raw NBConvert`. Although this cell type does not render the markdown styling — the text is presented in a "raw" teletype style text view —  if you used markdown annotations *they should still mark up your text in a __meaningful__ way*. And the text is visually distinguishable from the provided, styled, markdown materials.
<!-- #endraw -->

### Previewing Style Markup

Although I find it second nature to write in markdown (I've been been writing in simple text formats for a long time!) you may find it takes some getting used to, and that you keep having to flip between the edit view and the rendered view to make sure you are creating the text effect you intended.

To make it easier, if you enable the `livemdpreview` notebook extension [[direct link](/nbextensions/?nbextension=livemdpreview/livemdpreview)], you can preview how your rendered markdown looks in a preview window directly underneath a markdown cell you are editing.

*You may need to save your notebook and reload it in your browser after enabling the extension to see the effect. It should be enabled by default for any notebooks you open after enabling the extension.*

A checkbox option in the extension's configuration panel optionally allows you to display the preview alongside, rather then below, the markdown cell being edited. The preview disappears when you return the cell to its display mode.


### WYSIWYG "Text Editor" View
If you really cannot get to grips with writing raw markdown, a WYSIWG editor is available.

Enable the [`jupyter_wysiwyg`](/nbextensions/nbextension=jupyter_wysiwyg/index) extension from the `nbextensions` notebook configuration tab on the notebook server homepage. (You may find that access to the *WYSIWYG text editor* extension is disabled at first; at the top of the extensions configurator page, uncheck the *disable configuration for nbextensions without explicit compatibility* option.)

Save and reload your notebook. When you double click on a markdown cell to edit it, you should now see two buttons have appeared on the left-hand side of the cell, one with a `Rich Text Editing` tooltip when you hover over it, the other with a `Run Cell` tooltip.

The `Run Cell` button provides a convenient additional way of rendereing a markdown cell that is currently in edit mode. You also need to use this button to render the cell if you have been editing it using the rich text WYSIWYG editor.

The `Rich Text Editing` button provides a way of launching the rich text editor. This editor allows you to style your text, and immediately see the result, as you type. You can still see the raw mark-up text by rendering the cell and then double clicking on it to take it into the edit mode. However, you may find that the marked up text is not quite as clean as mark-up text: HTML tags are used to style the text and any previous markdown annotations will be converted to theitr HTML equivalents.


## Creating New Cells

To create a new cell in a notebook, click on the `+` button in the notebook toolbar. A new cell will be created directly below the current selected cell.

By default, a new cell is created as a code cell. To convert the cell to a *markdown* cell type, change the cell type using the cell type drop-down list in the notebook toolbar from `Code` to `Markdown`.

A keyboard shortcut — `ESC-M` (that is, the escape key followed by the letter `m`) — also converts a selected cell in *Edit mode* to the *markdown* cell type.


## Code Cells

Code cells can be used to enter — and *execute* — Python code.

To run a code cell, which is to say, to execute the code contained in a code cell, click in the code cell to select it and then press the run ("play") button on the notebook toolbar. Alternatively, use a keyboard shortcut - `SHIFT-RETURN` — to run the selected cell.

```python
print("Hello!")
```

When a cell has successfully completed executing, the run status indicator is coloured green. After running a code cell, a number in square brackets displays a cell execution index number. Each time a code cell is run, the overall index count goes up by one and is used to indicate the cell execution index (or "cell run number") for that cell.

When a code cell is running, or waiting to run, it is highlighted with a light blue colour on the left hand side. A * character also indicates the status of the running cell.

<img alt="Screenshot of notebook showing one completed cell execution with green run status indicator in the cell sidebar, along with one running cell and one yet to be run cell with a light blue run status indicator." src="../images/00_01_cell_run_status_running.png" width=400 />

If you run all the cells in a notebook, all the cells yet to be run, as well as the running cell, are highlighted with a blue run status indicator and the * cell run number.

<img alt="Screenshot of notebook showing one completed cell execution with green run status indicator in the cell sidebar, along with one running cell and one yet to be run cell with a light blue run status indicator." src="../images/00_01_cell_run_status.png" width=400 />


If an error is raised that causes a code cell not to execute correctly, the run status indicator is coloured pink and an error message is show beneath the the cell in the code cell display area.

<img alt="Screenshot of notebook showing one completed cell execution with green run status indicator in the cell sidebar, along with one running cell and one yet to be run cell with a light blue run status indicator." src="../images/00_01_cell_run_error.png" width=800/>

Clicking on the arrow will at the end of the error messge will reveal the full error message.

<img alt="Screenshot of notebook showing a code cell execution error with expanded error message." src="../images/00_01_cell_run_error_message.png" width=800 />


Run the following cells to see the indicators in action.

```python
import time
```

```python
time.sleep(25)
```

```python
print("hello")
```

```python
print("hello again"
```

### Displaying Code Line Numbers

Sometimes it can be useful to display line numbers in a code cell to more easily reference or refer to a particular line of code. Line numbers can be toggled on and off within a particular code cell using the keyboard shortcut `ESC-L` (that is, *escape* and *l*).

When a notebook is saved, the  line number toggled display settings are also saved.

```python
# Example of code cell line numbering

# This is actually line 3...
```

Click in the above code cell to select it and practice toggling the line numbers on and off.


### Code Style

To make code as readable as possible, the [Pyhton PEP8 style guide](https://www.python.org/dev/peps/pep-0008/) provides guidance on how to lay out your code so that it is easier to read. Code style guidance includes things like:

 - use of white space within lines and between lines
 - naming conventions for function and variable names 
 - maximum line lengths to maintain readability
 
Throughout the notebooks, we have tried to use good practice, although PEP8 standards have not necessarily always been enforced. Various tools are available for warning about breaches of PEP8 style guidelines or even automatically formatting code so that it is style compliant, but these are disabled by default in these notebooks.

*See [Notebook Code Linting](https://github.com/innovationOUtside/TM351_forum_examples/blob/master/Notebook%20Code%20Linting.ipynb) for more information about automatically linting code in Jupyter notebooks.*


## Creating New Code Cells

Single click on this markdown cell to ensure that it has the focus and then create a new code cell by clicking on the `+` button in the notebook toolbar. A new cell will be created directly below the currently selected cell, whatever type of cell it is. By default, newly created cells are created as code cells. The cursor focus is automatically moved to the new cell, so once it is created you can immediately start typing code into it.

__DO:__ *Click on the `+` button in the notebook toolbar to create a new code cell, entry `print('hello world')` and run the cell to execute the code and see the result.*

Feel free to create and run your own notebook code cells to try out your own code examples. Remember, the notebooks *are yours*. So make full use of them...


## How the simulator relates to the notebooks

The simulator we are using is created as an interactive `ipywidget` that is embedded within a Jupyter notebook. In the current iteration, the layout is not ideal, but we are working on improving on it.

The simulator runs as a Javascript programme in the browser tab associated with the notebook the simulator is embedded in. The simulator has various settings that can be configured within the simulator UI, or from the notebook commands that invoke it.

*TO DO: there may also be magicked UIs for various settings; still to be decided.*


Run the following code cell to load in an instance of the simulator and embed it within this notebook:

```python
from nbev3devsim import ev3devsim_nb as eds
%load_ext nbev3devsim

roboSim = eds.Ev3DevWidget()
display(roboSim)
```

Code is "downloaded" from a code cell in the notebook to the simulator by running the code cell with some special IPython *magic* in the first line of the cell.

Run the following code cell to download the code to the simulator. Then click the *Run* button in the simulator to run the downloaded code there.

```python
%%sim_magic_preloaded roboSim

# Stay inside
tank_drive.on(SpeedPercent(50), SpeedPercent(50))
tank_turn.on_for_rotations(-100, SpeedPercent(75), 2)
```

Only a single instance of the simulator should be embedded in any given notebook, although you may have different notebooks open each running their own embedded simulator. (It is generally not advisable to have multiple copies of *the same notebook* open in multiple windows. As the notebooks autosave, you may find that work you have created and saved from one notebook gets overwritten by an earlier version of the notebook in a different browser tab or window.


### Alternative RoboLab User Environments

The original `ev3devsim` simulator ran solely within a web browser (that is, it did not require any support from Jupyter tools). The embedded simulator has been extended and whilst many of the extensions could be integrated back into the original standalone simulator, they have not currently been so.

Withing the Jupyter ecosystem, using tools such as JupyterLab, or Voilà interactive dashboards/applications, there is more scope for controlling the layout of the RoboLab environment. For the initial treatment, however, we are just working with Jupyter notebooks.

One advantage of using Jupyter notebooks is that we can retrieve logged data from sensors mounted on the robot in the simulator back into the notebook environment and then use the full range of Python charting and analysis tools to expore the data.


### Configuring the Simulator Layout

The simulator environment includes a range of user controls that can be used to configure the layout and view of the simulator user interface, as well as controlling operations performed within it. These include positioning the simulated robot, loading in different simulator backgrounds, loading obstacles into the simulated world, displaying status messages from the robot and dynamically charting logged sensor readings, as well as many other features.

You will be introduced to these in more detail as and when they are required.


## Creating and Saving Your Own Code

The activities hve been created within Jupyter notebooks using the embedded simulator. In many activities, you will have the opportunity to create and run your own programmes to run within the simulator, as well as within the notebook's own Python coding environment.

Saving a notebook will save your code and any currently displayed cell outputs (the notebooks also autosave regularly), so you can close the notebook, shutdown the associated notebook process, and then restart the notebook and return to it later. 

Although the current simulator view, any other displayed widgets, and the internal state of the simulator and the notebook's own Python environment, are not saved, rerunning the code cells that create them will generate them afresh.

As well as using the provided notebooks, you are also encouraged to create and save your own notebooks and use the simulator for your own exercises.