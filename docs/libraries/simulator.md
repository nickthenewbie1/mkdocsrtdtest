---
id: libReadmes-simulator
title: Simulator
---

# Simulator

Simulator is a tool for simulating IoT devices within the Leverege Platform.

## Configuration

Simulator runs as a stateful service that manages simulated devices, and generates data that pertains to the specification of the simulated devices.

| ENV Variable | Description |
| --- | --- |
| MODEL_FIREBASE_SERVICE_ACCOUNT | service account for the model Firebase database |
| MODEL_FIREBASE_DATABASE_URL | URL of the model Firebase database |
| DATA_FIREBASE_DATABASE_URL | URL of the data Firebase database |
| DATA_FIREBASE_SERVICE_ACCOUNT | service account for the data Firebase database |
| TRANSPORT_CONFIG | configuration to be passed into the [Message Queue](http://docs.leverege.com/docs/message-queue) |
| PORT | the port the Imagine server will run on |

## Simulated Devices

Simulator is capable of simulating many devices at the same time, and each device is configured at run-time individually.

Devices consist of several components aggregated together. Namely:

- a set of updaters
  - exist in a one-to-one relationship with blueprint attributes for the device
  - have many different ways of updating
- a behavior
  - determines how the device sends messages
  - can either send messages as generated, or aggregate them over time and send a package of messages all at once
- a connector
  - specifies how a device connects to the Leverege Platform
  - most used uses message-queue library

Devices have an overall state that determines whether or not they are sending data, they are:

- initialized (coming up but not sending data)
- pause (not sending data)
- play (sending data)
- stopped (shutting down, not sending data)

### Updaters

Updaters are the most used and most variable aspect of a simulated device. They can generate values in several different ways, as specified below.

| Updater Type | Description |
| --- | --- |
| collection | generates values as specified by an array of child updaters with specified ttl's |
| constant | repeatedly generates the same value specified in the updater config |
| controlled | essentially a constant updater, but the value can be changed externally by a user |
| function | generates a value based on the device's other updater values, time, and an input function |
| jitter | generates values that jitter randomly or randomly around an initial value |
| list | generates values from a specified list with specified gaps of time between them |
| null | does nothing, this is a placeholder updater |
| randomBoolean | generates true or false randomly |
| randomNumber | randomly generates a number in a range |

### Scenarios

Scenarios are objects that can be played on a device that take control of a subset of the device's updaters. This allows the scenario to generate values on that device. Scecnarios can loop, allowing the scenario behavior to play over a device continuously. This is useful, for example, when simulating running the same route repeatedly.

#### Structure

| field | description |
| --- | --- |
| behavior | a behavior object to control the device |
| updater | a set of updaters in an object that can take control of different data paths in the device |
| updater.\<path\> | an updater object to be put in place at the specified path on the device |