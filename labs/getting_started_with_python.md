## Lab 1: Getting Started with Python
*William Gilpin*

Additional information about Python and conda environments can be found in [William’s detailed notes](http://www.wgilpin.com/howto/howto_conda.html)

1. Install Miniconda on your development environment. OS-specific instructions can be found [here](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html). macOS or Linux users should install [Homebrew](https://brew.sh/) as well

2. Open your computer’s terminal app. On Windows, you may need to install [Windows Terminal](https://github.com/microsoft/terminal) if it is not already installed. If Windows Terminal has any issues, you might consider [gitbash](https://gitforwindows.org/) instead. If you plan to use Windows for the class, please keep track of any bugs or compatibility issues you encounter, as well as their solutions—that will make it easier to make the materials more accessible in future iterations.

3. In your terminal app, create a new virtual environment using the base Python install.

```
  $ conda create -n hwenv python=3
```

This virtual environment will be used to isolate your code and the packages on which it depends from your system’s own Python installation, as well as from other Python projects you might make in the future. For example, you will likely want to make a separate environment for your final project, and for separate personal projects. On my personal computer, I have about a half-dozen environments—one for each different project, including one for this class. If I make a mistake while working on this class and break my environment’s Python installation, it won’t affect my other projects.

4.  Before writing any code, always make sure that you have activated your environment.

```
  $ conda activate hwenv
```

5. We can now start Python and check that it is working

```
    (hwenv) $ python
```

6. Check that your Python version is greater than 3.0
  
```python
  >> import sys
  >> print("User Current Version:-", sys.version)
```

7. Terminate the Python process with Ctrl + D on \*nix, or  Ctrl + Z followed by Enter on Windows.

8. (Optional). If your Python version does not start with a 3, delete your environment and then make a new environment with a newer version

```
  $ (hwenv) $ conda deactivate
  $ conda remove -n hwenv --all
  $ conda create -n hwenv python=3
```

9. Back in the Terminal, install some other packages that we will end up using a lot

```
  $ conda install numpy matplotlib 
```

10. There are two ways that I would recommend using Jupyter notebooks for the class. One option is to manually activate an environment and then launch the notebook server from the Terminal. The other option is to let an IDE like VSCode handle everything for you, and just launch notebooks from the GUI. There are lots of other options (like PyCharm).

11. For a slightly more user-friendly experience, I recommend run our Jupyter Notebooks within a full-featured integrated development environment (IDE). I really like Visual Studio Code and would currently recommend it over JupyterLab for the time being. [Installation instructions](https://code.visualstudio.com/). 

12. (Optional, recommended). If you successfully install VSCode above, you can just open the course notebooks using the VSCode GUI, as you would a document or slide deck. However, if opening a .ipynb file, you should always check in the upper-right-hand corner of the notebook that you are using the correct conda environment (since we skipped using the Terminal, we never specified what environment to use). VSCode should automatically find and list the available environments in a drop-down menu, and it will remember your selection for each notebook.

For VSCode, you will still need to use the Terminal to create/edit your conda environments, as well as install and update packages into your environment.

13. To test that you have everything working, try running the Mandelbrot set example at the end of the [first lecture notebook](https://github.com/williamgilpin/cphy/blob/main/talks/python_intro.ipynb)

<!-- 12. Now that we know that everything is working, head over to the class repository on GitHub and start working on Lab 1, which uses some parts of the Python ecosystem in order to make really cool embeddings of high-dimensional datasets. -->


## FAQ:

*Any questions or problems that arise, as well as their solutions, can go here.*
