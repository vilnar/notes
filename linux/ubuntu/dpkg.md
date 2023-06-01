## dpkg

install
```sh
dpkg -i {package_name}
```

remove
```sh
dpkg -r {package_name}
```

### Listing All Installed Packages

```sh
dpkg -l | grep manticore
```

Understanding dpkg Output
The first column will show 2 characters showing the package’s status (In the previous screenshot, “i”). Each letter has its own meaning, where the first shows desired package status as explained in the first line of the output. Possible desired status include:
i: The package is chosen to be installed.
r: The package is chosen to be removed.
p: The package is chosen to be purged (Removed, including all related files and directories).
u: The package status is unknown.
h: The package is kept and not managed by dpkg.
The second character (in the screenshot below also “i”) shows the package’s current status. Therefore if the second character is “r” and the first character is “i,” the meaning is the package is currently installed but selected for removal by the user. There are 8 possible letters for a package’s current status:
i: The package is installed.
n: The package is not installed in the system.
c: The package is not installed, but its configuration files remain.
f: The system failed to remove configuration files.
u: The package is unpacked.
h: The package installation started but wasn’t installed for an unknown reason.
f: The package was unpacked and partially configured but not installed for an unknown reason.
w: The package is waiting to be triggered by another package.
t: The package has been triggered by another package.
The second column displays package names.
The third column shows package versions.
The fourth column shows package architecture.
Finally, the fifth column shows package descriptions.

