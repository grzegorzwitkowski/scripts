scripts
=======

useful scripts for developers

**switchversion** switch between different versions of tools like jdk or gradle

Lets say you have installed two versions of jdk:

* /home/john.doe/tools/jdk1.7.0_65
* /home/john.doe/tools/jdk1.8.0_20

and have symbolic link to one of these added to path

```
/home/john.doe/tools/jdk -> /home/john.doe/tools/jdk1.7.0_65
PATH=$PATH:/home/john.doe/tools/jdk/bin
```

By using this script you can easily switch between these 2 versions by typing:

```
switchversion jdk 1.8
```

To do that you need to configure tools dictionary in the script to follow your paths, e.g.:

```python
...
tools_dir = '/home/john.doe/Development/Tools'
tools = {
  'jdk': {
    '1.7': 'jdk1.7',
    '1.8': 'jdk1.8'
  }
}
...
```
