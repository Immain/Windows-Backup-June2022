<img src=https://www.gamerevolution.com/assets/uploads/2021/07/Windows-11-downgrade-to-Windows-10-1280x720.png >

# Win10-11-SimpleBackupScript-Mar2022
Simple Win Copy Script using Ansible
Use this ansible script to backup documents on your Windows machine

## Operating System Requirements to run Ansible
- MacOS
- Linux

## Enable WinRM on the remote machine using this Action Script
```
$url = "https://raw.githubusercontent.com/ansible/ansible/devel/examples/scripts/ConfigureRemotingForAnsible.ps1"
$file = "$env:temp\ConfigureRemotingForAnsible.ps1"
(New-Object -TypeName System.Net.WebClient).DownloadFile($url, $file)
powershell.exe -ExecutionPolicy ByPass -File $file
winrm enumerate winrm/config/Listener
```
## To run the script, use the following command:
```
sudo ansible-playbook backup.yml -i hosts
```



