---
layout: post
title: "ExLL Overview"
description: "Basic ExLL Design and it's performance"
date: 2019-04-18
tags: ExLL
comments: true
---

 ExLL is a new low-latency congestion control scheme which can adapt to dynamic cellular channels without overloading the network. To do so, we develop two novel techniques that run on the cellular receiver: 1) cellular bandwidth inference from the downlink packet reception pattern and 2) minimum RTT calibration from the inference on the uplink scheduling interval. Furthermore, we incorporate the control framework of FAST into ExLL’s cellular specific inference techniques. Hence, ExLL can precisely control its congestion window to not overload the network unnecessarily. Our implementation of ExLL on Android smartphones demonstrates that ExLL reduces latency much closer to the minimum RTT compared to other low-latency congestion control algorithms in both static and dynamic channels of LTE networks.

![Receiver-based ExLL Design Overview](https://raw.githubusercontent.com/msnl/exll/master/assets/ExLL_Overview_receiver.PNG)

![Sender-based ExLL Design Overview](https://raw.githubusercontent.com/msnl/exll/master/assets/ExLL_Overview_sender.PNG)

## Features
- ExLL congestion control can be implemented at both of sender-side and receiver-side. (We first provide receiver-side ExLL implementation)
- Receiver-side ExLL can be deployed without touching sender-side device. (Easy Deployment)
- Cellular bandwidth inference from the downlink packet reception pattern.
- Minimum RTT calibration from the inference on the uplink scheduling interval.

## Performance

![Static Performance](https://raw.githubusercontent.com/msnl/exll/master/assets/ExLL_Static.PNG)

![Mobile Performance](https://raw.githubusercontent.com/msnl/exll/master/assets/ExLL_Mobile.PNG)




# Licnese
The MIT License (MIT)

Copyright (c) 2017 Mike JS. Choi

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
