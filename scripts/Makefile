all: data.cdb

backupdata:
        mv -f data backup/data.`date +%Y%m%d-%T`

data:
        cat zones/* > data

remote: data.cdb
        rsync -az -e ssh * tinydns@dns2.example.com:/var/lib/ndjbdns/

data.cdb:       backupdata data
                /usr/local/bin/tinydns-data
