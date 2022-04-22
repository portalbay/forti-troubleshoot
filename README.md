# forti-troubleshoot
Various FortiGate Troubleshooting Commands and Configuration Settings.

 
```
#Packet Cap examples 
diag sniffer packet internal 'src host 192.168.0.130 and dst host 192.168.0.1'  
di sniff packet any 'host 10.0.1.5 and port 8443' 4 0 l 

#config system netflow 
 set collector-ip <ipv4_addr> 
 set collector-port <port_int> 
end 

#VPN Troubleshooting 
get vpn ipsec tunnel summary 
diag vpn tunnel list 
 ** sa=0 indicates there is mismatch between selectors or no traffic is being initiated 
diagnose debug application ike -1 
diagnose debug enable 
diagnose debug disable 

config system settings 
 set vpn-stats-log ipsec ssl 
 set vpn-stats-period 300 
End



config vpn ipsec phase2-interface 
 set auto-negotiate enable 
 next 

### 
 
#arp
get system arp 

#ping tests
execute ping-options source 192.168.2.1 


#enable scp 
config system global 
  set admin-scp enable 
end 

 

#show dhcp lease 
execute dhcp lease-list 

 

#set up rsa keys for ssh 
config system admin 
set ssh-public-key1 “ssh-rsa” 

 

#Commands to update license.. 
diag deb reset  
diag deb app update -1  
diag deb en  
execute update-now  
diag deb dis  
diag deb reset 

```
