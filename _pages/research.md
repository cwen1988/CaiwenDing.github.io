---
ID: 158
post_title: Research
author: cading
post_excerpt: ""
layout: page
permalink: >
  https://cading.expressions.syr.edu/research/
published: true
post_date: 2018-06-03 01:18:29
---
<h2>Block-Circulant Matrix-Based Deep Learning Systems</h2>
<img class=" wp-image-159 alignleft" src="https://cading.expressions.syr.edu/wp-content/uploads/2018/06/Fig_Block_matrix-300x254.jpg" alt="" width="304" height="257" />

[AAAI’18][MICRO’17][FPGA'18][DATE'18][GLSVLSI’18]

The rapidly expanding model size in deep learning systems is posing a significant restriction on both the computation and weight storage, for both inference and training, and on both high-performance computing systems and low-power embedded system and IoT applications. In order to overcome these limitations, we propose a holistic framework of incorporating structured matrices (block-circulant matrices) into deep learning systems, and could achieve (i) simultaneous reduction on weight storage and computational complexities, (ii) simultaneous speedup of training and inference, and (iii) generality and fundamentality that can be used for both software and hardware implementations, different platforms, and different neural network types, sizes, and scalability.

Besides algorithm-level achievements, our framework has (i) a solid theoretical foundation to prove that our approach will converge to the same “effectiveness” as deep learning without compression; (ii) platform-specific implementations and optimizations on smartphones, FPGAs, and ASIC circuits. We demonstrate that our smartphone-based implementation achieves the similar speed of GPU and existing ASIC implementations on the same application. Our FPGA-based implementations for deep learning systems and LSTM networks could achieve 10X+ energy efficiency improvement compared with state-of-the-art, and even higher energy efficiency gain compared with IBM TrueNorth. Our proposed framework can achieve 3.5 TOPS performance in FPGAs and is the first to enable nano-second level recognition speed for image recognition tasks.
<h2>Design Optimization for Efficient Recurrent Neural Networks</h2>
<img class="size-medium wp-image-257 alignleft" src="https://cading.expressions.syr.edu/wp-content/uploads/2019/01/fig_phase1-1-300x209.png" alt="" width="300" height="209" />[HPCA'19]

Recurrent Neural Networks (RNNs) are becoming increasingly important for time series-related applications which require efficient and real-time implementations. The two major types are Long Short-Term Memory (LSTM) and Gated Recurrent Unit (GRU) networks. It is a challenging task to have real-time, efficient, and accurate hardware RNN implementations because of the high sensitivity to imprecision accumulation and the requirement of special activation function implementations. Recently two works have focused on FPGA implementation of inference phase of LSTM RNNs with model compression. First, ESE uses a weight pruning based compressed RNN model but suffers from irregular network structure after pruning. The second work C-LSTM mitigates the irregular network limitation by incorporating block-circulant matrices for weight matrix representation in RNNs, thereby achieving simultaneous model compression and acceleration.

<img class=" wp-image-253 alignleft" src="https://cading.expressions.syr.edu/wp-content/uploads/2019/01/fig_framework-1-300x100.png" alt="" width="438" height="146" />A key limitation of the prior works is the lack of a systematic design optimization framework of RNN model and hardware implementations, especially when the block size (or compression ratio) should be jointly optimized with RNN type, layer size, etc. In this paper, we adopt the block-circulant matrix-based framework, and present the Efficient RNN (E-RNN) framework for FPGA implementations of the Automatic Speech Recognition (ASR) application. The overall goal is to improve performance/energy efficiency under accuracy requirement. We use the alternating direction method of multipliers (ADMM) technique for more accurate block-circulant training, and present two design explorations providing guidance on block size and reducing RNN training trials. Based on the two observations, we decompose E-RNN in two phases: Phase I on determining RNN model to reduce computation and storage subject to accuracy requirement, and Phase II on hardware implementations given RNN model, including processing element design/optimization, quantization, activation implementation, etc. Experimental results on actual FPGA deployments show that E-RNN achieves a maximum energy efficiency improvement of 37.4x compared with ESE, and more than 2x compared with C-LSTM, under the same accuracy.
<h2>A Resource-Aware, Efficient Quantization Framework for Object Detection</h2>
<div><img class="size-medium wp-image-247 alignleft" src="https://cading.expressions.syr.edu/wp-content/uploads/2019/01/Fig_Grid2-300x91.jpg" alt="" width="300" height="91" />[FPGA’19]</div>
<div></div>
<div>Deep neural networks (DNNs), as the basis of object detection, will play a key role in the development of future autonomous systems with full autonomy. The autonomous systems have special requirements of real-time, energy-efficient implementations of DNNs on a power-budgeted system. Two research thrusts are dedicated to performance and energy efficiency enhancement of the inference phase of DNNs. The first one is model compression techniques while the second is efficient hardware implementations. Recent researches on extremely-low-bit CNNs such as binary neural network (BNN) and XNOR-Net replace the traditional floating point operations with binary bit operations, significantly reducing memory bandwidth and storage requirement, whereas suffering non-negligible accuracy loss and waste of digital signal processing (DSP) blocks on FPGAs.</div>
<div></div>
<div>To overcome these limitations, this paper proposes REQ-YOLO, a resource aware, systematic weight quantization framework for object detection,</div>
<div><img class="size-medium wp-image-260 alignleft" src="https://cading.expressions.syr.edu/wp-content/uploads/2019/01/Fig_CONV-300x287.png" alt="" width="300" height="287" />considering both algorithm and hardware resource aspects in object detection. We adopt the block-circulant matrix method and propose a heterogeneous weight quantization using Alternative Direction Method of Multipliers (ADMM), an effective optimization technique for general, non-convex optimization problems. To achieve real-time, highly-efficient implementations on FPGA, we present the detailed hardware implementation of block circulant matrices on CONV layers and develop an efficient processing element (PE) structure supporting the heterogeneous weight quantization, CONV dataflow and pipelining techniques, design optimization, and a template-based automatic synthesis framework to optimally exploit hardware resource. Experimental results show that our proposed REQ-YOLO framework can significantly compress the YOLO model while introducing very small accuracy degradation.</div>
<h2>Hybrid Electrical Energy Storage Systems</h2>
<h3>Reconfigurable Photovoltaic Systems for Electric Vehicles</h3>
[IEEE D&amp;T'18][ASP-DAC'17][DAC'17][ICCD'16]

<img class="wp-image-167 alignleft" src="https://cading.expressions.syr.edu/wp-content/uploads/2018/06/fig5-300x298.jpg" alt="" width="314" height="312" />

The ever-tightening emission standards on internal combustion engine vehicles (ICEVs) have brought a new era for electric vehicles (EVs). As an external energy source, the photovoltaic (PV) system has been deployed onto the surfaces of EVs to help propel EVs. An onboard PV system can charge the EV battery pack whenever there is sunlight and the EV battery pack may get fully charged after some time of parking.
We conducted research on deploying onboard PV systems for EVs. We provide a complete system architecture with the corresponding sensing and control loop.
We employ novel and effective design elements to push the performance limit of the onboard PV systems. The design elements include reconfiguration algorithm and structure, luminescent solar concentrator (LSC) technology, optimal macrocell size design, and simplification and acceleration methods. We use the actual measure solar irradiance profiles and vehicle panel areas in the validation of our design. Experimental results show that onboard PV systems can provide significant propulsion power and therefore achieve longer all-electric driving range for EVs.
<h3>Reconfigurable thermoelectric generators for vehicle radiators energy harvesting</h3>
[TVLSI'18][DATE'18][ISLPED'17]

<img class=" wp-image-166 alignleft" src="https://cading.expressions.syr.edu/wp-content/uploads/2018/06/TEG_system-300x222.png" alt="" width="342" height="253" />

Thermoelectric generation (TEG) has increasingly drawn attention for being environmentally friendly. A few researches have focused on improving TEG efficiency at the system level on vehicle radiators. The most recent reconfiguration algorithm shows improvement on performance but suffers from major drawback on computational time and energy overhead, and non-scalability in terms of array size and processing frequency. We propose a novel TEG array reconfiguration
algorithm that determines near-optimal configuration with an acceptable computational time. Additionally, we incorporate prediction methods to further reduce the runtime and switching overhead during the reconfiguration process. Experimental results present 30% performance improvement, almost 100× reduction on switching overhead and 13× enhancement on computational speed compared to the baseline and prior work. The scalability of our algorithm makes it applicable to larger scale systems such as industrial boilers and heat exchangers.
<h2>Enabling Efficient Non-Volatile Processors on Energy Harvesting Powered Embedded Systems</h2>
[IEEE D&amp;T'17][ICCD'16][GLSVLSI'16][ISCAS'16][IGSC'15]<img class="size-medium wp-image-178 alignleft" src="https://cading.expressions.syr.edu/wp-content/uploads/2018/06/fig5-1-300x288.jpg" alt="" width="300" height="288" />

In this project, we combined multiple indoor energy sources including TEG, PV,
and PZ, to eliminate the limitation of single energy source (unstable and sporadic)
and increase the overall converted output power to obtain a joint stable power source that effectively drives energy‐harvesting‐based embedded systems. We adopted artificial neural network‐based energy‐harvesting prediction methods, which were responsible for predicting the time of the next power failure of the nonvolatile processors (NVPs) and compensating the power failure through triggering the OS scheduler. Comprehensive comparison works regarding mean square error (MSE) of the multiple proposed prediction mechanisms are performed. We thoroughly investigated the methods of the neural network‐based harvesting predictions for both single and multiple sources and has evaluated the prediction accuracies on the measured TEG, PV, and PZ energy‐harvesting traces.

Additionally, we proposed a dynamic converter reconfiguration technique for ambient energy harvesting‐based NVPs to address the supply voltage gap between NTC operations and NVP checkpointing in the super‐threshold regime. By dynamically changing the connectivity of these MOSFET switches, near‐threshold operation for NVPs during normal operations and super‐threshold operation for a short period of time can be achieved when a power outage occurs. This time period allows the NVP to backup the current states to non‐volatile FRAM, and therefore, guarantees resilient program executions. Experimental results have demonstrated that the proposed techniques can significantly reduce the power consumption and improve the performance of energy harvesters and NVPs.

&nbsp;

&nbsp;

&nbsp;

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>

<audio style="display: none;" controls="controls"></audio>