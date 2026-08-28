# Module 3: Core SOC Solutions
## Room 1: Intoduction to EDR
### What I learned about:
- Endpoint Detection and Response (EDR) is a widely adopted security solution designed to monitor, detect, and respond to advanced threats at the endpoint level. It offers deep-level protection for endpoints. No matter where the endpoints are, the EDR will make sure they are monitored constantly and threats are detected. It is a series of tools that monitor devices for activity that could indicate a threat.
- Some of the EDR solutions in the market:
    - [CrowdStrike Falcon](https://www.crowdstrike.com/wp-content/uploads/2022/03/crowdstrike-falcon-insight-data-sheet.pdf)
    - [Symantec EDR](https://docs.broadcom.com/doc/endpoint-detection-and-response-atp-endpoint-en)
    - [SentinelOne EDR](https://sentinelone.com/resources/datasheets/assets/usecase/sentinel-one-active-#page=1)
    - [Microsoft Defender for Endpoint](https://learn.microsoft.com/en-us/defender-endpoint/microsoft-defender-endpoint)
- Features of EDR: There are three main features of an EDR, which can also be referred to as the three pillars of an EDR solution.
  - Visibility: A good analysis often depends on the available level of visibility of the activity.  The level of visibility EDR provides is impressive. It collects detailed data from the endpoints, then presents this information in a very structured format to the analyst.
  - Detection: It incorporates signature-based detections as well as behavior-based detections, such as unexpected user activities. With modern machine learning capabilities, it identifies any deviation from the baseline behavior and instantly flags it. It can also detect fileless malware that resides in memory.
  - Response:  Imagine getting a detection on the EDR with full-fledged details on when, where, and what happened. As an analyst, you may decide to isolate a complete endpoint, terminate a process, or quarantine some files. You can also connect to the host remotely and execute actions independently. You can do this all from within the EDR console.

    > However, it's also important to remember that an EDR is a host-only security solution and does not detect network-level threats.