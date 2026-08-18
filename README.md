# gh

New-NetFirewallRule `
  -DisplayName "Hyper-V VM -> Host ALL" `
  -Direction Inbound `
  -Action Allow `
  -Protocol Any `
  -InterfaceAlias "vEthernet (Default Switch)"
