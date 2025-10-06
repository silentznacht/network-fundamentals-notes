
1. Configure the device name.
```
Router(config)# hostname hostname
```

2. Secure privileged EXEC mode.
```
Router(config)# enable secret password
```

3. Secure user EXEC mode.
```
Router(config)# line console 0    
Router(config-line)# password password    
Router(config-line)# login
```

4. Secure remote Telnet / SSH access.
```
Router(config-line)# line vty 0 4   
Router(config-line)# password password    
Router(config-line)# login    
Router(config-line)# transport input { ssh | telnet }
```

5. Secure all passwords in the config file.
```
Router(config-line)# exit    
Router(config)# service password-encryption
```

6. Provide legal notification.
```
Router(config)# banner motd delimiter message delimiter
```

7. Save the configuration.
```
Router(config)# end    
Router# copy running-config startup-config
```

- **`hostname hostname`** – Sets the router’s device name.
- **`enable secret password`** – Protects privileged EXEC mode with a secure password.
- **Console password commands** – Secures local console access with a password.
- **VTY password commands** – Secures remote Telnet/SSH access with a password and protocol selection.
- **`service password-encryption`** – Encrypts all plaintext passwords in the configuration.
- **`banner motd`** – Displays a legal or informational message when users log in.
- **`copy running-config startup-config`** – Saves the current configuration to persist after reboot.