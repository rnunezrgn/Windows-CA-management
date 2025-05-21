# Windows-CA-management
Ansible role to create and import Windows Certificate Authority on CA Host and Client node

# Generating a Self-signed Certificate Using Ansible
You can generate a self-signed certificate on Windows using Ansible playbooks. However, since there's no native Ansible module for creating self-signed certificates, we typically rely on win_shell or win_powershell to invoke PowerShell commands.
We can encapsulate the certificate generation step into a PowerShell script, which we then execute via Ansible as show in this Ansible role.
