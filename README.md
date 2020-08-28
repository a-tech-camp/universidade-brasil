# Visual Studio Code

VIsual Studio Code is a text editor. It is popular for its simplicity and extendability. 

## Left Side Navigators
### Folder
We can open a folder in vscode and edit the files as text. This is where we do the majority of the work.

It's worth looking up these folder commands:
 - search for text in files:
    - mac: `command` `shift` `f`
 - search for file:
    - mac: `command` `p`
 - search through command pallete (a series of macro commands that can be looked up):
    - mac: `command` `shift` `p`
    - common commands is _Format Document_ 
   

### Search
Search looks into our files

### Version Control
Track changes on our file and track version history. Has common functionality as git cli, or command line tinerface.

### Debugger
Common debugger tools. Requires configuration. The configuration for these files can be found in `.vscode/launch.json`. You will often need other extensions to integrate breakpoints.

### Extensions
Here we can look for more tools. They will fulfill roles such as:
 - visualization our code
 - UIs for other tools
 - More comprehensive syntax highlighting

A good metric for determining if it's popularity through number of downloads. The more people using it, the more likely there are people maintaining it

Less is more. Extensions will start to conflict especially if you have multiple linters. Get comfortable with them one at a time. 

#### Pinning extensions
Extensions can be pinned into a workspace (or repository or folder) by adding a file called `vscode/extensions.json` with the json object:
```
{
	recommendations:
}
```

For a given

## Further Reading
 - https://code.visualstudio.com/docs/getstarted/userinterface
 