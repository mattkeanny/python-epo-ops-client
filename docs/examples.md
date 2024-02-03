# Usage of the python-epo-ops-client

The `python-epo-ops-client` library provides an easy-to-use Python interface to  
the European Patent Office's Open Patent Services (OPS). Below, you'll find various  
examples to help you get started and make the most out of the library.  

## Table of Contents

1. [Getting Started](#getting-started)
2. [Searching for Patents](#searching-for-patents)
3. [Retrieving Patent Details](#retrieving-patent-details)
4. [Downloading Patent Documents](#downloading-patent-documents)

## Getting Started

To use the library, you need to have an OPS user account, then install the library and  
configure your OPS credentials.

### OPS Account Setup

1.  [Sign up for an OPS user login with the EPO][ops registration].  
2.  Create an App at the OPS Console, which will provide you with a corresponding  
    pair of authentication credentials, the OPS application key and its secret.  

### Credentials setup

Before using the library, you will need to define the `OPS_KEY`,and `OPS_SECRET`  
environment variables.

You can either define them interactively using `export VARNAME=VALUE`, or store  
them into an `.env` file within the same directory you are running the tests from.  
Here an example `.env` file.  

```shell
export OPS_KEY=NKdGMmedZBGLRxTrUwCZMQCYp7Ak5a0u
export OPS_SECRET=v3vARPu7DFPEDB8i
```

_Note that the OPS credentials have been invalidated for demonstration purposes._  

### Installation

Go ahead and install the `python-epo-ops-client`:  

```bash
pip install python-epo-ops-client
```

### Setup

Instantiate a client using your OPS credentials.  

```python
from epo_ops import Client
client = Client(key='your-consumer-key', secret='your-consumer-secret')  # Replace with your actual credentials
```

[ops registration]: https://developers.epo.org/user/register