### CHOCO
    [powershell]
    Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
### HYPER-V ENABLED, CONTAINER ENABLED
    GO TO Program & Features/Features On & Off
    ENABLE HYPER-V
### DOCKER
    choco install docker
    choco install docker-for-windows
