# The Platform API Getting Started Guide

- This README will guide you through the steps required to try out the Platform
  API from [General System](https://www.generalsystem.com).

- OpenAPI endpoint to access the Data Flow Index (DFI) is available at
  <https://api.dataflowindex.io/docs/api>.

- Additional resources and support are available at <https://support.generalsystem.com>.

## Repository Overview

In this quickstart-guide repository you can find a range of [Jupyter Notebooks](https://jupyter.org/)
written in Python with a range of examples of interactions with the DFI platform.

All the notebooks connect to the API via the client library `requests`.
For a more ergonomic approach to connect with a DFI instance, you can also consider the
library [`dfipy`](https://github.com/thegeneralsystem/dfipy) providing direct API
wrappers written in python, as well as the related examples
repository [`dfipy-examples`](https://github.com/thegeneralsystem/dfipy-examples).

## Step 1: Obtain your API token

Access to the demonstration datasets requires an API token, which can be obtained contacting General System [www.generalsystem.com](www.generalsystem.com).

1. Enroll at <https://eap.generalsystem.com> if you have not done so already.
2. Check your inbox for a confirmation email and click the URL link to redeem
   your API token.
3. Additional or replacement API tokens may be obtained from visiting
   <https://tokens.dataflowindex.io/>.

## Step 2: Launch a Jupyter Notebook

The Jupyter Notebooks may be downloaded and installed
locally, or alternatively there are a number of free online options.

### Running On Cloud

To get started, we recommend [Google Colab](https://colab.research.google.com/).

Open the Quick Start guides directly in Google Colab:

1. [dfi_quick_start_geolife.ipynb](https://colab.research.google.com/github/thegeneralsystem/quickstart-guide/blob/main/quickstart_guide/dfi_quick_start_geolife.ipynb)
2. [dfi_quick_start_sys_traffic.ipynb](https://colab.research.google.com/github/thegeneralsystem/quickstart-guide/blob/main/quickstart_guide/dfi_quick_start_syn_traffic.ipynb)
3. [dfi_quick_start_add_new_data.ipynb](https://colab.research.google.com/github/thegeneralsystem/quickstart-guide/blob/main/quickstart_guide/dfi_quick_start_add_new_data.ipynb)

Using <https://mybinder.org>:

1. Open <https://mybinder.org/> in your browser.
2. Enter `https://github.com/thegeneralsystem/quickstart-guide` into the GitHub repository field.
3. Click the launch button.

Our example notebooks make use of the following Python libraries:

- [requests](https://pypi.org/project/requests/) - a simple HTTP library
- [sseclient](https://pypi.org/project/sseclient-py/) - used for iterating over HTTP Server Sent Event streams
- [tabulate](https://pypi.org/project/tabulate/) - used to pretty-print data in a tabular format
- [pydeck](https://pypi.org/project/pydeck/) - bindings for making spatial visualizations with <deck.gl>
- [pandas](https://pypi.org/project/pandas/) - used for making spatial visualizations

Or you can use the [`dfipy`](https://github.com/thegeneralsystem/dfipy) python library wrappers.
Its list of dependencies can be found [here](https://github.com/thegeneralsystem/dfipy/blob/main/pyproject.toml).

### Running Locally

Follow the installation instructions at <https://jupyter.org/install#jupyter-notebook>:

```console
python3 -m pip install dfipy
python3 -m pip install notebook
jupyter notebook
```

## Step 3: Running the example notebooks

Once you have opened the example notebooks from the GitHub URL
`https://github.com/thegeneralsystem/quickstart-guide`, simply follow the
guidance contained within each notebook. You will need to provide your Platform API
token to run the code.

The example notebooks in the `quick_start_guides/` folder are as follows:

| Notebook                             | Description                                                                         |
| :----------------------------------- | :---------------------------------------------------------------------------------- |
| `dfi_quick_start_geolife.ipynb`      | API basics; query a small GeoLife dataset of 25 million records                     |
| `dfi_quick_start_sys_traffic.ipynb`  | Query a large synthetic traffic dataset of 92 billion records using a streaming API |
| `dfi_quick_start_add_new_data.ipynb` | Insert data into an instance                                                        |

## Step 4: consider also the `dfipy` client library

In this quickstart tutorial, you have seen how to access DFI, directly querying on the exposed endpoints via `requests`.

Within DFI we also provide a open source API wrapper: [dfipy](https://github.com/thegeneralsystem/dfipy) This Python package provides a layer of abstraction over the Web API, returning responses in [Pandas](https://pandas.pydata.org/) dataframes. For examples of the usage of `dfipy` you can look under the [examples notebooks](https://github.com/thegeneralsystem/dfipy-examples).

## Licence

- Copyright (c) 2023, General System Group Limited.
- DFIPyExamples is provided as it is and copyrighted under Apache2 License.
- DFIPyExamples is publicly available on github strictly for testing and evaluation purposes.
