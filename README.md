# TensorFlow Tutorial

## Changes from sherrym/tf-tutorial

* Update to tensorflow 1.0.0
* Add new tutorial for TensorBoard
* Use a local virtualenv instead of polluting home directory
* Reworked installation instructions

# Install Tensorflow and Friends

The tutorials run through [Jupyter Notebooks][juypter].

## Clone this repository

Using git, clone this tutorial and enter that directory.

    git clone https://github.com/xtoddx/tf-tutorial.git
    cd tf-tutorial

## Install Pip and Virtualenv

Make sure your base system dependencies for pip and virtualenv,
which are common python tools,
are up to date.
Other packages are installed into a local directory via virtualenv,
so they don't need to be managed manually.

    sudo easy_install --upgrade pip
    sudo pip install --upgrade virtualenv

Now, create a virtual environment.

    virtualenv --system-site-packages .venv

Activate the new virtual environment.
This lets you use an isolated python version and dependency graph.

    source .venv/bin/activate

## Install the dependencies

TODO(todd): move these into requirements.txt

    pip install --upgrade protobuf
    TF_ROOT=https://storage.googleapis.com/tensorflow/mac/cpu/
    TF_WHEEL=tensorflow-1.0.0-py2-none-any.whl
    pip install --upgrade ${TF_ROOT}${TF_WHEEL}
    pip install --upgrade jupyter
    pip install --upgrade Pillow

Matplotlib on OSX is a bit tricky.

    pip install --upgrade matplotlib

You may need to symlink /usr/local/opt/freetype/include/freetype2 to
/usr/local/include/freetype

    brew install freetype
    ln -s /usr/local/opt/freetype/include/freetype2 /usr/local/etc/include/freetype

# Running the Tutorial

Launch the server.
It will automatically launch a new browser window.

    jupyter notebook

For any project in the notebook,
you can step through the blocks using Shift+Enter to execute.
The results are added to the page.

# Watch the Video

[Shery Moore presents Tensor Flow Tutorial][youtube]

[jupyter]: https://jupyter.org/
[youtube]: https://www.youtube.com/watch?v=Ejec3ID_h0w
