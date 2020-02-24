# Kamailio_IMS_Config
Fixed version of Kamailio IMS configuration files for basic calling

## Components
- Kamailio (5.2.4+bionic)
- RTPEngine (7.4.1.5+0~mr7.4.1.5)
- Fraunhofer OpenHSS (r1198)

## Testbed Setup

**For VoLTE setup, make sure to have eNB and (EPC + IMS) machines are in the same subnet**

### VoLTE test
<pre>
  +---------+        +-------+       +-------+
  |         | <-->   |  IMS  |  <--> |       |
  |  UE1    |        |   +   |       | UE2   |
  |         |        |  EPC  |       |       |
  |         |        |       |       |       |
  +---+-----+        +-------+       +-------+
</pre>

- Kamailio IMS + Open5gs (EPC) => Running in a OpenStack VM with internal IP 10.4.128.21 and Floating IP 172.24.15.30 (OpenStack is not mandatory, can run on a physical machine)
- UE1 => OnePlus 5t UE with IMSI 00101123456791 and MSISDN 0198765432100
- UE2 => OnePlus 5t UE with IMSI 00101123456792 and MSISDN 0298765432100

### VoIP test
<pre>
  +---------+        +-------+       +-------+
  |         | <-->   |  IMS  |  <--> |       |
  |  Alice  |        |       |       | Bob   |
  |         |        |       |       |       |
  |         |        |       |       |       |
  +---+-----+        +-------+       +-------+
</pre>

- Kamailio IMS => Running in a OpenStack VM with internal IP 10.4.128.21 and Floating IP 172.24.15.30 (OpenStack is not mandatory, can run on a physical machine)
- Alice => OnePlus UE SIP client IP (UE maybe behind NAT or otherwise, works in both cases)
- Bob => OnePlus UE SIP client IP (UE maybe behind NAT or otherwise, works in both cases)

## Tested
- Basic VoIP calling with WiFi and LTE
- VoLTE

## Not Tested
- VoWiFi
