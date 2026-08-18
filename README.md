# gh

New-NetFirewallRule `
  -DisplayName "Hyper-V VM -> Host ALL" `
  -Direction Inbound `
  -Action Allow `
  -Protocol Any `
  -InterfaceAlias "vEthernet (Default Switch)"


(Get-NetIPAddress `
  -InterfaceAlias "vEthernet (Default Switch)" `
  -AddressFamily IPv4).IPAddress


Get-NetTCPConnection -State Listen |
Select-Object LocalAddress, LocalPort |
Sort-Object LocalPort
