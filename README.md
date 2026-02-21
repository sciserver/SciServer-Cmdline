# SciServer command-line interface (CLI)

The SciServer command-line interface (CLI) is a tool that allows users to interact with SciServer services and resources directly from the command line. The CLI Python script currently implements basic file operations, such as listing files, uploading files, and downloading files from SciServer.

## Installation

Download `bin/sciserver` and make it executable:

```bash
chmod +x sciserver
```

## Usage

### Authenticate with SciServer:

```bash
eval $(./sciserver login -s -u <username> -p <password>)
```

The authentication token will be stored in the `SS_TOKEN` environment variable for subsequent commands.

### List `persistent` directory contents:

```bash
./sciserver ls ss://Storage/<username>/persistent/
```

### Display help information:

```bash
./sciserver --help
```

# Acknowledgments

The code is based on https://github.com/sciserver/SciScript-Python by mtaghiza et al. but has no dependecies other than `requests` and the standard Python 3 library. It does not provide a Python API, just command-line access to SciServer services.