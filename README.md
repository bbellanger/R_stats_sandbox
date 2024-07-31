# Installation

## Install R
To install the complete R system, use:

```bash
sudo apt-get update
sudo apt-get install r-base
```

Users who need to compile R packages from source [e.g. package maintainers, or anyone installing packages with install.packages()] should also install the r-base-dev package:

```bash
sudo apt-get install r-base-dev
```

## CRAN R kernel for jupyter

Start R in the same terminal, and proceed as below.
You can install the packages via:

```bash
install.packages(c('repr', 'IRdisplay', 'IRkernel'), type = 'source')
```

To update your source installation, repeat above step.

### Making the kernel available to Jupyter
If you haven’t done this already, you will have to make Jupyter see the newly installed R kernel by installing a kernel spec.
The kernel spec can be installed for the current user with the following line from R: 

```bash
IRkernel::installspec()
```

To install system-wide, set user to False in the installspec command:

```bash
IRkernel::installspec(user = FALSE)
```

### Make useful shortcuts available
If you use Jupyter lab (and you should!), install Ryan Homer’s text-shortcuts extension:

```bash
jupyter labextension install @techrah/text-shortcuts
```

