# ansible-windows-powerstig


## Usage

- Update your [inventory](inventory/windows.yml) to include relevant hosts and appropriate `winrm_transport`
- Update the [PowerStig template](templates/win_stig_dsc.ps.j2) to reflect the proper version [OsVersion, OsRole, and StigVersion to apply](https://github.com/Microsoft/PowerStig/wiki/WindowsServer)
- Execute the win_stig.yml playbook:

```
ansible-playbook -i inventory/ win_stig.yml --vault-password-file ~/.vaultp
```
