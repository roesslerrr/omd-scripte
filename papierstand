#!/bin/bash

# Holt die Seitenzahl vom Samsung-Drucker

seiten=`snmpget -v2c -Oqv -c public 10.1.2.4 1.3.6.1.2.1.43.11.1.1.9.1.1`


if [ $seiten -gt 70 ] ; then
    status=0
    statustxt=OK
elif [ $seiten -le 70 ] && [ $seiten -ge 60 ] ; then
    status=1
    statustxt=WARNING
else
    status=2
    statustxt=CRITICAL
fi
                        
echo "$status PAPER paper=$seiten $statustxt - $seiten im Samsung-Drucker"


