	IP Address 192.168.1.5
	Binary 	 : 11000000.10101000.00000001.00000101
	subnet ma  11111111.11111111.11111111.00000000

count number of 1 in subnet mask 
count no of 0s in subnet mask

	1st octate:2nd octate: 3rd octate: 4th octate
------------------------------------
Subnet mask


	Network bit 	Host bit
	2019BEC 		07
________________________________________

Exam :

	Network Address: 192.168.1.0				formule(network address as it is and host bit all zero)	
	Subnet Mask: 	 255.255.255.0
	Block Size:	 256   			formule(2^host bit)
	Valid host Range:  192.168.1.1 --192.168.1.254
	Broadcast Address: 192.168.1.255


	interperetation :192.168.1.0/24		(here 24 is the total no of bits of subnet mask which are 1)



------------------------------------------------------------------------------------------------------
Subnetting is the process of breaking large network into smaller network by stealing host bit,
stealing host bit :

	General :192.168.1.1
	Binary 	 : 11000000.10101000.00000001.X000000
	Subnet Mask:  11111111.11111111.11111111.10000000

   when
   
   
   										X=0 				when X=1
	Network Address : 	192.168.1.0	 	192.168.1.128
	Subnet		  		255.255.255.128	255.255.255.128
	Broadcast Address 192.168.1.127		192.168.1.255
	Block Size					128						128
	Valid Host Range	  192.168.1.1 - 126		192.168.1.129 - 254
	Interpretation	192.168.1.0/25		192.168.1.128/25



Stealing 2 bit

	Binary 	 : 11000000.10101000.00000001.XX000101
	subnet ma  11111111.11111111.11111111.11000000
				When X=00		When X=01 		When X=10 		When X=11
	Network Address :

		192.168.1.0	 	192.168.1.64			192.168.1.128		192.168.1.192
SUBNET	

		255.255.255.192	255.255.255.192			255.255.255.192		255.255.255.192
Broadcast address

		192.168.1.63		192.168.1.127			192.168.1.191		192.168.1.255
Block size		

				64						64											64							64
Valid host ra	

		192.168.1.1 - 62	192.168.1.65 - 127		192.168.1.129 - 191	192.168.1.193 - 254

interpretation	

	192.168.1.0/26		192.168.1.64/26			192.168.1.128/26	192.168.1.192/26





_________________________________________________________________________________________________________________________________________________
Class 2

Configure 


	Router> user executive mode
	Router> enable  
	Password:
	Router# //privillege executive mode
	Router# configure terminal 
	Router(config)#  //global executive Mode
	Router(config)# hostname ccna
	ccna(config)#


	config# line console 0
	# password ccna
	#login


	Config# line vty 0
	#password cisco 
	#login

-------------------------------------------------------------------------------------------------------------------------------

 ios(internet operating system)
	
	
	Ram  			 Flash
	
running-config		


	NvRam 				Server
	startup-config 		TFTP (udp protocol)

	
Date:2076/08/14
----------------------------------------------------------------------------------------------------------------------------
#Group A
	1 Hub
	2 Repeater
	3 Switch
	4 Bridge
#Group B
	1 PC
	2 Server
	3 Router

Connecting device from differnet group requires a straight through cable


:Connecting devices from same group requires Cross Over cable



New technology called MIDIX which stands for Media Independent Interface Crossover 
 will automatically transform signal between device which in fact doesnt require any convention to be followed
 
 
__________________________________________________________________________________________________
##Setting Up ip address in Router
![](https://i.ibb.co/hRBwcvV/figure1.png )


!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!Fig:1!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!



	
	Router>
	Router>en
	Router#conf t
	Enter configuration commands, one per line.  End with CNTL/Z.
	Router(config)#int 
	Router(config)#in
	Router(config)#interface g0/0
	Router(config-if)#ip add 192.168.1.2 255.255.255.0
	Router(config-if)#no shut

_____________________________________________________________________
#Output


	Router(config-if)#
	%LINK-5-CHANGED: Interface GigabitEthernet0/0, changed state to up

	%LINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0, changed state to up
	!
	Router#
	%SYS-5-CONFIG_I: Configured from console by console
__________________________________________________________________________
#Showing the interface ip address

	Router(config-if)#show ip interface brief
						^
	% Invalid input detected at '^' marker.
	 Because this code can only be done outside as
	!!!!!!!!!!!!!!!!!!!!!
	Router#show ip interface brief
	Interface              IP-Address      OK? Method Status                Protocol 
	GigabitEthernet0/0     192.168.1.2     YES manual up                    up 
	GigabitEthernet0/1     192.168.2.1     YES manual up                    up 
	Vlan1                  unassigned      YES unset  administratively down down
 ______________________________________________________________________
OR use 	

	Router(config-if)#do show ip interface brief
	Interface              IP-Address      OK? Method Status                Protocol 
	GigabitEthernet0/0     192.168.1.2     YES manual up                    up 
	GigabitEthernet0/1     192.168.2.1     YES manual up                    up 
	Vlan1                  unassigned      YES unset  administratively down down


______________________________________________________________________


#pinging the Router For 
	Router#ping 192.168.1.1

	Type escape sequence to abort.
	Sending 5, 100-byte ICMP Echos to 192.168.1.1, timeout is 2 seconds:
	.!!!!
	Success rate is 80 percent (4/5), round-trip min/avg/max = 0/0/0 ms

![]( https://i.ibb.co/w67Dz0P/figure2.png)
_______________figure 2_____________

________________________________________
------------------------------------------------------------------------
![](https://i.ibb.co/n0YJXZL/Screenshot-from-2019-11-30-19-42-51.png)
	
	Setting up ip address for router 6
----------------------------------------------------------

![](https://i.ibb.co/jVFjCMb/Screenshot-from-2019-11-30-19-50-46.png)

	Setting up ip address for router 3

------------------------------------------------------

