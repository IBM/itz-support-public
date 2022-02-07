# Skytap Auto-Shutdown/Suspend Timer

## All Skytap Environments provisioned through IBM Technology Zone have an Automatic shutdown/suspend timer.  This is an amount of idle time that varies by environment, after that time the Environment will shutdown/suspend.  

### The following activities prevent auto-shutdown (the environment stays active):

There is keyboard or mouse activity in a VM browser client session or sharing portals session.

An API script checks or makes a change to a VM or the environment (see Using the API with auto-suspend).

A VM script sends a “keep-alive” message to the Skytap metadata service (see Sending keep-alive messages from a VM to prevent automatic shutdown or suspend).

A signed in user or administrator is viewing the Environment Details page for the environment.

A VM in the environment was started (run) within the previous 30 minutes

###  By default, Skytap does not check for active connections over published services or public IP addresses.

To prevent a VM from shutting down or suspending while published services or other unmonitored services are in use, run a script that periodically sends keep-alive messages to Skytap. For instructions, see Sending keep-alive messages from a VM to prevent automatic shutdown or suspend.

Full Information can be found here, https://help.skytap.com/auto-shutdown.html.

### Support

For any questions, contact ITZ support - techzone.help@ibm.com
