# HMS Systems Immunology (Fall 2026)

Welcome to Systems Immunology (aka IMMUN 306QC)! 

This Github page contains the workshops that we will be going over throughout the course. The workshops are organized into separate folders. Please note that not all workshops have been uploaded yet — we like to build suspense!

## Schedule

| Date | Lecture<br>9-10:30am<br>Countway Library 104 | Workshop<br>1-3pm<br>TMEC 250 | Deadlines |
| --- | --- | --- | --- |
| Sep. 16, 18, 23, 25* | | Python Bootcamp <br>*(Ralph Estanboulieh)* | | 
| Oct. 9 | **Principles of Systems Immunology** <br>*(all instructors)*  | Python Bootcamp* <br>*(Ralph Estanboulieh)*|  | 
| Oct. 16 | **Transcriptomics** <br>*(Martin Hemberg)* | **RNA sequencing analysis** <br>*(Ralph Estanboulieh, Martin Hemberg)* |  | 
| Oct. 23 | **Tissue and spatial analysis**<br>*(Jeff Moffitt)* | **Single-cell RNA sequencing analysis** <br>*(Ralph Estanboulieh, Martin Hemberg)*|   |
| Oct. 30 | **All that AI will do for Immunology** <br>*(Marinka Zitnik)* | **Spatial analysis** <br>*(Martin Hemberg)*|   |
| Nov. 6 | **Proteomics and immunopeptidomics** <br>*(Jenn Abelin, Nir Hacohen)*| **AI agents for RNA-seq analysis** <br>*(Nir Hacohen)*|   Pre-proposal due Nov. 9 |
| Nov. 13 | \[9am] **T and B cell receptor repertoires** <br>*(Dan Lingwood, Christophe Benoist)* |  | Proposal due Nov. 18|
| | \[1pm] **Perturbations** <br>*(Nir Hacohen, Dave Root)* | |  |
| Nov. 20 | **Applications of systems immunology** <br>*(all instructors)* | Project feedback (as needed) <br>*(Ralph Estanboulieh)*|  |
| Dec. 4 | **Epigenomics**<br>*(Deb Sen)*  | Project feedback (as needed)  <br>*(Ralph Estanboulieh)*|  |
| Dec. 11 | **Student presentations** <br>*(all instructors)*| | |

*: the Python bootcamp might take more than 4-5 sessions.

## Before we start

This course is based on the powerful programming language that is Python (specifically, Python 3). To interact with programming languages, we use something called an integrated development environment (IDE). The IDE of choice for this class is JupyterLab notebooks, which allow us to write normal text, code, and view outputs (including graphs and figures) in the same notebook.

There are two ways you could do the workshops:
1) If you don't want to download any packages on your computer because you are worried about storage or computing space, you can import the notebooks into [Google Colab](https://colab.research.google.com/) and do everything in your browser.
2) If you are willing to download packages on your machine (FYI, there are no security risks involved!), you can follow the guidelines below. I recommend this option especially if you think you will use the tools covered by this course often in your work. I also recommend this option in general because dealing with packages and processing data on your machine is an essential aspect of data analysis.

### Installing Anaconda

(Yet another snake pun!) To code in Python and use Jupyter Lab, you need to install them — and other coding packages — on your computer. Installing packages and libraries can get complicated because each package has its own set of requirements and version compatibilities. Thankfully, we have **package managers** that.. well, manage packages! They do that so seamlessly that all you have to do is ask them to insall or update the package, and they'll figure out the dependencies on their own. 

One very popular and powerful package manager is **Anaconda**. If you do not have Anaconda installed, you can install it by [following these instructions](https://www.anaconda.com/download). Once downloaded and installed, you will have immediate access to Python and Jupyter!

### Using JupyterLab

JupyterLab is a powerful IDE that allows for a very smooth and interactive experience with Python. To open it, follow [these instructions](https://www.anaconda.com/docs/legacy/anaconda-navigator/tutorials/how-to-open-jupyterlab).

We recommend you (at least try) to familiarize yourself with JupyterLab before starting the course. JupyterLabs' extensive documentation can be found [here](https://jupyterlab.readthedocs.io/en/latest/user/index.html), but I recommend starting by watching the video [on their Get Started page](https://jupyterlab.readthedocs.io/en/latest/getting_started/overview.html).

### Learning Python

The first session of this bootcamp will cover Python 101, however, I strongly recommend you check out existing resources and tutorials before coming to the first class. There are at least two highly-rated free online courses available on [Coursera](https://www.coursera.org/learn/python-crash-course) and [MIT OpenCourseWare](https://ocw.mit.edu/courses/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/) (the latter being the course that taught me Python a very long time ago — highly recommended!). If you're really tight on time, I have found at least three good video tutorials on YouTube covering Python basics in [80 minutes](https://www.youtube.com/watch?v=VchuKL44s6E), [30 minutes](https://www.youtube.com/watch?v=WEm3EUdicDg), and a whopping [10 minutes](https://www.youtube.com/watch?v=fWjsdhR3z3c), and I am sure there are many more. Help yourself!


## Navigating GitHub

GitHub is an awesome version control tool to share and maintain code online and collaborate with others on coding projects — all this while also keeping track of all previously uploaded versions and managing the complex situations that arise when multiple people are working on different parts of the same project. All this functionality makes GitHub very powerful and complex, but in this course, we will only need it to share files. While GitHub is the online platform, Git is the version-control software that is locally installed on your machine and which interacts with GitHub.


### Installing Git

There are many ways to install Git on your machine. But before installing it, check that you do not have it installedd by running the command `git` in your Terminal. If you get output that starts with something like `usage: git [-v | --version] [-h | --help]...`, or really anything other than `command not found`, then congratulations! You already have Git on your computer!

If you do not have Git installed, follow the instructions [here](https://git-scm.com/install/). You will notice there are many ways. For macOS, Two common ways are:
1. Using Homebrew, a package manager for macOS, which you can download [from here](https://brew.sh/). Once you have Homebrew install, you can simply run `brew install git` in your Terminal.
2. Apple's core developer toolbox Xcode Command Line Tools, which can easily be installed on macOS with the command `xcode-select --install`, contains Git.

### Using GitHub

Git is a powerful version-control and code-sharing tool. Projects on GitHub (just like this one) are called **repositories** (aka repos). You can copy (aka **clone** in Git-speak) a repo to your computer, make local changes and commit them to the original repo online, pull new versions of the repo, and so on. However, in this course, all you need to do is that first step: to clone (copy) the workshop sessions' contents onto your computer. To do so, run the following command in your terminal:
```
git clone https://github.com/RalphEST/HMS-Systems-Immunology-Fall-2026.git
```
This will automatically create a new folder called `HMS-Systems-Immunology-Fall-2026` which is directly connected to Git and GitHub. (You can find the cloning link for any repo by clicking the bright green `<> Code` button at the top of the page and copying the HTML URL to your clipboard.)

Because the workshops have newly been re-designed for Python, there is a very high likelyhood that the files on GitHub will change after you have cloned the repo. If you want to pull the updated files and simply run the commands:
```
git reset --hard
git pull
```
This will bring all the files up to date **while discarding the local changes you've made**. If you want to keep your edits, you can copy and past the files outside the `HMS-Systems-Immunology-Fall-2026` folder. 




