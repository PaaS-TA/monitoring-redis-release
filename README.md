# paas-ta-monitoring-redis-release

### Create PaaS-TA Monitoring Redis Release   
  - Download the latest PaaS-TA Monitoring Redis Release
    ```   
    $ git clone https://github.com/PaaS-TA/paas-ta-monitoring-redis-release.git
    $ cd paas-ta-monitoring-redis-release
    ```
  - Download & Copy "source files" into the src directory
    ```   
    ## download source files
    $ wget -O src.zip https://nextcloud.paas-ta.org/index.php/s/E2RNq3rXPmGksQp/download

    ## unzip download source files
    $ unzip src.zip

    ## final src directory
    src
     ├── pidutils.sh
     └── redis
        └── redis-4.0.14.tar.gz

    ```
  - Create PaaS-TA Monitoring Redis Release
    ```   
    ## <VERSION> :: release version (e.g. 15.3.5)
    ## <RELEASE_TARBALL_PATH> :: release file path (e.g. /home/ubuntu/workspace/monitoring-influxdb-release-<VERSION>.tgz)
    $ bosh -e <bosh_name> create-release --name=redis --sha2 --version=<VERSION> --tarball=<RELEASE_TARBALL_PATH> --force
    ```
### Deployment
- https://github.com/PaaS-TA/monitoring-deployment
