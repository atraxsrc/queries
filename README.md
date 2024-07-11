
event_simpleName=FileWritten OR event_simpleName=ProcessRollup2 OR event_simpleName=NetworkConnectIP4 OR event_simpleName=DnsRequest
(
    MD5HashLower=ce7dc5df5568a79affa540aa86b24773 OR 
    MD5HashLower=8f0071027d513867feb3eb8943ccaf05 OR 
    MD5HashLower=77970a04551636cc409e90d39bbea931 OR 
    MD5HashLower=6adaeb6543955559c05a9de8f92d1e1d OR 
    MD5HashLower=4383b1ea54a59d27e5e6b3122b3dadb2 OR
    RemoteIP=154.201.87.185 OR RemotePort=999 OR
    RemoteIP=164.155.205.99 OR
    DomainName="support.firewallsupportservers.com" OR
    RemoteIP=188.116.22.65 OR RemotePort=5000 OR
    RemoteIP=121.204.249.123 OR RemotePort=8077 OR
    RemoteIP=185.173.93.167 OR RemotePort=13306 OR
    DomainName="imgdev.s3.eu-west-3.amazonaws.com"
)
