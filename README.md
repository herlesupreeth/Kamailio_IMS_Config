# Kamailio_IMS_Config
Fixed version of Kamailio IMS configuration files for basic calling

## Components
- Kamailio (5.2.4+bionic)
- RTPEngine (7.4.1.5+0~mr7.4.1.5)
- Fraunhofer OpenHSS (r1198)

## Testbed Setup
<pre>
  +---------+        +-------+       +-------+
  |         | <-->   |  IMS  |  <--> |       |
  |  Alice  |        |       |       | Bob   |
  |         |        |       |       |       |
  |         |        |       |       |       |
  +---+-----+        +-------+       +-------+
</pre>

- Kamailio IMS => Running in a OpenStack VM with internal IP 10.4.128.8 and Floating IP 172.24.15.10
- Alice => OnePlus UE SIP client IP (UE maybe behind NAT or otherwise, works in both cases)
- Bob => OnePlus UE SIP client IP (UE maybe behind NAT or otherwise, works in both cases)

## Tested
- Basic VoIP calling with WiFi and LTE

## Not Tested
- VoLTE
