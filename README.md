# sphinx-retina-extension

A Sphinx extension to load low-res or hi-res images depending on the user's screen.

The standard way to managing hi-res images is to append `@2x` to the  filename. The problem is that Sphinx only copies the images that are used to the output folder, so the hi-res images are unavailable in the output.

Use this extension to force the copy or `@2x` images.


## Installation

1.  Copy the `retina_images.py` file to your Sphinx project. For example copy it to the `_ext` folder at the root of the project.
1.  Ensure the extension folder is declared in `conf.py`. For example, insert the following at the top:

    ```python
    sys.path.append(os.path.abspath("./_ext"))
    ```

1.  In `conf.py`, enable the extension:

    ```python
    extensions.append("retina_images")
    ```


## Usage

1. Create 2 versions of each image, one of them with a hight resolution and add the `@2x` prefix. Example: `my_image.png` and `my_image@2x.png`.

1. When you build the project, the `@2x` images are copied to the output folder.

> To see the effect of the extension, you must start a local server, for example using the [auto-reload extension](https://github.com/GaretJax/sphinx-autobuild).