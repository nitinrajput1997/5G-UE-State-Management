# 5G-UE-State-Management

In 5G, it provides different services to the devices. For providing that service is the 5G system, it needs to track the availability and also the reachability of the device. 5G system tracks these states of the device such as:- RRC (radio resource control), Connection Management (CM), and Registration management (RM).

RRC determines the RRC connection between the device and the RAN. The RAN keeps tracking the RRC state of the connected device. Connection Management determines the status of the connection between the device and the AMF. This is also known as the Non-Access Stratum (NAS) connection. And AMF on the network side keeps track of the connection management state of the device. Registration Management determines whether devices are connected to the 5G system or not. 


RRC State
It indicates the RRC connection status between the device and the RAN. When the device is first powered-ON, it was in the RRC idle state. It means that there is no RRC connection established between the device and the RAN. In an idle state, the device can monitor the broadcast information from the RAN and based on that information and power level measurement made on the signal which is received from RAN, the device identifies the RAN which has a strong signal. And this procedure is known to be a cell selection procedure. Suppose, in some scenarios the device moves to another cell, then the device again has to perform the previous procedure. But now it is known to be a cell re-selection procedure. 

After that, the device wants to register with the 5G system and suppose it wants to make a voice call over the 5G. In that case, the device needs to enter into the RRC-connected state. When the device is in RRC connected, then the network will know the location of the device at the cell level. RRC inactive is an intermediate state between the RRC idle and RRC connected state. It's not available in 4G but now it was first introduced in the 5G to save the power. 

For example, the device is supposed to be in RRC connected mode and it is transferring the data to the RAN. This data transfer is not continuous, there was a long pause between the data transfer. Then the device, during the pause the data transfer. It suspends the RRC connection state and moves toward the inactive state. And the data are stored in the device and RAN. This parameter is known to be the RRC connection context. This RRC connection context is stored in the UE and RAN both. Suppose, there was data sent by the device to the RAN, so at that time it will resume the RRC connection and move towards the connected state again. 


Connection management 
It indicates if there is any active Non-Access Stratum (NAS) connection between the AMF and the device or not. This connection is also known to be the N1-Signaling link.

CM-Idle indicates that there is no N1 signalling link between the device and the AMF. If the device is registered with a 5G system and is in an idle state, then the network knows the registration area. The registration area is the list of tracking area that has been assigned to the device. In others in another scenario, if the device wants to register itself or transfer the data or wants to do a registration update with the 5G system, then it needs to enter into the CM-Connected state. This can achieve by establishing an RRC connection. When the device enters into the CM-Connected state, then the RAN knows in which cell it was located or in another way the AMF knows to which RAN the device disconnected.


Registration Management State
It is used to indicate the status of the registration or device with the 5G system. When the device is in the RM-Deregistered state then, the device is either switch-OFF or switched ON but deregistered from the 5G system, which means it is no longer registered with the 5G network. Now, it moves from RM-Deregistered estate to RM-Registered state by registering itself with the AMF. Once the registration is complete, that device will be served by the AMF. The device will also get a temporary identifier known to be GUTI. In the RM-Registered state, if the device is roaming or moves from one to another registration area, this updation is notified by the device by performing the registration update procedure.
