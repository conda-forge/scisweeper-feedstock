About scisweeper
================

Home: https://github.com/scisweeper/scisweeper

Package license: BSD-3-Clause

Feedstock license: BSD 3-Clause

Summary: scientific parameter sweeper, with easy debugging capabilities and an interface for most scientific queuing systems.

scisweeper is a utility for parameter sweeps in a scientific environment.
By defining the write_input and collect_output function, as well as a
link to the executable the users can link scisweeper to their own code.
Afterwards scisweeper can execute the parameter sweep either locally
using a given number of parallel threads or submit the individual
calculations to a queuing system like LFS, MOAB, SGE, SLURM, or TORQUE
using the built-in interface to pysqa. After the calculations are
finished the results are summarized in a pandas.DataFrame, which makes
them easily accessible for machine learning tools like tensorflow or
pytorch. Coming from a scientific environment scisweeper was develop
with a focus on debugging. Broken jobs can be identified, executed again
manually or deleted and in case you need to update the collect_output
function there is no need to execute the calculations again, the output
can be parsed separatly to update the results in the pandas.DataFrame.


Current build status
====================


<table><tr><td>All platforms:</td>
    <td>
      <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=7393&branchName=master">
        <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/scisweeper-feedstock?branchName=master">
      </a>
    </td>
  </tr>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-scisweeper-green.svg)](https://anaconda.org/conda-forge/scisweeper) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/scisweeper.svg)](https://anaconda.org/conda-forge/scisweeper) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/scisweeper.svg)](https://anaconda.org/conda-forge/scisweeper) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/scisweeper.svg)](https://anaconda.org/conda-forge/scisweeper) |

Installing scisweeper
=====================

Installing `scisweeper` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
```

Once the `conda-forge` channel has been enabled, `scisweeper` can be installed with:

```
conda install scisweeper
```

It is possible to list all of the versions of `scisweeper` available on your platform with:

```
conda search scisweeper --channel conda-forge
```


About conda-forge
=================

[![Powered by NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](http://numfocus.org)

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[CircleCI](https://circleci.com/), [AppVeyor](https://www.appveyor.com/)
and [TravisCI](https://travis-ci.org/) it is possible to build and upload installable
packages to the [conda-forge](https://anaconda.org/conda-forge)
[Anaconda-Cloud](https://anaconda.org/) channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](https://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating scisweeper-feedstock
=============================

If you would like to improve the scisweeper recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/scisweeper-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@jan-janssen](https://github.com/jan-janssen/)

