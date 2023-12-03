# DPM360-framework

This repository is for Disease Progression Modeling workbench 360 - an end-to-end deep learning model training framework in Python on OHDSI-OMOP data.

You can check out the overview and YouTube demonstration [here](https://bestdrave.github.io/DPM360/). You'll also find the license, contribution guide, and publications there.

Major components of the DPM360 project is depicted in the figure below.

<figure><center><img src=./docs/resources/png/dpm360v2.png "DPM360" width="300"/></center><figcaption>DPM360 Component View</figcaption></figure>

# Installation Guides

DPM360 components can work together or as standalone elements. DPM360 is usually set up over a cluster with various interconnected micro-services. The components can be divided into two groups: (i) components for micro service setups, and (ii) standalone Python packages offering core functionalities, each having its own installation procedure.

Detailed guides for each component are provided below.

## DPM360 micro-service utilities

One of the key micro-service utilities is the **installer** that sets up an OHDSI stack (Atlas, WebAPI, a Postgres Database, and Achilles) into a cloud cluster such as Kubernetes or OpenShift. For more details, see the [installation guide](installer/docs/installer.md).

The **service builder** component packages and deploys the learned models to the target cloud cluster. You can check its [installation guide](service_builder/docs/README.md) for more details.

## DPM360 standalone Python packages

The **lightsaber** component is a Python training framework. You can refer to the [installation guide](lightsaber/docs/install.md) and [user guide](lightsaber/docs/user_guide.md) for details.

The **cohort tools** component provides Python scripts to extract features from cohorts defined via ATLAS or custom queries. It can be integrated with lightsaber to use features extracted from OHDSI databases. For more information, check out the [user guide](cohort_tools/docs/user_guide.md).