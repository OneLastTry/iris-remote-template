# InterSystems IRIS Remote Connection for VSCode Template

This template allow easy setup of VSCode (leveraging [InterSystems ObjectScript Extension](https://marketplace.visualstudio.com/items?itemName=intersystems-community.vscode-objectscript)) to connect to InterSystems IRIS products.

[remote-template.code-workspace](remote-template.code-workspace) holds configuration such as:

- Physical address of the code in the project structure
- Logical name where the code is stored
- InterSystems IRIS network address
- InterSystems IRIS web port
- InterSystems IRIS username (password will be prompted when connection is established)

While [settings.json](code/user/.vscode/settings.json) can be used to specify the namespace.

In order to maintain the code organized, create separate folders for separate namespaces under [code](code/). If reusing the existing [user](code/user/) folder for a namespace named anything other than _user_, make sure to rename the folder and change the relevant places in [remote-template.code-workspace](remote-template.code-workspace) and [settings.json](code/user/.vscode/settings.json).

To create a new namespace simply copy and rename the [user](code/user/) folder, also making sure to change the relevant places on the new structure.

One example of changing the namespace would be like below:

```json
// my new connection to a namespace called MYNS
{
    "objectscript.conn": {
        "active": true,
        "server": "remote",
        "ns": "MYNS"            // IRIS namespace
    }
}
```
