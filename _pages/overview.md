---
layout: content
title: ExLL Overview
permalink: /overview/
---

 ExLL is a new low-latency congestion control scheme which can adapt to dynamic cellular channels without overloading the network. To do so, we develop two novel techniques that run on the cellular receiver: 1) cellular bandwidth inference from the downlink packet reception pattern and 2) minimum RTT calibration from the inference on the uplink scheduling interval. Furthermore, we incorporate the control framework of FAST into ExLL’s cellular specific inference techniques. Hence, ExLL can precisely control its congestion window to not overload the network unnecessarily. Our implementation of ExLL on Android smartphones demonstrates that ExLL reduces latency much closer to the minimum RTT compared to other low-latency congestion control algorithms in both static and dynamic channels of LTE networks.

![Receiver-based ExLL Design Overview](https://raw.githubusercontent.com/msnl/exll/master/assets/ExLL_Overview_receiver.PNG)

![Sender-based ExLL Design Overview](https://raw.githubusercontent.com/msnl/exll/master/assets/ExLL_Overview_sender.PNG)

# Features
- ExLL congestion control can be implemented at both of sender-side and receiver-side. (We first provide receiver-side ExLL implementation)
- Receiver-side ExLL can be deployed without touching sender-side device. (Easy Deployment)
- Cellular bandwidth inference from the downlink packet reception pattern.
- Minimum RTT calibration from the inference on the uplink scheduling interval.

# Performance

![Static Performance](https://raw.githubusercontent.com/msnl/exll/master/assets/ExLL_Static.PNG)

RTT and throughput performance comparison between ExLL and other protocols. ExLL outperforms other low-latency protocols and operates very closely to the ideal performance characterized by sending 1.0×BDP of the network.


![Mobile Performance](https://raw.githubusercontent.com/msnl/exll/master/assets/ExLL_Mobile.PNG)

RTT and throughput performance comparison between ExLL and other protocols in a mobile channel. ExLL shows nearly 20 ms less RTT compared to BBR while getting throughput as much as Cubic.

