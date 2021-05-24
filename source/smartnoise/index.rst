SmartNoise
==========

**Contents:**

.. toctree::

   quickstart
   api-reference/index


Introduction
============

The SmartNoise project provides:

- A pluggable open source library of differentially private algorithms and mechanisms for releasing privacy preserving queries and statistics.
- APIs for defining an analysis and a validator for evaluating these analyses and composing the total privacy loss on a dataset.
- An SDK with tools which allow researchers and analysts to:
   - Use SQL dialect to create differentially private results over tabular data stores.
   - Host a service to compose queries from heterogeneous differential privacy modules (including non-SQL) against shared privacy budget
   - Perform privacy algorithm stochastic testing against differential privacy modules

The mechanisms library provides a fast, memory-safe native runtime for validating and running differentially private analyses. The runtime and validator are built in Rust, while Python support.

Differentially private computations are specified as an analysis graph that can be validated and executed to produce differentially private releases of data. Releases include metadata about accuracy of outputs and the complete privacy cost of the analysis.


SmartNoise Repository Orientation
---------------------------------

SmartNoise project includes four GitHub repositories:
(Don't worry about remembering them all. In practice, use of SmartNoise normally includes installation of a single python package as shown in the next section: `Quickstart and Notebooks`_.)

1. `smartnoise-core`_ - A `Rust`_ runtime and validator which include an `extensive set of components (Rust docs)`_
2. `smartnoise-core-python`_ - Python bindings which provide access to the `components (Python docs)`_.
3. `smartnoise-sdk`_ - The SDK includes tools built upon the  Python bindings.
4. `smartnoise-samples`_ - A set of exemplar notebooks which range from demonstrating basic functionality and utility to showing how to create synthetic data with high utility for machine learning.

.. _Quickstart and Notebooks: https://docs.opendp.org/en/main/smartnoise/index.rst#quickstart-and-notebooks
.. _smartnoise-core: https://github.com/opendp/smartnoise-core
.. _smartnoise-core-python: https://github.com/opendp/smartnoise-core-python
.. _smartnoise-sdk: https://github.com/opendp/smartnoise-sdk
.. _smartnoise-samples: https://github.com/opendp/smartnoise-samples
.. _extensive set of components (Rust docs): https://opendp.github.io/smartnoise-core/doc/smartnoise_validator/docs/components/index.html
.. _Python bindings: https://docs.opendp.org/en/main/smartnoise/api-reference/opendp.smartnoise.core.components.html
.. _components (Python docs): https://docs.opendp.org/en/main/smartnoise/api-reference/opendp.smartnoise.core.components.html

.. _Rust: https://todo-WHY-RUST


.. _SmartNoise Installation:

Quickstart and Notebooks
------------------------

In practice, full SmartNoise functionality is available through a single `Python package`_ which is compatible with Python 3.6 to 3.8:

.. _Python package: https://pypi.org/project/opendp-smartnoise/


.. code-block:: python

   pip install opendp-smartnoise

This package gives access to all of the `SmartNoise core components`_ as well as the `SmartNoise SDK`_.

.. _SmartNoise core components: https://docs.opendp.org/en/main/smartnoise/api-reference/opendp.smartnoise.core.components.html
.. _SmartNoise SDK: https://github.com/opendp/smartnoise-sdk

To best way to get started with SmartNoise is by reviewing and trying examples from the repository `smartnoise-samples`_ notebooks which includes:

.. _smartnoise-samples: SDK: https://github.com/opendp/smartnoise-samples

- `Sample Analysis Notebooks`_  includes a brief tutorial as well as SmartNoise examples of histograms, differentially private covariance, how dataset size and privacy-loss parameter selection impact utility, and working with unknown dataset sizes.
- `Attack Notebooks`_ demonstrate how SmartNoise mitigate a basic attack and as well as a database reconstruction attack.
- `SmartNoise Whitepaper Demo Notebooks`_ Based on the whitepaper titled `Microsoft SmartNoise Differential Privacy Machine Learning Case Studies`_ these notebooks include a demonstration of how to perform supervised machine with differential privac and an example of creating synthetic data with high utility for machine learning as well as examples of creating DP releases with histograms and protecting against a reidentification attack.

.. _Sample Analysis Notebooks: https://github.com/opendp/smartnoise-samples/tree/master/analysis
.. _Attack Notebooks: https://github.com/opendp/smartnoise-samples/tree/docs-notebooks/attacks
.. _Microsoft SmartNoise Differential Privacy Machine Learning Case Studies: https://azure.microsoft.com/en-us/resources/microsoft-smartnoisedifferential-privacy-machine-learning-case-studies/
.. _SmartNoise Whitepaper Demo Notebooks: https://github.com/opendp/smartnoise-samples/tree/master/whitepaper-demos