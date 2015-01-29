# StrongLoop Arc load-balancer

Provides load-balancing support for multiple strong-pm instances configured and
run using StrongLoop Arc.

Please see the [official documentation](http://docs.strongloop.com/display/ARC).

## Install

### Prerequisite:

* You must have [Node.js](http://nodejs.org) installed.
* You must have [Nginx](http://nginx.org/) installed.

### Install using `npm` as follows:

```sh
$ npm install -g strong-arc-lb
```

## Usage

```
usage: sl-arc-lb [options]

Options:
  -h,--help             Print this message and exit.
  -v,--version          Print version and exit.
  -b,--base BASE        Base directory to work in (default is .strong-arc-lb).
  -c,--control CONTROL  Control API endpoint (Default http://0.0.0.0:0)
  -l,--listen ENDPOINT  Listen ENDPOINT for incoming HTTP traffic
                          (Default: http://0.0.0.0:8080)
  -x,--nginx            Path to Nginx binary (Default: /usr/sbin/nginx)
```

## Install

```
usage: sl-arc-lb-install [options]

Options:
  -h,--help             Print this message and exit.
  -v,--version          Print version and exit.
  -b,--base BASE        Base directory to work in (default is .strong-arc-lb).
  -u,--user USER        User to run manager as (default is strong-arc-lb).
  -c,--control CONTROL  Control API endpoint (Default http://0.0.0.0:0)
  -l,--listen ENDPOINT  Listen ENDPOINT for incoming HTTP traffic
                        (Default: http://0.0.0.0:8080)
  -n,--dry-run          Don't write any files.
  -j,--job-file FILE    Path of Upstart job to create (default is
                        /etc/init/strong-arc-lb.conf)
  -f,--force            Overwrite existing job file if present
  -x,--nginx            Path to Nginx binary (Default: /usr/sbin/nginx)
  --upstart VERSION     Specify the version of Upstart, 1.4 or 0.6
                        (default is 1.4)
  --systemd             Install as a systemd service, not an Upstart job.

OS Service support:
  The --systemd and --upstart VERSION options are mutually exclusive.
  If neither is specified, the service is installed as an Upstart job
  using a template that assumes Upstart 1.4 or higher.
```
