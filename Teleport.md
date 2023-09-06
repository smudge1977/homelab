# Teleport v13.3.7
Running on cloud.sneconsulting.co.uk  
git:api/v13.3.7-0-geb15b29 go1.20.7 installed successfully!  
https://teleport.keithmarston.me.uk

The following commands are now available:
*  teleport - The daemon that runs the Auth Service, Proxy Service, and other Teleport services.
*  tsh      - A tool that lets end users interact with Teleport.
*  tctl     - An administrative tool that can configure the Teleport Auth Service.
*  tbot     - Teleport Machine ID client.

```bash
sudo teleport configure -o file \
    --acme --acme-email=keith@sneconsulting.co.uk \
    --cluster-name=teleport.keithmarston.me.uk
```

A Teleport configuration file has been created at "/etc/teleport.yaml".
To start Teleport with this configuration file, run:

sudo teleport start --config="/etc/teleport.yaml"

Note that starting a Teleport server with this configuration will require root access as:
- The Teleport configuration is located at "/etc/teleport.yaml".
- Teleport will be storing data at "/var/lib/teleport". To change that, run "teleport configure" with the "--data-dir" flag.

Happy Teleporting!

## Credentials

url|user|pass|2FA
---|---|--|--|
https://teleport.keithmarston.me.uk | teleport-admin | letmein123! | GoogleAuth on phone

