# Batch Connect - AweSim AltaSim HeatSinkSim

![GitHub Release](https://img.shields.io/github/release/osc/bc_awesim_altasim_heatsink.svg)
[![GitHub License](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT)

An interactive app designed for AweSim that launches a COMSOL Server
with access to AltaSim's HeatSinkSim app within a Quick batch job.

## Prerequisites

This Batch Connect app requires the following software be installed on the
**compute nodes** that the batch job is intended to run on (**NOT** the
OnDemand node):

- [COMSOL Server](https://www.comsol.com/comsol-server) 5.2a Update 3 or
  greater
- Access to AltaSim's HeatSinkSim app

**Optional** software:

- [Lmod](https://www.tacc.utexas.edu/research-development/tacc-projects/lmod)
  6.0.1+ or any other `module purge` and `module load <modules>` based CLI used
  to load appropriate environments within the batch job before launching the
  COMSOL Server.

> **Warning:**
>
> Care must be taken when installing the COMSOL Server on your cluster such
> that it has a proper Authentication module in place. We recommend setting up
> the LDAP module for the local authentication of your users.

## Install

Use Git to clone this app and checkout the desired branch/version you want to
use:

```sh
scl enable git19 -- git clone <repo>
cd <dir>
scl enable git19 -- git checkout <tag/branch>
```

You will not need to do anything beyond this as all necessary assets are
installed. You will also not need to restart this app as it isn't a Passenger
app.

To update the app you would:

```sh
cd <dir>
scl enable git19 -- git fetch
scl enable git19 -- git checkout <tag/branch>
```

Again, you do not need to restart the app as it isn't a Passenger app.

## Contributing

1. Fork it ( https://github.com/OSC/bc_awesim_altasim_heatsink/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
