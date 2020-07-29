# Keytool commands

## list an entry
`keytool -list -keystore <mykeystore> -storepass <password> -alias <alias>`
 
## import normal certificate
`keytool -import -alias <targetalias> -file <certfile> -keystore <keystore> -storepass <passord>`

## import p12 cert
To figure out the source alias you can use the command
`keytool -list -keystore xmlgw_Martin_Singbartl.p12 -storetype PKCS12`
After you know the alias you can copy it into your main keystore
`keytool -importkeystore -srckeystore <p12 cert> -srcstoretype PKCS12 -destkeystore <target keystore> -srcstorepass <passord for p12 ert> -srcalias "<source alias>" -destalias <dest alias>`

