# Torque Orb for CircleCI

[![CircleCI](https://circleci.com/gh/QualiTorque/torque-orb/tree/master.svg?style=svg)](https://circleci.com/gh/QualiTorque/torque-orb/tree/master)

## The Torque Orb

Torque provides on-demands sandbox environments integrating with test tools and storage providers to pull
the artifacts and push to Production.

Using this orb you can integrate the Torque sandboxes into your CI/CD pipeline configure in CircleCI

## How to use Torque Orb

1. Follow the instructions at the [Orb Quick Start Guide](https://circleci.com/orbs/registry/orb/quali/torque#quick-start) to enable usage of Orbs in your projects workflow.
2. Set up the following environment variables in CircleCI project settings:

    `TORQUE_SERVER` - The url of Torque server
    
    `TORQUE_TOKEN` - The Torque Token which could be generate on integrations page of Torque Settings

    `TORQUE_SPACE` - The name of your Torque space
 
3. In the config.yml, call the `torque/start-sandbox` and `torque/end-sandbox` to start and stop 
sandbox in Torque
4. Supply parameters to customize orb behaviour (see the list of parameters for orb commands [here](https://circleci.com/orbs/registry/orb/quali/torque#commands) 
5. After starting Torque sandbox (`torque/start-sandbox` command) you can use the following environment
variables in your job steps (the names of variable could be overridden):

    `SANDBOX_ID` - the id of launched sandbox
    
    `SANDBOX_DETAILS` - the full description of sandbox in json format
    
    `SB_<SANDBOX_ID>_SHORTCUT_<1...N>` - quick links of the sandbox
