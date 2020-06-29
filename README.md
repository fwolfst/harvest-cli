# Harvest Command Line Interface

### Install jq (json parser for bash)
Mac: `brew install jq`

Win: `chocolatey install jq`

### Setup Harvest app and update config.sh
- Duplicate config.example and rename to config.sh
- Update config.sh with the following variables
- [Create harvest account](https://www.getharvest.com/signup)
- Client: **Isobar** Project: **Coding**
- Visit profile page, get the user id from the url, and update the ```USER_ID``` variable
- Visit projects page -> your project, get the project ID from the url, and update the ``PROJECT`` variable
- Visit [developers page] (https://id.getharvest.com/developers), generate an Access token, and update the ```ACCESS_TOKEN``` & ``` ACCOUNT_ID ``` variable

### Setup complete

## Usage
>Note that any branches with no slash will generate a time entry with an empty message, so if you're on eg. develop, master, use the `hv <message>` command

To be able to use the `hv internal` command, start with creating the internal task using:
`hv newTask internal`


### Usage commands:

        hv                          Toggle timer using git to get task and branchname as message
        hv <message>                Toggle timer using git to get task and with given message
        hv internal <message>       Toggle timer to internal task with given message
        hv stop                     Stops the current timer
        hv note <message>           Add message to current running task
        hv getToday                 Get time summary for today
        hv getToday <yyyy-mm-dd>    Get time summary for given

### Utility commands:

        hv deleteTask               Delete task using current git directory
        hv deleteTask <name>        Delete task using name
        hv newTask                  Create task using current git directory
        hv newTask <name>           Create task using name
        hv getTasks                 Display all tasks info in JSON