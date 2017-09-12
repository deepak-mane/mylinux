# mylinux


# LINUX SNIPPETS FOR TROUBLESHOOTING ORACLE SERVER-CLIENT-DATABASE ISSUES/CONFIGURATION/SETUP

## TO Check the LDAP entry for Database if its pointing to Correct Service Name

```linux
#!/bin/bash
COUNTER=0;while [ $COUNTER -lt 10 ]; do tnsping pshcm04d| grep SERVICE_NAME; let COUNTER=COUNTER+1 ;done
```


##### END OF SNIPPET 4:53 PM 9/12/2017

