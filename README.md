# findbugs-sec

FindBugs + security plugin Docker container

Very much a PoC at this moment. The Dockerfile needs some love.

[Find Security Bugs](http://find-sec-bugs.github.io/) is a promising plugin that extends the old warhorse [FindBugs](http://findbugs.sourceforge.net/). Hopefully the Docker image built from this repository makes it easier to use in certain situations, like CI/CD pipeline.

To run, do something like this. Assuming your source code is under "src" in the current directory:

```
docker pull lokori/findbugs-sec
docker run --rm  -v `pwd`:/workdir/src lokori/findbugs-sec src
```

To get a HTML report in your current working directory out of the Docker container you could try this:
```
 docker run --rm -v `pwd`:/workdir/src lokori/findbugs-sec -html -output /workdir/src/findsec-report.html src
```

Docker volume mount lets the container output the file for you.

 