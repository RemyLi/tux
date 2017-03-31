# tux

lord of tux

## Force root user

```
if (( $EUID != 0 )); then
    echo "Please run as root"
    exit
fi
```

## Set date in var

```
NOW=$(date +%Y-%m-%d)
yesterday=$(date +%Y-%m-%d -d yesterday)
```

## chmod for file and dir

```
find {ezpublish/{cache,logs,config,sessions},ezpublish_legacy/{design,extension,settings,var},web} -print0 -type d | xargs -0 chmod -R 775
find {ezpublish/{cache,logs,config,sessions},ezpublish_legacy/{design,extension,settings,var},web} -print0 -type f | xargs -0 chmod -R 664
```
