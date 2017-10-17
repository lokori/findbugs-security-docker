# findbugs-sec

FindBugs + security plugin Docker container

Very much a PoC at this moment. The Dockerfile needs some love.

[Find Security Bugs](http://find-sec-bugs.github.io/) is a promising plugin that extends the old warhorse [FindBugs](http://findbugs.sourceforge.net/). Hopefully the Docker image built from this repository makes it easier to use in certain situations, like CI/CD pipeline.

To run, do something like this:

```
docker pull lokori/findbugs-sec
docker run  -v `pwd`:/workdir/src lokori/findbugs-sec src
```
