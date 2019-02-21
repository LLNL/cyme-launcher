# CYME Launcher

CYME Launcher is a Go program that helps with starting up CYME using WINE on Linux, in a way that works with HPC clusters. It makes sure that a license manager with available licenses is running, and handles the arguments needed by WINE to launch the CYME gui as well as run Python scripts using cympy.

## Installation

Use `go build cyme-launcher.go` to compile a self-contained executable. Or use `go run cyme-launcher.go` to run the launcher as if it were a script. X forwarding must be enabled to run CYME from an SSH session (or a virtual X11 framebuffer server should be used, such as using `xvfb-run` to run `cyme-launcher`). 

## Usage

The following options are supported for setting up paths:

```
-cymepath string
    path to the cyme installation (default "C:\\Program Files\\CYME\\CYME")
-hasplmpath string
    the path to the hasplm daemon (default "/usr/workspace/wsb/cyme/sentinel_lm")
-hasplmserver string
    remote hasplm server to use (default "eng-tools4.llnl.gov")
-python string
    python script to run
-winepath string
    the root path where wine is installed
-wineprefix string
    the wine prefix to use (default "/usr/workspace/wsb/cyme/wine32_prefix")
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


