---
id: jsdocs-cluster-manager
title: Cluster Manager
---
<a name="start"></a>

## start(options, [startFunction], [masterFunction])
There are two ways of using this. If you supply a startFunction, invoke this from your
start file. The startFunction will be called when the process is not the master. If startFunction
is not supplied, this method should only be called when Cluster.isMaster is true, and it is up
to the invoker to handle the non-master case.

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the options for the cluster manager |
| [options.count] | <code>int</code> | number of child processes to start. If not set, This will use the env variable CM_MAX_CHILD_PROCESSES or MAX_CHILD_PROCESSES or 32 clamped to the number of cpus to determine the number of child processes to start |
| [options.autoRestart] | <code>boolean</code> | If true, cluster manager will restart a child on exit (default true) |
| options.webServerPort | <code>false</code> \| <code>int</code> | if a port is supplied this will start a web server |
| [options.webServerSetup] | <code>function</code> | optional function to configure the express server |
| [options.adjustRootStatus] | <code>function</code> | a optional intercept to allow you to change the status object  returned by hitting the webServer root |
| options.sendStatusOnRestart | <code>boolean</code> | If true, sends the last status reported by a child to its  reforked replacement (default true) |
| options.updateStatusMs | <code>int</code> | If startFunction is supplied, this is used when connecting to  the parent process to define the status update rate. |
| [startFunction] | <code>function</code> | the function used to start the child processes.  It is only invoked on child processes |
| [masterFunction] | <code>function</code> | this will be called if the process is the master |

