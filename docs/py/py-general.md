#  Python Programming Notes
## OS calls

### OS System

```py
import os
os.system("ls -l")
```

```py
import os
stream = os.popen("ls -la")
```

### Subprocess

```py
import subprocess
subprocess.run(["ls", "-l"])
```
Pre 3.5
```py
import subprocess
subprocess.call(["ls", "-l"])
```

## Useful way to call OS commands

```py
def my_func():
    cmd = "ls -l *"
    sp = subprocess.popen(cmd,
        shell=True,
        stdout=subprocess.PIPE,
        stderr=subprocess.PIPE,
        universal_newlines=True)

    out,err=sp.communicate()
    rc=sp.wait()
    print('Return Code:',rc,'\n')
    print('output is: \n', out)
    print('error is: \n', err)
```

 