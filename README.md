# refresh_oui
Updating the vendor files oui &amp; iab systemwide

-german- -english translation below-

Jeder, der sich administrativ mit Linux beschäftigt, angefangen bei einem einfachen Scan mit nmap über eine Intrusion-Detection mit arpalert oder arpwatch bis zu spezielleren Programmen wie unicornscan oder btscan, alle haben eigentlich immer ein gleiches Problem:

Die Vendor-Dateien, welche einer MAC-Adresse einen Hersteller zuordnen, sind in der Regel hoffnungslos veraltet, wodurch die Zuordnung lückenhaft ist. Erschwerend kommt hinzu, dass die Dateien nicht das Original-Format beinhalten, sondern oftmals speziell formatiert sind.

Hat man sich also die Arbeit gemacht und die Dateien für nmap angepasst, hat man dieselbe Arbeit nochmal für die anderen Programme vor sich.

Da ich mich nur ungern immer wieder mit denselben Problemen aufhalte, aber veraltete Daten auch nicht mag, habe ich hierfür ein Programm geschrieben, welches nur noch in /usr/bin kopiert und eventuell ausführbar gemacht werden muss, anschließend erledigt dieses Script die notwendige Arbeit.

Hierzu werden die Dateien oui.txt und iab.txt in ihrer aktuellsten Version heruntergeladen, in die unterschiedlichen und auf diverse Programme zugeschnittenen Standards konvertiert und automatisiert Links zu diesen Dateien gesetzt, damit die Anpassungen systemweit zur Verfügung stehen.

Zur Zeit werden die folgenden Programme unterstützt:

    arp-scan
    arpalert
    arpwatch
    bluelog
    btscanner
    golismero
    nmap
    unicornscan

Idealerweise kann das Script in einen update-Prozess mittels /etc/cron.d oder crontab eingebunden werden, dann sind die Daten stets aktuell.

Sollten noch weitere Formate relevant sein oder andere zu unterstützende Programme, dann schreibt mir bitte eine Mail, damit ich diese in mein Script mit einbinden kann.

Gruesse

burningfog

-english-

Everyone, who works with linux at admin-niveau, starting with a normal nmap-scan about intrusion detection with arpalert or arpwatch up to specific programs like unicornscan or btscan has the same problem:

the vendor files, which translate the MAC-address to a manufacturer, are really old, so the result is incomplete. In addition the vendor-files dont have the same form like the original oui-files and need to be transferred via scripts. Updating the vendor file for nmap is not the same like updating the file for unicornscan.

So I decided to write a script which does this automatically for different applications. The best way is to coy the script as root to /usr/bin and prove the rights, that it is executable. After that you only have to start refresh_oui without parameters, the rest of the work has been done from the script.

oui.txt and iab.txt are transferred from the sources and are converted to the different forms, after that some links to detected applications are set to replace the old vendor files.

The following applications are automatically supported:

    arp-scan
    arpalert
    arpwatch
    bluelog
    btscanner
    golismero
    nmap
    unicornscan

You should thinkk about taking this script in an update-process with /etc/cron.d or crontab, so your vendor-files are always actualized.

If there are other vendor-file-formats or applications to support, please write an email so I can insert them into my script.

Greets

burning fog
