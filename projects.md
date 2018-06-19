---
layout: page
title: Project results
---


## Project descriptions and reports

### ThebeLab

- Prepared and delivered a demo; now included in ThebeLab's [examples](https://github.com/minrk/thebelab/tree/master/examples) directory
- [GAP demo](https://sebasguts.github.io/thebelab_test_gap/chap42)
- [SageMath demo](http://sage-package.readthedocs.io/en/latest/sage_package/sphinx-demo.html) ([about](http://sage-package.readthedocs.io/en/latest/sage_package/thebe.html))
- Improved ThebeLab's documentation
- Finalized [Sage's ticket](https://trac.sagemath.org/ticket/24593) enabling live documentation with ThebeLab
- Experiments to turn GAP documentation into live documentation using ThebeLab

### Around Binder

- [Alternative deployment on EGI's cloud](https://binderhub-jupyter.fedcloud-tf.fedcloud.eu/)
- Fix the alternative deployement and upgrade its docker

### Docker image for GAP

- Update the official GAP Docker to 4.9.1
- Update the GAP Docker Master image
- Test GAP Docker containers after updates and cleaning up old issues in their repositories
- Use GAP Docker Master to create a Binder-ready image
    - Add Jupyter to it
    - Provide fixed tags
    - Provide a boiler-plate repo that shows how to use gap-docker-master on binder [gap-system/gap-docker-binder](https://github.com/gap-system/gap-docker-binder) [![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/gap-system/gap-docker-binder/master)
    - Provide a Readme

### Jupyter kernel for GAP

- Multiple Bugfixes on Jupyter Kernel
- Added visjs demo to JupyterKernel repo: examples to work with graphs either by nodes and edges, or using dot language.
- Created [FrancyMonoids package](https://gap-packages.github.io/FrancyMonoids)
- Working on francy async branch errors
- Added dot functions to the [NumericalSgps package](https://gap-packages.github.io/numericalsgps) to be used either with `JupyterSplashDot` or with the provided function `DotSplash`
- Make syntax errors and warnings show in red
  - Make use of error output stream consistent in GAP
- Checked that we support latest version of Jupyter protocol (5.3 at the time of writing).
- Fix to GAP's Help to make Jupyter help display work again
- Fix indenting in the syntax highlighting: [gap-packages/JupyterKernel/pull/46](https://github.com/gap-packages/JupyterKernel/pull/46)
- Explore viz.js as an alternative to command line `graphviz`: see [`DotSplash`](https://github.com/pedritomelenas/dot-numericalsgps/blob/08edd05783440f7618da57096c622efc9dd4a33d/dot.gi#L23) in dot-numericalsgps repo or provide a way to choose engine in `JupyterSplashDot`
- Look at [inorder.js](https://github.com/minrk/ipython_extensions/blob/master/nbextensions/inorder.js) and see if we can use it to adress some wishes for using Jupyter in teaching
- Deposit JupyterKernel and Dependencies (uuid, crypting) with GAP for 4.9.2

### GAP Package development

- [FSR package](https://github.com/nzidaric/gap-fsr)
  - Set up Travis CI and CodeCov integration
  - Make a website using [GitHubPagesForGAP](https://github.com/gap-system/GitHubPagesForGAP)
  - Make a beta-release using [ReleaseTools](https://github.com/gap-system/ReleaseTools)
- Get CurlInterface and the Debugger released for distribution
- Update the build system of ~20 GAP packages to take advantage of GAP 4.9 improvements; also several other pull requests for those package fixing various other minor issues

### libgap

Goal: push further the integration of GAP's own libgap implementation, and experiment with it from Sage, Julia, ...
- Created a plan for the future libgap development
- Extracted and analyzed the [GAP symbols used by Sage](https://hackmd.io/emNi76svSWCh1fBeLKqPdA#)
- Try the latest libgap in Sage

### libsemigroups

- Wrote and [published on binder](https://mybinder.org/v2/gh/james-d-mitchell/libsemigroups/binder?filepath=index.ipynb) a sample notebook illustrating the interactive use of libsemigroups with cling
- Lots of improvements to libsemigroups

#### Python/Sage bindings

In the Cernay meeting we started exploring the use of cppyy to obtain bindings for libsemigroups. The technology looks very promissing but still on the bleeding edge: it tends to segfault due to bugs in cppyy.
Bugs analyzed, reduced, and reported upstream:
- [#24, explicit constructors](https://bitbucket.org/wlav/cppyy/issues/24) fixed
- [#28, virtual destructor, array refcounting](https://bitbucket.org/wlav/cppyy/issues/28) fixed
- [#30, private numbers](https://bitbucket.org/wlav/cppyy/issues/30) fixed

With the fixes, a non trivial part of libsemigroups works now smoothly:
- Basic elements: transformations, ...
- Semigroups of elements preexisting types
- Semigroups of Python objects

### Notebook collection website for ODK and GAP

Current version available in Sebastian Gutsche's [try branch](https://github.com/sebasguts/OpenDreamKit.github.io/tree/try)


### Experimenting with Azure

- Try to use GAP in Azure Notebooks
- Try https://docs.microsoft.com/en-us/azure/container-instances/container-instances-quickstart-portal

## Results of GAP Developers meeting

### General

- Develop a roadmap for refactoring the REPL in GAP to better support libGAP/JuPyter and generally be more flexible

### Discuss GAP release/development cycle 

- Suggested release schedule for GAP 4.10.
  - 2018-11-01 release of GAP 4.10.1 (first user release)
  - 2018-10-01 release of GAP 4.10.0
  - 2018-09-17 prepare changelog (during GAP days)
  - 2018-09-01 branching of stable-4.10

### OpenDreamKit

- [Brainstorm discussion on ODK D6.9: persistent memoization library](https://hackmd.io/1M5clex-TYWCuxxgi05k5A)
- [MitM brainstorm](https://hackmd.io/13i3MB8IQse2uY2lcYuHOw#) (Markus, Nicolas)


