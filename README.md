# Windows-CA-management
Ansible role to create and import Windows Certificate Authority on CA Host and Client node

# A bit of background
For many Windows CA management tasks, you can use specific Ansible modules like:

	ansible.windows.certificate_info: Get certificates information from Windows Certificate Store
 	ansible.windows.win_certificate_store: Manage the Windows Certificate store
	
However, some tasks, like generating self-signed certificates, require PowerShell due to its native support for certificates

# Generating a Self-signed Certificate Using Ansible
You can generate a self-signed certificate on Windows using Ansible playbooks. 
However, since there's no native Ansible module for creating self-signed certificates, we typically rely on win_shell or win_powershell to invoke PowerShell commands.

We can encapsulate the certificate generation step into a PowerShell script, which we then execute via Ansible as show in this Ansible role.
