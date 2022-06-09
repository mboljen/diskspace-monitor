# NAME

diskspace-monitor - Monitor diskspace usage over time


# SYNOPSIS

**diskspace-monitor** [ **-f** ] [ **-a** _unit_ ] [ **-d** _days_ ] [ **-n** _npts_ ] [ **-h** ]


# DESCRIPTION

**diskspace-monitor**


# OPTIONS

**-f**
: plot free diskspace instead of used diskspace.

**-a** _unit_
: plot absolute diskspace usage in _unit_ instead of relative diskspace usage.  Valid specifiers are `B` for Bytes, `kB` for kBytes, `MB` for MBytes, `GB` for GBytes, and `TB` for TBytes.

**-d** _days_
: skip data older than _days_.

**-n** _npts_
: limit plot to latest _npts_ datapoints.

**-h**
: show this help message.


# INSTALLATION

Clone the remote repository and change into the local repository:

```bash
$ git clone https://github.com/mboljen/diskspace-monitor
$ cd diskspace-monitor
```

Use the following command to install this software:

```bash
$ make
$ make install
```

The default `PREFIX` is set to `/usr/local`.  In order to successfully complete the installation, you need to have write permissions for the installation location.


## CRONJOB

Invoke the script `<PREFIX>/sbin/diskspace-monitor-update` on a regular basis to update the diskspace logfiles.  You can place a symbolic link in `/etc/cron.daily` refering to `<PREFIX>/etc/cron.daily/diskspace-monitor-crontab`.

### OPTIONS

**-e** _regex_
: exclude drives matching the regular expression _regex_ from monitoring.

**-m** _num_
: limit number of lines in logfiles to _num_.

**-h**
: show this help message.


# CONTRIBUTION

Pull requests are welcome.  For major changes, please open an issue first to discuss what you would like to change.

Submit bug reports online at: <https://github.com/mboljen/diskspace-monitor/issues>

Please make sure to update tests as appropriate.


# SEE ALSO

Full documentation and sources at: <https://github.com/mboljen/diskspace-monitor>


# LICENSE

[MIT](https://choosealicense.com/licenses/mit/)
