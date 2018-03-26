# Dockerfiles

There are several `Dockerfile` files within subdirectories that we make sure of
to build out our container images. These `Dockerfile`s are intended to be
consumed from the root of the repository.

Directories consist of:

* **builder**: The base `ONBUILD` image for the multi-stage build of the
  metrics and events consumers.
* **events**: Used to build the events consumer.
* **metrics**: Used to build the metrics consumer.
* **qdr**: QPID Dispatch Router. Consumes a newer version of QPID Dispatch
  Router than what is available in Fedora 27 currently. RPMs are built from the
  `<root>/qdr/buildit.sh` script.
