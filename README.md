# Monitoring Institutional Ownership Changes with Python and LSEG Ownership Data

## <a id="overview"></a>Overview
Companies use reported ownership data to understand the composition of their shareholder base and identify changes that may warrant further investigation. This notebook demonstrates a programmatic workflow using the LSEG Data Library for Python: retrieve two period-end ownership snapshots for an issuer, compare reported positions, and produce a concise investor watchlist.

The workflow:
1. **Opens** an LSEG Data Library session using LSEG Workspace access.
2. **Retrieves** the latest two quarterly or monthly ownership snapshots for a selected company.
3. **Checks** that the response is complete before comparing the periods.
4. **Identifies** material increases, material reductions, newly reported positions, and positions no longer represented.
5. **Ranks** the flagged investors by materiality and reporting recency.
6. **Presents** the results in a compact watchlist suitable for analyst review, reporting, dashboards, or alerts.

The notebook is a monitoring and operationalization example, not a transaction feed, trading strategy, or stock-performance forecast. It compares reported ownership snapshots and does not infer trade dates, investor intent, or a confirmed sale when an investor is no longer represented. The thresholds and review cadence can be adapted to the issuer and the needs of the analyst or team using the workflow.

Details and concepts are further explained in the [Who Owns Your Company, and What Has Changed?](https://developers.lseg.com/en/article-catalog/article/ownership-monitoring) article published on the [LSEG Developer Community portal](https://developers.lseg.com).


## <a id="disclaimer"></a>Disclaimer
The source code presented in this project has been written by LSEG only for the purpose of illustrating the concepts of creating example scenarios using the LSEG Data Library for Python.

***Note:** To [ask questions](https://community.developers.lseg.com/index.html) and benefit from the learning material, I recommend you to register on the [LSEG Developer Community](https://developers.lseg.com)*

## <a name="prerequisites"></a>Prerequisites

To execute the workbook, refer to the following:

License(s):

- Permissions and API access to Ownership data


[Development Environment](https://developers.lseg.com/en/api-catalog/eikon/eikon-data-api/tutorials#setting-up-a-python-development-environment)

- Tested with Python 3.12.14
- Packages: [lseg-data](https://pypi.org/project/lseg-data/) and [pandas](https://pypi.org/project/pandas/)
- LSEG Data Library for Python installation:  '**pip install lseg-data**'

## <a name="setup"></a>Setup

The package includes a single Jupyter Notebook, [ownership_monitoring_report.ipynb](ownership_monitoring_report.ipynb), demonstrating the monitoring workflow. Users with API access to Ownership data can run the notebook through either supported session type:
* **Desktop session**
  
  Uses Ownership access provided through the LSEG Workspace desktop application.
* **Platform session**
  
  Uses Ownership access provided through the LSEG Data Platform. Configure the session and credentials according to the access available in your environment.

### <a id="authors"></a>Authors

* **Nick Zincone** - Release 1.0. *Initial version*



