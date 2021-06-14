# Disown command

  + disown %1

# Ausführen eines Programmes vom Terminal (hinzufügen)

  + Erstellen Link in /usr/local/bin
    + sudo ln -s /path/to/file CommandToExecute

# Bearbeiten eines Speiermediums

  + über dd
    + sudo dd if=/dev/zero of=/dev/*name_of_device* bs=*4096* status=progress
    + *name_of_device* kann über lsblk oder dmesg herausgefunden werden
    + *4096* ist die Blocksize und kann alternieren

# Teilen der Internetverbindung

  + sudo iptables -t nat -A POSTROUTING -s 10.10.0.0/16 -o <IPINTERFACENAME_HERE> -j MASQUERADE
