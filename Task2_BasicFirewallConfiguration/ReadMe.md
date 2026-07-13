# Basic Firewall Configuration with UFW

## Objective

The objective of this task was to configure a basic firewall on Ubuntu using UFW (Uncomplicated Firewall). The firewall was configured to allow and deny specific network traffic based on security requirements.

## What is a Firewall?

A firewall is a security tool that monitors and controls incoming and outgoing network traffic. It protects a computer by allowing trusted connections while blocking unwanted or potentially dangerous traffic.

## Firewall Rules Applied

### Enable UFW

```bash
sudo ufw enable
```

This command activates the firewall.

### Allow SSH

```bash
sudo ufw allow ssh
```

This allows remote administration through SSH on port 22.

### Deny HTTP

```bash
sudo ufw deny http
```

This blocks HTTP traffic on port 80.

### Allow HTTPS

```bash
sudo ufw allow https
```

This allows secure web traffic on port 443.

### Deny Telnet

```bash
sudo ufw deny telnet
```

This blocks Telnet because it is an insecure protocol that sends data in plain text.

## Firewall Verification

The firewall configuration was verified using:

```bash
sudo ufw status verbose
```

The output confirmed that all rules were active.

## Firewall Testing

The firewall was tested by attempting to access an HTTP website using `wget`.

Command used:

```bash
wget http://example.com
```

The connection did not successfully retrieve the webpage, and the terminal returned a name resolution error. The testing process was documented with screenshots.

## Files Included

- README.md
- ufw_configuration.sh
- Screenshots of the firewall configuration and verification

## Conclusion

This task demonstrated how to configure a basic firewall using UFW, create allow and deny rules, verify the firewall configuration, and document the testing process.
