# How to pack and unpack stuff

## tar

**Make a tarball**: 

```bash
$ tar -cf stuff.tar stuff-files-* stuff-folder/
```

**Extract a tarball**: 

```bash
$ tar -xf stuff.tar
```

### tar.gz

**Pack with gzip**:

```bash
$ tar -czf stuff.tar.gz stuff-files-* stuff-folder/
```

**Extract gzipped stuff**:

```bash
$ tar -xzf archiv.tar.gz
```

### tar.bz

**Pack with bz2**:

```bash
$ tar -cjf stuff.tar.gz stuff-files-* stuff-folder/
```

**Extract bz2 stuff**:

```bash
$ tar -xjf stuff.tar.gz
```


## zip

**Create zip archive**:

```bash
$ zip stuff.zip stuff-files-* stuff-folder/
```

**Extract zip file**:

```bash
$ unzip archiv.zip 
```