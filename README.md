# Message Logging across Orgs and Envs

## Problem Statement
The Message Logging policy requires fixed or hardcoded values for "Host" and "Port", they cannot be set from variables.

How can message logging be configured to log to different Syslog targets for each organization and environment?

## Solution Options

### Maven Configuration - Log-Loggly-SF
Use CI / CD setup with maven to replace the host and port during configure and deployment from source code.

A single Message Logging policy that is modified during the "configure" phase.

See config.json in Log-Loggly-SF folder.

Uses: https://github.com/apigee/apigee-deploy-maven-plugin

### Conditional Policy Execution - Log-Loggly-Orgs-Envs-SF

Use conditional flows based on organization and environment names with separate hardcoded policies for each.

## Usage
Clone this repo and run the maven install command: `mvn -Pyour-profile-name install`
