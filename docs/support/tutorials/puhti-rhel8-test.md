# Puhti RHEL8 test system documentation

## RHEL8 login nodes

There are two virtualized login nodes available for RHEL8 testing,
`puhti-login11.csc.fi` and `puhti-login12.csc.fi`. These new test
nodes have same `/users`, `/scratch` and `/projappl` folders as current
production setup, so you can test your current installations easily.

!!! Note
    These test system nodes share the same home folder with the
    current production environment. All settings that you have in your
    normal login scripts and environment are visible and active on
    RHEL8 nodes too. Please make sure that you clean your `.bashrc`
    and other relevant files before you log in to the test nodes for
    the first time.

!!! Note
    Lmod caches the module information into your home folder under
    `~/.lmod.d/.cache` and may give you wrong listing of modules when
    working on both RHEL7 and RHEL8 nodes. Please use `--ignore-cache`
    option on module commands or clean the cache folder when
    necessary.

## CPU and GPU nodes with RHEL8

There are three different test partitions that can be used to run
short tests:

| Name      | Nodes | Max jobs | Max run time | Max job size |
|-----------|------:|---------:|-------------:|-------------:|
| rhel8-cpu |    10 |        5 |       30 min |      8 nodes |
| rhel8-gpu |     2 |        2 |       30 min |      2 nodes |
| rhel8-fmi |    12 |        5 |       30 min |     12 nodes |
