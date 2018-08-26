= Logging =
systemd has its own logging system called the journal. Written at
/var/log/journal
`journalctl`

`journalctl -b`    : show all messages from this boot
`journalctl -b -0` : show all messages from this boot
`journalctl -b -1` : show all messages from previous boot
`journalctl --list-boots` : list of boots with numbers
`journalctl --since "2012-10-30 18:17:16"`
`journalctl --since "20 min ago"`
`journalctl -f`  : follow new messages
`journalctl /usr/lib/systemd/systemd`  : show messages from executable
`journalctl _PID=1`  : show messages by process
`journalctl -u netcfg` : show messages of unit
`journalctl -k` : show kernel ring buffer
`journalctl -p err..alert` : show error, critical, alert priority messages
`journalctl -fp err`
`journalctl SYSLOG_FACILITY=10` : show auth log

`journalctl --vacuum-time=2weeks` : keep no data older than 2 weeks

* journalctl -f
Log watching - systemd style
1. journalctl -b -p err
(-b show events since last reboot)
(err show events marked as error or worse)
