#RDP Lateral Movement

**Purpose**: Identify lateral movement via RDP 

**Data Required**: RDP connection / authorization logs. It's critical that analysts can identify the source and destination systems from the data. Useful sources for this data are the Bro RDP analyzer and Windows Event IDs 4624 (Type 10) and 4778.

**Collection Considerations**: Bro requires a production NSM deployment, Windows events may be easier to collect for many organizations. 

**Analysis Techniques**: Baselining / outlier detection

**Description**

Identifying lateral movement via RDP requires baselining to understand normal authentication activity in the network. While not always true, it's common for an attacker to move laterally at uncommon times, between uncommon systems, or between uncommon organizaitonal / business units-- baselining and looking for outliers can help identify this activity. Adding friendly intelligence--for example, knowing which systems belong to different organizational units--and threat intelligence--for example, understanding the path an attacker is most likely to take or has taken in the past--will increase an analysts ability to identify lateral movement.  

**More Info**

* [Hunting Through RDP Data - Josh Liburdi (BroCon 2015)](https://www.youtube.com/watch?v=mOV_9YMgYZw)
