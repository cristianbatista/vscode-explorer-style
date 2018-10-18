# vscode-style-explorer
Increases indentation on the file tree and adds some lines to each directory/file

![alt text](https://github.com/cristianbatista/vscode-style-explorer/blob/master/images/explorer.png)

### Instructions
* install extension "Custom CSS and JS" 
* grant permission for extesion "Custom CSS and JS"
```
#For VSCode:
sudo chown -R $(whoami) /usr/share/code

#For VSCode Insiders:
sudo chown -R $(whoami) /usr/share/code-insiders
```
* create file "tree.css", include the code:

```
.monaco-tree-row {
	overflow: hidden;
	position: relative;
}

.monaco-tree-row:before {
	content: '';
	background: rgba(255, 255, 255, 0.4);
	position: absolute;
	width: 1px;
	height: 100%;
}

.monaco-tree-row:after {
	content: '';
	background: rgba(255, 255, 255, 0.4);
	position: absolute;
	width: 14px;
	height: 1px;
	top: 50%;
}

.monaco-tree-row:not([aria-level="1"]):not([aria-level="2"]):before {
	box-shadow:  -20px 0Open Preferences > Settings, and add this settin 0 0 rgba(255, 255, 255, 0.4),
				 -40px 0 0 0 rgba(255, 255, 255, 0.4),
				 -60px 0 0 0 rgba(255, 255, 255, 0.4),
				 -80px 0 0 0 rgba(255, 255, 255, 0.4),
				-100px 0 0 0 rgba(255, 255, 255, 0.4),
				-120px 0 0 0 rgba(255, 255, 255, 0.4),
				-140px 0 0 0 rgba(255, 255, 255, 0.4),
				-160px 0 0 0 rgba(255, 255, 255, 0.4),
				-180px 0 0 0 rgba(255, 255, 255, 0.4),
				-200px 0 0 0 rgba(255, 255, 255, 0.4),
				-220px 0 0 0 rgba(255, 255, 255, 0.4),
				-240px 0 0 0 rgba(255, 255, 255, 0.4),
				-260px 0 0 0 rgba(255, 255, 255, 0.4);
}

.monaco-tree-row[aria-level="1"]  { padding-left:   0px !important; }
.monaco-tree-row[aria-level="2"]  { padding-left:  20px !important; }
.monaco-tree-row[aria-level="3"]  { padding-left:  40px !important; }
.monaco-tree-row[aria-level="4"]  { padding-left:  60px !important; }
.monaco-tree-row[aria-level="5"]  { padding-left:  80px !important; }
.monaco-tree-row[aria-level="6"]  { padding-left: 100px !important; }
.monaco-tree-row[aria-level="7"]  { padding-left: 120px !important; }
.monaco-tree-row[aria-level="8"]  { padding-left: 140px !important; }
.monaco-tree-row[aria-level="9"]  { padding-left: 160px !important; }
.monaco-tree-row[aria-level="10"] { padding-left: 180px !important; }
.monaco-tree-row[aria-level="11"] { padding-left: 200px !important; }
.monaco-tree-row[aria-level="12"] { padding-left: 220px !important; }
.monaco-tree-row[aria-level="13"] { padding-left: 240px !important; }
.monaco-tree-row[aria-level="14"] { padding-left: 260px !important; }
.monaco-tree-row[aria-level="15"] { padding-left: 280px !important; }

.monaco-tree-row[aria-level="1"]:before { display: none; }
.monaco-tree-row[aria-level="2"]:before   { left:  11px; }
.monaco-tree-row[aria-level="3"]:before   { left:  31px; }
.monaco-tree-row[aria-level="4"]:before   { left:  51px; }
.monaco-tree-row[aria-level="5"]:before   { left:  71px; }
.monaco-tree-row[aria-level="6"]:before   { left: 91px; }
.monaco-tree-row[aria-level="7"]:before   { left: 111px; }
.monaco-tree-row[aria-level="8"]:before   { left: 131px; }
.monaco-tree-row[aria-level="9"]:before   { left: 151px; }
.monaco-tree-row[aria-level="10"]:before  { left: 171px; }
.monaco-tree-row[aria-level="11"]:before  { left: 191px; }
.monaco-tree-row[aria-level="12"]:before  { left: 211px; }
.monaco-tree-row[aria-level="13"]:before  { left: 231px; }
.monaco-tree-row[aria-level="14"]:before  { left: 251px; }
.monaco-tree-row[aria-level="15"]:before  { left: 271px; }

.monaco-tree-row[aria-level="1"]:after { display: none; }
.monaco-tree-row[aria-level="2"]:after   { left:  11px; }
.monaco-tree-row[aria-level="3"]:after   { left:  31px; }
.monaco-tree-row[aria-level="4"]:after   { left:  51px; }
.monaco-tree-row[aria-level="5"]:after   { left:  71px; }
.monaco-tree-row[aria-level="6"]:after   { left: 91px; }
.monaco-tree-row[aria-level="7"]:after   { left: 111px; }
.monaco-tree-row[aria-level="8"]:after   { left: 131px; }
.monaco-tree-row[aria-level="9"]:after   { left: 151px; }
.monaco-tree-row[aria-level="10"]:after  { left: 171px; }
.monaco-tree-row[aria-level="11"]:after  { left: 191px; }
.monaco-tree-row[aria-level="12"]:after  { left: 211px; }
.monaco-tree-row[aria-level="13"]:after  { left: 231px; }
.monaco-tree-row[aria-level="14"]:after  { left: 251px; }
.monaco-tree-row[aria-level="15"]:after  { left: 271px; }
```
* Open Preferences > Settings, and add this setting:
```
 "vscode_custom_css.imports": [
        "file:///Users/semenov/.vscode/css/tree.css"
    ]
```
* Open "Command Palette" in VSCode (View -> Command Palette), input the command: "Reload Custom CSS and JS"
* Restart VSCode
