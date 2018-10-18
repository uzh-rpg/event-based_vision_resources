# Event-based Vision Resources

## Table of Contents:
- [Devices and Manufacturers](#devices)
- [Companies working on Event-based Vision](#companies_sftwr)
- [Neuromorphic Systems](#neuromorphic-systems)

- [Algorithms](#algorithms)
    - [Feature Detection and Tracking](#feature-detection)
        - [Corners](#corner-detection)
    - [Depth Estimation (3D Reconstruction)](#depth-estimation)
        - [Monocular](#depth-mono)
        - [Stereo](#depth-stereo)
    - [Optical Flow Estimation](#optical-flow-estimation)
    - [Intensity-Image Reconstruction](#image-reconstruction)
    - [Localization and Ego-motion estimation](#egomotion)
    - [Visual Odometry and SLAM (Simultaneous Localization And Mapping)](#VOSLAM)
    - [Visual-Inertial Odometry](#visual-inertial)
    - [Visual Stabilization](#visual-stabilization)
    - [Video Processing](#video-processing)
    - [Pattern recognition](#pattern-recognition)
    - [Control](#control)
    - [Space Applications](#space)
    - [Slip detection (Manipulation)](#slip_detection)

- [Datasets and Simulators](#datasets)
- [Software](#software)
    - [Drivers](#drivers)
    - [Calibration](#calibration)
    - [Algorithms](#software-algorithms)
    - [Utilities](#software-utilities)

- [Neuromorphic Processors and Platforms](#processors-platforms)
- [Workshops and Tutorials](#workshops)
- [Theses and Dissertations](#theses)
    - [Dissertations](#theses-phd)
    - [Master Theses](#theses-master)
- [People / Organizations](#people)
- [Contributing](#contributing)

___
<br>

<a name="devices"></a>
# Devices & Companies Manufacturing them
- **DVS (Dynamic Vision Sensor)**: Lichtsteiner, P., Posch, C., and Delbruck, T., *[A 128x128 120dB 15μs latency asynchronous temporal contrast vision sensor](http://doi.org/10.1109/JSSC.2007.914337)*, IEEE J. Solid-State Circuits, 43(2):566-576, 2008.
    - [Product page at iniVation](https://inivation.com/dvs/). [**Buy a DVS**](https://inivation.com/buy/)
    - [Product specifications](https://inivation.com/support/product-specifications/)    
    - [User guide](https://inivation.com/support/hardware/dvs128/)
    - [Introductory videos about the DVS](https://inivation.com/dvs/videos/dvs-introduction/)
    - [More videos about the DVS technology](https://inivation.com/dvs/videos/)
    - [iniVation AG](https://inivation.com/) invents, produces and sells neuromorphic technologies with a special focus on event-based vision into *business*. [Slides](http://rpg.ifi.uzh.ch/docs/ICRA17workshop/Jakobsen.pdf) by [S. E. Jakobsen](https://inivation.com/company/), board member of iniVation.
- **Samsung's DVS (Gen2)**
    - Son, B., et al., *[4.1 A 640×480 dynamic vision sensor with a 9µm pixel and 300Meps address-event representation](https://doi.org/10.1109/ISSCC.2017.7870263)*, IEEE Int. Solid-State Circuits Conf. (ISSCC), San Francisco, CA, 2017, pp. 66-67.
    - [Slides](http://rpg.ifi.uzh.ch/docs/ICRA17workshop/Samsung.pdf) and [Video](https://youtu.be/9t4vGSVqSAI) by [Yoel Yaffe](https://www.linkedin.com/in/yoel-yaffe-a606841/), Samsung Israel Research Center, Samsung Electronics.
- **DLS (Dynamic Line Sensor)**: Posch, C., Hofstaetter, M., Matolin, D., Vanstraelen, G., Schoen, P., Donath, N., and Litzenberger, M., *[A dual-line optical transient sensor with on-chip precision time-stamp generation](https://doi.org/10.1109/ISSCC.2007.373513)*, IEEE Int. Solid-State Circuits Conf. - Digest of Technical Papers, Lisbon Falls, MN, US, 2007.
    - [Fact sheet at AIT](https://www.ait.ac.at/fileadmin/mc/digital_safety_security/downloads/Factsheet_-_Linescan-Chip_DLS_en.pdf).
- **LWIR DVS**: Posch, C., Matolin, D., Wohlgenannt, R., Maier, T., Litzenberger, M., *[A Microbolometer Asynchronous Dynamic Vision Sensor for LWIR](https://doi.org/10.1109/JSEN.2009.2020658)*, IEEE Sensors Journal, 9 (2009), 6; S. 654 - 664.
    - Prototype, commercially n.a.
- **Smart DVS (GAEP)**: Posch, C., Hoffstaetter, M., Schoen, P., *[A SPARC-compatible general purpose Address-Event processor with 20-bit 10ns-resolution asynchronous sensor data interface in 0.18um CMOS](https://doi.org/10.1109/ISCAS.2010.5537575)*, IEEE International Symposium on Circuits and Systems (ISCAS), 2010.
    - Prototype, commercially n.a.
- **DAVIS (Dynamic and Active-Pixel Vision Sensor)** :
Brandli, C., Berner, R., Yang, M., Liu, S.-C., Delbruck, T., *[A 240x180 130 dB 3 µs Latency Global Shutter Spatiotemporal Vision Sensor](https://doi.org/10.1109/JSSC.2014.2342715)*, IEEE J. Solid-State Circuits, 49(10):2333-2341, 2014.
    - [Product page at iniVation](https://inivation.com/dvs/).  [**Buy a DAVIS**](https://inivation.com/buy/)
    - [Product specifications](https://inivation.com/support/product-specifications/)
    - [User guide](https://inivation.com/support/hardware/davis240/)
    - **Color-DAVIS**: Li, C., Brandli, C., Berner, R., Liu, H., Yang, M., Liu, S.-C., Delbruck, T., *[Design of an RGBW Color VGA Rolling and Global Shutter Dynamic and Active-Pixel Vision Sensor](https://doi.org/10.1109/ISCAS.2015.7168734)*, IEEE Int. Symp. Circuits and Systems (ISCAS), 2015, pp. 718-721.
- [**Insightness's Silicon Eye**](https://youtu.be/Y0mIb_MehK8) QVGA event sensor. 
    - [The Silicon Eye Technology](http://www.insightness.com/?p=361)
    - [Slides](http://rpg.ifi.uzh.ch/docs/ICRA17workshop/Insightness.pdf) and [Video](https://youtu.be/6YyOW6DDGKw) by [Christian Brandli](http://www.insightness.com/#team), CEO and co-founder of Insightness.
- **ATIS (Asynchronous Time-based Image Sensor)**: Posch, C., Matolin, D., Wohlgenannt, R. (2011). *[A QVGA 143 dB Dynamic Range Frame-Free PWM Image Sensor With Lossless Pixel-Level Video Compression and Time-Domain CDS](http://doi.org/10.1109/JSSC.2010.2085952)*, IEEE J. Solid-State Circuits, 46(1):259-275, 2011.
    - [Prophesee](http://www.prophesee.ai) (Formerly [Chronocam](http://www.chronocam.com/))
    - [AIT Austrian Institute of Technology](https://www.ait.ac.at/en/research-fields/new-sensor-technologies/optical-sensor-systems-for-industrial-processes/)
- Posch, C., Serrano-Gotarredona, T., Linares-Barranco, B., Delbruck, T.,  
*[Retinomorphic Event-Based Vision Sensors: Bioinspired Cameras With Spiking Output](https://doi.org/10.1109/JPROC.2014.2346153),*  
Proc. IEEE (2014), 102(10):1470-1484.
- CeleX ([Hillhouse Technology](http://www.hillhouse-tech.com/), Singapore). [YouTube](https://youtu.be/Wlzc-5sgm1g)
- Sensitive DVS (sDVS)
    - Leñero-Bardallo, J. A., Serrano-Gotarredona, T., Linares-Barranco, B., *[A 3.6us Asynchronous Frame-Free Event-Driven Dynamic-Vision-Sensor](https://doi.org/10.1109/JSSC.2011.2118490)*,  IEEE J. of Solid-State Circuits, 46(6):1443-1455, 2011.
    - Serrano-Gotarredona, T. and Linares-Barranco, B., *[A 128x128 1.5% Contrast Sensitivity 0.9% FPN 3us Latency 4mW Asynchronous Frame-Free Dynamic Vision Sensor Using Transimpedance Amplifiers](https://doi.org/10.1109/JSSC.2012.2230553)*,  IEEE J. Solid-State Circuits, 48(3):827-838, 2013.

<a name="companies_sftwr"></a>
# Companies working on Event-based Vision
- [iniVation AG](https://inivation.com/) invents, produces and sells neuromorphic technologies with a special focus on event-based vision into *business*.
- [iniLabs AG](https://inilabs.com/) invents neuromorphic technologies for *research*.
- [Samsung](http://www.samsung.com) develops Gen2 and Gen3 dynamic vision sensors and event-based vision solutions.
  - [IBM Research](http://www.research.ibm.com/articles/brain-chip.shtml) ([Synapse project](http://www.research.ibm.com/cognitive-computing/brainpower/)) and Samsung partenered to combine the [TrueNorth chip (brain) with a DVS (eye)](https://www.cnet.com/news/samsung-turns-ibms-brain-like-chip-into-a-digital-eye/).
- [Prophesee](http://www.prophesee.ai) (Formerly [Chronocam](http://www.chronocam.com/)) develops bio-inspired and self-adapting approach to the need for visual sensing and processing in autonomous vehicles, connected devices, security and surveillance systems.
- [Insightness AG](http://www.insightness.com/) builds visual systems to give mobile devices spatial awareness. [The Silicon Eye](http://www.insightness.com/?p=361) Technology.
- [SLAMcore](https://www.slamcore.com/) develops Localisation and mapping solutions for AR/VR, robotics & autonomous vehicles.
- [Hillhouse Technology](http://www.hillhouse-tech.com/) offer integrated sensory platforms that incorporate various components and technologies, including a processing chipset and an image sensor (a dynamic vision sensor called CeleX).
- [AIT Austrian Institute of Technology](https://www.ait.ac.at/en/research-fields/new-sensor-technologies/optical-sensor-systems-for-industrial-processes/) sells neuromorphic sensor products.
    - [Inspection during production of carton packs](https://www.youtube.com/watch?v=8PZmb2z2bXw&index=39&list=PL659671AC92E70F19)
    - [UCOS Universal Counting Sensor](https://www.ait.ac.at/fileadmin/mc/digital_safety_security/downloads/Factsheet_-_People-Counting-Sensor_en.pdf)
    - [IVS Industrial Vision Sensor](https://www.ait.ac.at/fileadmin/mc/digital_safety_security/downloads/Factsheet_-_Industrial-Vision-Sensor_en.pdf)

<br><br>
<a name="neuromorphic-systems"></a>
# Neuromorphic Systems
- <a name="SerranoGotarredona99tcas"></a> Serrano-Gotarredona, T. , Andreou, A.G. , Linares-Barranco, B.,  
*[AER Image Filtering Architecture for Vision Processing Systems](https://doi.org/10.1109/81.788808)*,  
IEEE Trans. Circuits Syst. I, Fundam. Theory Appl., 46(9):1064-1071, 1999.
- <a name="SerranoGotarredona06anips"></a> Serrano-Gotarredona, R., Oster, M., Lichtsteiner, P., Linares-Barranco, A., Paz-Vicente, R., Gomez-Rodriguez, F., Riis, H.K., Delbruck, T., Liu, S.-H., Zahnd, S., Whatley, A.M., Douglas, R., Hafliger, P., Jimenez-Moreno, G., Civit, A.,  Serrano-Gotarredona, T., Acosta-Jimenez, A., Linares-Barranco, B.,  
*[AER building blocks for multi-layer multi-chip neuromorphic vision systems](http://papers.nips.cc/paper/2889-aer-building-blocks-for-multi-layer-multi-chip-neuromorphic-vision-systems.pdf)*,  
Advances in neural information processing systems, 1217-1224, 2006.
- <a name="Delbruck08issle"></a>Delbruck, T.,  
[Frame-free dynamic digital vision](http://www.zora.uzh.ch/17620/)*,  
Int. Symp. Secure-Life Electronics, Advanced Electronics for Quality Life and Society, University of Tokyo, Tokyo, Japan, Mar. 6-7, 2008, pp. 21-26. Introduces the software architecture of jAER and shows examples of several event-based processing algorithms.
- <a name="Liu10conb"></a>Liu, S.-C. and Delbruck, T.,  
*[Neuromorphic sensory systems](https://doi.org/10.1016/j.conb.2010.03.007)*,  
Current Opinion in Neurobiology, 20:3(288-295), 2010.
- <a name="Posch12jinst"></a>Posch, C.,
*[Bio-inspired vision](https://doi.org/10.1088/1748-0221/7/01/C01054)*,  
J. of Instrumentation, 7 C01054, 2012.  Bio-inspired explanation of the DVS and the ATIS.
- <a name="Delbruck12eccvw"></a>Delbruck, T.,  
*[Fun with asynchronous vision sensors and processing](https://www.ini.uzh.ch/~tobi/wiki/lib/exe/fetch.php?media=delbruck_funwithasynsensors_2012.pdf)*.  
Computer Vision - ECCV 2012. Workshops and Demonstrations. Springer Berlin/Heidelberg, 2012. A position paper and summary of recent accomplishments of the INI Sensors' group.
- <a name="ZamarrenoRamos13tbcas"></a> Zamarreño-Ramos, C., Linares-Barranco, A., Serrano-Gotarredona, T., Linares-Barranco, B.,  
*[Multi-Casting Mesh AER: A Scalable Assembly Approach for Reconfigurable Neuromorphic Structured AER Systems. Application to ConvNets](https://doi.org/10.1109/TBCAS.2012.2195725)*,  
IEEE Trans. Biomed. Circuits Syst., 7(1):82-102, 2013.
- <a name="Liu14book"></a>Liu, S.-C., Delbruck, T., Indiveri, G., Whatley, A., Douglas, R.,  
*[Event-Based Neuromorphic Systems](http://eu.wiley.com/WileyCDA/WileyTitle/productCd-1118927621.html)*,  
Wiley. ISBN: 978-1-118-92762-5, 2014.
- <a name="Chicca14ieee"></a>Chicca, E., Stefanini, F., Bartolozzi, C., Indiveri, G.,  
*[Neuromorphic Electronic Circuits for Building Autonomous Cognitive Systems](http://dx.doi.org/10.1109/JPROC.2014.2313954)*,  
Proc. IEEE, 102(9):1367-1388, 2014.
- <a name="Delbruck16essderc"></a>Delbruck, T.,  
*[Neuromorophic Vision Sensing and Processing (Invited paper)](https://doi.org/10.1109/ESSDERC.2016.7599576)*,  
46th Eur. Solid-State Device Research Conference (ESSDERC), Lausanne, 2016, pp. 7-14.
- <a name="Vanarse16fnins"></a>Vanarse, A., Osseiran, A., Rassau, A,  
*[A Review of Current Neuromorphic Approaches for Vision, Auditory, and Olfactory Sensors](http://dx.doi.org/10.3389/fnins.2016.00115)*,
Front. Neurosci. (2016), 10:115.

<br><br>
<a name="algorithms"></a>
# Algorithms

<a name="feature-detection"></a>
## Feature Detection and Tracking
- <a name="Litzenberger06dspws"></a>Litzenberger, M., Posch, C., Bauer, D., Belbachir, A. N., Schon. P., Kohn, B., Garn, H.,  
*[Embedded Vision System for Real-Time Object Tracking using an Asynchronous Transient Vision Sensor](https://doi.org/10.1109/DSPWS.2006.265448)*,  
IEEE 12th Digital Signal Proc. Workshop and 4th IEEE Signal Proc. Education Workshop, Teton National Park, WY, 2006, pp. 173-178.
- <a name="Litzenberger06itsc"></a>Litzenberger, M., Kohn, B., Belbachir, A.N., Donath, N., Gritsch, G., Garn, H., Posch, C., Schraml, S.,  
*[Estimation of Vehicle Speed Based on Asynchronous Data from a Silicon Retina Optical Sensor](https://doi.org/10.1109/ITSC.2006.1706816)*,  
IEEE Intelligent Transportation Systems Conf., Toronto, Ont., 2006, pp. 653-658. [PDF](http://belbachir.info/PDF/itsc2006.pdf)
- <a name="Drazen11eif"></a>Drazen, D., Lichtsteiner, P., Haefliger, P., Delbruck, T., Jensen, A.,  
*[Toward real-time particle tracking using an event-based dynamic vision sensor](https://doi.org/10.1007/s00348-011-1207-y)*,  
Experiments in Fluids (2011), 51(1):1465-1469. [PDF](http://www.zora.uzh.ch/60624/1/Drazen_EIF_2011.pdf)
- <a name="Ni11jmcro"></a>Ni, Z., Pacoret, C., Benosman, R., Ieng, S., Regnier, S.,  
*[Asynchronous event-based high speed vision for microparticle tracking](http://doi.org/10.1111/j.1365-2818.2011.03565.x)*,  
J. Microscopy (2011), 245(3):236-244.
- <a name="Ni12tro"></a>Ni, Z., Bolopion, A., Agnus, J., Benosman, R., Regnier, S.,  
*[Asynchronous event-based visual shape tracking for stable haptic feedback in microrobotics](https://doi.org/10.1109/TRO.2012.2198930)*,  
IEEE Trans. Robot., 28(5):1081-1089, 2012.
- <a name="Piatkowska12cvprw"></a>Piatkowska, E., Belbachir, A. N., Schraml, S., Gelautz, M.,  
*[Spatiotemporal multiple persons tracking using Dynamic Vision Sensor](https://doi.org/10.1109/CVPRW.2012.6238892)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2012, pp. 35-40. [PDF](https://publik.tuwien.ac.at/files/PubDat_209369.pdf)
- [Ni, Ph.D. Thesis, 2013](#Ni13PhD),  
*Asynchronous Event Based Vision:  Algorithms and Applications to Microrobotics*.
- <a name="Lagorce13iros"></a>Lagorce, X., Ieng, S. H., Benosman, R.,  
*[Event-based features for robotic vision](http://dx.doi.org/10.1109/IROS.2013.6696960)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2013, pp. 4214-4219.
- <a name="Borer14isfv"></a>Borer, D.,  Rosgen, T.,  
*[Large-scale Particle Tracking with Dynamic Vision Sensors]()*,  
ISFV16 - 16th Int. Symp. Flow Visualization, Okinawa 2014. [Project page](http://www.ifd.mavt.ethz.ch/research/group-roesgen/dynamic-vision-sensors.html), [PDF](http://www.ifd.mavt.ethz.ch/content/dam/ethz/special-interest/mavt/fluid-dynamics/ifd-dam/research/documents/posters/experimental-methods/daniel_borer_dynamic_vision_sensor.pdf)
- <a name="Lagorce14biocas"></a>Lagorce, X., Meyer, C., Ieng, S. H., Filliat, D., Benosman, R.,  
*[Live demonstration: Neuromorphic event-based multi-kernel algorithm for high speed visual features tracking](https://doi.org/10.1109/BioCAS.2014.6981681)*,  
IEEE Biomedical Circuits and Systems Conference (BioCAS), Lausanne, 2014, pp. 178-178.
- <a name="Lagorce15tnnls"></a>Lagorce, X., Meyer, C., Ieng, S. H., Filliat, D., Benosman, R.,  
*[Asynchronous Event-Based Multikernel Algorithm for High-Speed Visual Features Tracking](https://doi.org/10.1109/TNNLS.2014.2352401)*,  
IEEE Trans. Neural Netw. Learn. Syst., 26(8):1710-1720, 2015.
- <a name="Lagorce15fnins"></a>Lagorce, X., Ieng, S.-H., Clady, X., Pfeiffer, M., Benosman, R.,  
*[Spatiotemporal features for asynchronous event-based data](http://dx.doi.org/10.3389/fnins.2015.00046)*,  
Front. Neurosci. (2015), 9:46.
- <a name="Ni15neco"></a>Ni, Z., Ieng, S. H., Posch, C., Regnier, S., Benosman, R.,  
*[Visual Tracking Using Neuromorphic Asynchronous Event-Based Cameras](https://doi.org/10.1162/NECO_a_00720)*,  
Neural Computation (2015), 27(4):925-953.
- <a name="LinaresBarranco15iscas"></a>Linares-Barranco, A., Gómez-Rodríguez, F., Villanueva, V., Longinotti, L., Delbrück, T.,    
*[A USB3.0 FPGA event-based filtering and tracking framework for dynamic vision sensors](https://doi.org/10.1109/ISCAS.2015.7169172)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2015, pp. 2417-2420.
- <a name="Barranco15iccv"></a>Barranco, F., Teo, C. L., Fermüller, C., Aloimonos, Y.,  
*[Contour Detection and Characterization for Asynchronous Event Sensors](https://doi.org/10.1109/ICCV.2015.63)*,  
IEEE Int. Conf. Computer Vision (ICCV), 2015, pp. 486-494. [PDF](http://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Barranco_Contour_Detection_and_ICCV_2015_paper.pdf)
- <a name="Liu16iscas"></a>Liu, H., Moeys, D. P., Das, G., Neil, D., Liu, S.-C., Delbruck, T.,  
*[Combined frame- and event-based detection and tracking](https://doi.org/10.1109/ISCAS.2016.7539103)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2016, pp. 2511-2514.
- <a name="Tedaldi16ebccsp"></a>Tedaldi, D., Gallego, G., Mueggler, E., Scaramuzza, D.,  
*[Feature detection and tracking with the dynamic and active-pixel vision sensor (DAVIS)](https://doi.org/10.1109/EBCCSP.2016.7605086)*,  
IEEE Int. Conf. Event-Based Control Comm. and Signal Proc. (EBCCSP), 2016. [PDF](http://rpg.ifi.uzh.ch/docs/EBCCSP16_Tedaldi.pdf), [YouTube](https://www.youtube.com/watch?v=nglfEkiK308)
- <a name="Brandli16ebccsp"></a>Braendli, C., Strubel, J., Keller, S., Scaramuzza, D., Delbruck, T.,  
*[ELiSeD - An Event-Based Line Segment Detector](https://doi.org/10.1109/EBCCSP.2016.7605244)*,  
Int. Conf. on Event-Based Control Comm. and Signal Proc. (EBCCSP), 2016. [PDF](http://rpg.ifi.uzh.ch/docs/EBCCSP16_Braendli.pdf)
- <a name="Glover16iros"></a>Glover, A. and Bartolozzi, C.,  
*[Event-driven ball detection and gaze fixation in clutter](https://doi.org/10.1109/IROS.2016.7759345)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2016, pp. 2203-2208. [YouTube](https://youtu.be/xS-7xYRYSLc), [Code](https://github.com/robotology/event-driven)
- <a name="Clady17fnins"></a> Clady, X., Maro, J.-M., Barré, S., Benosman, R. B.,  
*[A Motion-Based Feature for Event-Based Pattern Recognition](https://doi.org/10.3389/fnins.2016.00594)*.  
Front. Neurosci. (2017), 10:594.
- <a name="Zhu17icra"></a>Zhu, A., Atanasov, N., Daniilidis, K.,  
*[Event-based Feature Tracking with Probabilistic Data Association](https://doi.org/10.1109/ICRA.2017.7989517)*,  
IEEE Int. Conf. Robotics and Automation (ICRA), 2017. [PDF](https://fling.seas.upenn.edu/~alexzhu/dynamic/wp-content/uploads/2017/07/EventBasedFeatureTrackingICRA2017.pdf), [YouTube](https://youtu.be/m93XCqAS6Fc), [Code](https://github.com/daniilidis-group/event_feature_tracking)
- <a name="Glover17iros"></a>Glover, A. and Bartolozzi, C.,  
*[Robust Visual Tracking with a Freely-moving Event Camera](https://doi.org/10.1109/IROS.2017.8206226)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2017. [YouTube](https://youtu.be/xS-7xYRYSLc), [Code](https://github.com/robotology/event-driven)
- <a name="BarriosAviles17arxiv"></a>Barrios-Avilés, J., Iakymchuk, T., Samaniego, J., Rosado-Muñoz, A.,  
*[An Event-based Fast Movement Detection Algorithm for a Positioning Robot Using POWERLINK Communication](https://arxiv.org/abs/1707.07188)*,  
arXiv:1707.07188, 2017.
- <a name="Li17bmvc"></a>Li, J., Shi, F., Liu, W., Zou, D., Wang, Q., Park, Paul-K.J., Hyunsurk, E.R.,  
*[Adaptive Temporal Pooling for Object Detection using Dynamic Vision Sensor](https://www.dropbox.com/s/m77i7cqqy7xbg51/0099.pdf?dl=1)*,  
British Machine Vision Conf. (BMVC), 2017.
- <a name="Peng17tnnls"></a>Peng, X., Zhao, B., Yan, R., Tang H., Yi, Z.,  
*[Bag of Events: An Efficient Probability-Based Feature Extraction Method for AER Image Sensors](http://dx.doi.org/10.1109/TNNLS.2016.2536741)*,  
IEEE Trans. Neural Netw. Learn. Syst., 28(4):791-803, 2017.
- <a name="Ramesh17arxiv"></a>Ramesh, B., Yang, H., Orchard, G., Le Thi, N.A., Xiang, C,  
*[DART: Distribution Aware Retinal Transform for Event-based Cameras](https://arxiv.org/pdf/1710.10800.pdf)*,  
arXiv:1710.10800, 2017.
- <a name="Gehrig18eccv"></a>Gehrig, D., Rebecq, H., Gallego, G., Scaramuzza, D.,  
*[Asynchronous, Photometric Feature Tracking using Events and Frames](http://rpg.ifi.uzh.ch/docs/ECCV18_Gehrig.pdf)*,  
European Conf. Computer Vision (ECCV) 2018. [Poster](http://rpg.ifi.uzh.ch/docs/ECCV18_Gehrig_poster.pdf), [YouTube](https://youtu.be/A7UfeUnG6c4), [Oral presentation](https://youtu.be/7EvY8SxdLl8).
- <a name="Mitrokhin18iros"></a>Mitrokhin, A., Fermuller, C., Parameshwara, C., Aloimonos, Y.,  
*[Event-based Moving Object Detection and Tracking](https://arxiv.org/pdf/1803.04523.pdf)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2018. [YouTube](https://youtu.be/UCAJi0ZFaZ8), [Project page and Dataset](http://prg.cs.umd.edu/BetterFlow.html)
- <a name="Barranco18iros"></a>Barranco, F., Fermuller, C., Ros, E.,  
*[Real-Time Clustering and Multi-Target Tracking Using Event-Based Sensors](https://arxiv.org/pdf/1807.02851.pdf)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2018.
- <a name="Iacono18iros"></a>Iacono, M., Weber, S., Glover, A., Bartolozzi, C.,  
*Towards Event-Driven Object Detection with Off-The-Shelf Deep Learning*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2018.
- <a name="Iacono18iros"></a>
Ramesh, B., Zhang, S., Lee, Z.-W., Gao, Z., Orchard, G., Xiang, C.,  
*[Long-term object tracking with a moving event camera](http://bmvc2018.org/contents/papers/0814.pdf)*,  
British Machine Vision Conf. (BMVC), 2018.  [Video](http://bmvc2018.org/contents/supplementary/video/0814_video.mp4)


<a name="corner-detection"></a>
### Corner Detection and Tracking

- <a name="Clady15neunet"></a>Clady, X., Ieng, S.-H., Benosman, R.,  
*[Asynchronous event-based corner detection and matching](https://doi.org/10.1016/j.neunet.2015.02.013)*,  
Neural Networks (2015), 66:91-106.
- <a name="Vasco16iros"></a>Vasco, V., Glover, A., Bartolozzi, C.,  
*[Fast event-based Harris corner detection exploiting the advantages of event-driven cameras](https://doi.org/10.1109/IROS.2016.7759610)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2016, pp. 4144-4149. [YouTube](https://youtu.be/YkI7AfBDBKE), [Code](https://github.com/robotology/event-driven)
- <a name="Mueggler17bmvc"></a>Mueggler, E., Bartolozzi, C., Scaramuzza, D.,  
*[Fast Event-based Corner Detection](http://rpg.ifi.uzh.ch/docs/BMVC17_Mueggler.pdf)*,  
British Machine Vision Conf. (BMVC), 2017. [YouTube](https://youtu.be/tgvM4ELesgI), [Code](https://github.com/uzh-rpg/rpg_corner_events)
- <a name="Alzugaray18ral"></a>Alzugaray, I., Chli, M.,  
*[Asynchronous Corner Detection and Tracking for Event Cameras in Real Time](http://dx.doi.org/10.1109/LRA.2018.2849882)*,  
IEEE Robotics and Automation Letters (RA-L), 3(4):3177-3184, Oct. 2018.  [PDF](https://doi.org/10.3929/ethz-b-000277131), [YouTube](https://youtu.be/bKUAZ7IQcf0).
- <a name="Alzugaray183dv"></a>Alzugaray, I., Chli, M.,  
*[ACE: An Efficient Asynchronous Corner Tracker for Event Cameras](https://doi.org/10.3929/ethz-b-000291763)*,  
Int. Conf. 3D Vision (3DV), 2018.  [YouTube](https://youtu.be/I31yQqmCsfs)


<a name="depth-estimation"></a>
## Depth Estimation (3D Reconstruction)

<a name="depth-mono"></a>
### Monocular Depth Estimation
- <a name="Rebecq16bmvc"></a>Rebecq, H., Gallego, G., Scaramuzza, D.,  
*[EMVS: Event-based Multi-View Stereo](http://www.bmva.org/bmvc/2016/papers/paper063/)*,  
British Machine Vision Conf. (BMVC), 2016. [PDF](http://rpg.ifi.uzh.ch/docs/BMVC16_Rebecq.pdf), [YouTube](https://www.youtube.com/watch?v=EUX3Tfx0KKE), [3D Reconstruction Experiments from a Train using an Event Camera](https://www.youtube.com/watch?v=fA4MiSzYHWA)
- <a name="Rebecq17ijcv"></a>Rebecq, H., Gallego, G., Mueggler, E., Scaramuzza, D.,  
*[EMVS: Event-Based Multi-View Stereo—3D Reconstruction with an Event Camera in Real-Time](https://doi.org/10.1007/s11263-017-1050-6)*,  
Int. J. of Computer Vision (IJCV), 2017. [PDF](http://rpg.ifi.uzh.ch/docs/IJCV17_Rebecq.pdf), [YouTube](https://youtu.be/EFpZcpd9XJ0).
- [Kim et. al. ECCV 2016](#Kim16eccv),  
*Real-Time 3D Reconstruction and 6-DoF Tracking with an Event Camera*.
- <a name="Gallego18cvpr"></a>Gallego, G., Rebecq, H., Scaramuzza, D.,  
*[A Unifying Contrast Maximization Framework for Event Cameras, with Applications to Motion, Depth and Optical Flow Estimation](https://arxiv.org/pdf/1804.01306.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR) 2018. [PDF](http://rpg.ifi.uzh.ch/docs/CVPR18_Gallego.pdf),  [Poster](http://rpg.ifi.uzh.ch/docs/CVPR18_Gallego_poster.pdf),  [YouTube](https://youtu.be/KFMZFhi-9Aw),  [Spotlight presentation](https://youtu.be/IOntXI5iRzA).


### Monocular Depth Estimation using Structured Light
- <a name="Brandli14fnins"></a>Brandli, C., Mantel, T.A., Hutter, M., Hoepflinger, M.A., Berner, R., Siegwart, R., Delbruck, T.,  
*[Adaptive Pulsed Laser Line Extraction for Terrain Reconstruction using a Dynamic Vision Sensor](https://doi.org/10.3389/fnins.2013.00275)*,  
Front. Neurosci. (2014) 7:275. [PDF](http://www.zora.uzh.ch/107736/1/fnins-07-00275.pdf), [YouTube](https://youtu.be/20OGD5Wwe9Q)
- <a name="Matsuda15iccp"></a>Matsuda, N., Cossairt, O., Gupta, M.,  
*[MC3D: Motion Contrast 3D Scanning](https://doi.org/10.1109/ICCPHOT.2015.7168370)*,  
IEEE Conf. Computational Photography (ICCP), Houston,TX, 2015, pp. 1-10. [PDF](http://compphotolab.northwestern.edu/wordpress/wp-content/uploads/2015/04/dvs_031.pdf), [YouTube](https://youtu.be/m7qOEsTyVwU), [Project page](http://compphotolab.northwestern.edu/project/mc3d-motion-contrast-3d-laser-scanner/)


<a name="depth-stereo"></a>
### Stereo Depth Estimation
- <a name="Schraml07visapp"></a>Schraml, C., Schon, P., Milosevic, N.,  
*[Smartcam for real-time stereo vision - address-event based embedded system](http://doi.org/10.5220/0002057604660471)*,  
Int. Conf. Computer Vision Theory and Applications (VISAPP), 2007, pp. 466-471.
- <a name="Kogler09icvs"></a>Kogler, J., Sulzbachner, C., Kubinger, W.,  
*[Bio-inspired stereo vision system with silicon retina imagers](https://doi.org/10.1007/978-3-642-04667-4_18)*,  
Int. Conf. Computer Vision Systems (ICVS), 2009, pp. 174-183. [PDF](http://adose-eu.org/documents/Paper/2009_10_13-15.pdf)
- <a name="Schraml10iscas"></a>Schraml, S., Belbachir, A. N., Milosevic, N., Schon, P.,  
*[Dynamic stereo vision system for real-time tracking](https://doi.org/10.1109/ISCAS.2010.5537289)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2010, pp. 1409-1412.
- <a name="Belbachir10icdsc"></a>Belbachir, A., Pflugfelder, R., Gmeiner, P.,  
*[A Neuromorphic Smart Camera for Real-time 360deg distortion-free Panoramas](https://doi.org/10.1145/1865987.1866022)*,  
IEEE Conference on Distributed Smart Cameras, 2010.
- <a name="Kogler11atasc"></a>Kogler, J., Sulzbachner, C., Humenberger, M., Eibensteiner, F.,  
*[Address-Event Based Stereo Vision with Bio-Inspired Silicon Retina Imagers](http://doi.org/10.5772/12941)*,  
Advances in Theory and Applications of Stereo Vision (2011), pp. 165-188.
- <a name="Kogler11icvs"></a>Kogler, J., Humenberger, M., Sulzbachner, C.,  
*[Event-Based Stereo Matching Approaches for Frameless Address Event Stereo Data](http://doi.org/10.1007/978-3-642-24028-7_62)*,  
Int. Symp. Visual Computing (ISVC) 2011, Advances in Visual Computing, pp. 674-685.
- <a name="Benosman11tnn"></a>Benosman, R., Ieng, S. H., Rogister, P., Posch, C.,  
*[Asynchronous Event-Based Hebbian Epipolar Geometry](https://doi.org/10.1109/TNN.2011.2167239)*,  
IEEE Trans. Neural Netw., 22(11):1723-1734, 2011.
- <a name="Rogister12tnnls"></a>Rogister, P. , Benosman, R., Ieng, S.-H., Lichtsteiner, P., Delbruck, T.,  
*[Asynchronous Event-Based Binocular Stereo Matching](https://doi.org/10.1109/TNNLS.2011.2180025)*,  
IEEE Trans. Neural Netw. Learn. Syst., 23(2):347-353, 2012.
- <a name="Carneiro13neunet"></a>Carneiro, J., Ieng, S.-H., Posch, C., Benosman, R.,  
*[Event-based 3D reconstruction from neuromorphic retinas](https://doi.org/10.1016/j.neunet.2013.03.006)*,  
Neural Networks (2013), 45:27-38.
- [Lee et. al., TNNLS 2014](#Lee14tnnls)
- [Carneiro, Ph.D. Thesis, 2014](#Carneiro14PhD),  
*Asynchronous Event-Based 3D Vision*.
- <a name="Piatkowska13iccvw"></a>Piatkowska, E., Belbachir, A. N., Gelautz, M.,  
*[Asynchronous Stereo Vision for Event-Driven Dynamic Stereo Sensor Using an Adaptive Cooperative Approach](https://doi.org/10.1109/ICCVW.2013.13)*,  
IEEE Int. Conf. Computer Vision Workshops (ICCVW), 2013, pp. 45-50.
- <a name="Piatkowska14mst"></a>Piatkowska, E., Belbachir, A. N., Gelautz, M.,  
*[Cooperative and asynchronous stereo vision for dynamic vision sensors](http://dx.doi.org/10.1088/0957-0233/25/5/055108)*,  
Meas. Sci. Technol. (2014), 25(5).
- <a name="Camunas14fnins"></a>Camuñas-Mesa, L. A., Serrano-Gotarredona, T., Ieng, S. H., Benosman, R. B., Linares-Barranco, B.,  
*[On the use of orientation filters for 3D reconstruction in event–driven stereo vision](https://doi.org/10.3389/fnins.2014.00048)*,  
Front. Neurosci. (2014) 8:48.
- <a name="Camunas14iscas"></a>Camuñas-Mesa, L. A., Serrano-Gotarredona, T., Linares-Barranco, B., Ieng, S., Benosman, R.,  
*[Event-Driven Stereo Vision with Orientation Filters](https://doi.org/10.1109/ISCAS.2014.6865114)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2014, pp. 257-260.
- <a name="Belbachir14cvprw"></a>Belbachir, A. N., Schraml, S., Mayerhofer, M., Hofstatter, M.,  
*[A Novel HDR Depth Camera for Real-time 3D 360-degree Panoramic Vision](https://doi.org/10.1109/CVPRW.2014.69)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2014, pp. 419-426. [PDF](http://www.cv-foundation.org/openaccess/content_cvpr_workshops_2014/W13/papers/Belbachir_A_Novel_HDR_2014_CVPR_paper.pdf)
- <a name="Eibensteiner14cvprw"></a>Eibensteiner, F., Kogler, J., Scharinger, J.,  
*[A High-Performance Hardware Architecture for a Frameless Stereo Vision Algorithm Implemented on a FPGA Platform](https://doi.org/10.1109/CVPRW.2014.97)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2014, pp. 637-644.
- <a name="Schraml15cvpr"></a>Schraml, S., Belbachir, A. N., Bischof, H.,  
*[Event-Driven Stereo Matching for Real-Time 3D Panoramic Vision](https://doi.org/10.1109/CVPR.2015.7298644)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2015, pp. 466-474. [PDF](http://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Schraml_Event-Driven_Stereo_Matching_2015_CVPR_paper.pdf). [Slides](https://www.anyline.io/wp-content/uploads/2016/03/event-driven-stereo-for-3d-360deg-panoramic-vision.pdf).
- <a name="Schraml16tie"></a>S. Schraml, A. N. Belbachir,  Bischof, H.,  
*[An Event-Driven Stereo System for Real-Time 3-D 360° Panoramic Vision](https://doi.org/10.1109/TIE.2015.2477265)*,  
IEEE Trans. Ind. Electron., 63(1):418-428, 2016.
- <a name="Firouzi16npl"></a>Firouzi, M. and Conradt, J.,  
*[Asynchronous Event-based Cooperative Stereo Matching Using Neuromorphic Silicon Retinas](http://doi.org/10.1007/s11063-015-9434-5),*  
Neural Processing Letters, 43(2):311-326, Apr. 2016. [PDF](https://mediatum.ub.tum.de/doc/1254531/131347.pdf)
- <a name="Osswald17srep"></a>Osswald, M., Ieng, S.-H., Benosman, R., Indiveri, G.,  
*[A spiking neural network model of 3D perception for event-based neuromorphic stereo vision systems](http://doi.org/10.1038/srep40703)*,  
Scientific Reports 7, Article number: 40703 (2017).
- <a name="Piatkowska17cvprw"></a>Piatkowska, E., Kogler, J., Belbachir, N., Gelautz, M.,  
*[Improved Cooperative Stereo Matching for Dynamic Vision Sensors with Ground Truth Evaluation](http://doi.org/10.1109/CVPRW.2017.51)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2017, pp. 370-377. [PDF](http://openaccess.thecvf.com/content_cvpr_2017_workshops/w4/papers/Piatkowska_Improved_Cooperative_Stereo_CVPR_2017_paper.pdf).
- <a name="Dikov17lmlncs"></a>Dikov, G., Firouzi, M., Röhrbein, F., Conradt, J., Richter, C.,  
*[Spiking Cooperative Stereo-Matching at 2 ms Latency with Neuromorphic Hardware](https://doi.org/10.1007/978-3-319-63537-8_11)*,  
Conf. Biomimetic and Biohybrid Systems. Living Machines 2017: Biomimetic and Biohybrid Systems, pp. 119-137. Lecture Notes in Computer Science, vol 10384. Springer, Cham.  [PDF](https://www.researchgate.net/publication/318449954_Spiking_Cooperative_Stereo-Matching_at_2_ms_Latency_with_Neuromorphic_Hardware),  [Videos](https://figshare.com/s/0d9fb146149b832ed8ec)
- <a name="Eibensteiner17radio"></a>Eibensteiner, F., Brachtendorf, H. G., Scharinger, J.,  
*[Event-driven stereo vision algorithm based on silicon retina sensors](http://doi.org/10.1109/RADIOELEK.2017.7937602)*,  
27th Int. Conf. Radioelektronika, Brno, 2017, pp. 1-6.
- <a name="Zou17bmvc"></a>Zou, D., Shi, F., Liu, W., Li, J., Wang, Q., Park P.-K.J., Hyunsurk, E. R.,  
*[Robust Dense Depth Map Estimation from Sparse DVS Stereos](https://www.dropbox.com/s/ee6dn8zy4odpfwl/0096.pdf?dl=1)*,  
British Machine Vision Conf. (BMVC), 2017. [Supp. Material](https://www.dropbox.com/s/eztqo109iue6ned/Active%20Papers%20Paper%2096%20%20Supplementary%20File.zip?dl=1).
- Camuñas-Mesa, L. A., Serrano-Gotarredona, T., Ieng, S., Benosman, R., Linares-Barranco, B.,  
*[Event-driven Stereo Visual Tracking Algorithm to Solve Object Occlusion](https://doi.org/10.1109/TNNLS.2017.2759326)*,  
IEEE Trans. Neural Netw. Learn. Syst., 2017.
- <a name="Xie17fnins"></a>Xie, Z., Chen, S., Orchard, G.  
*[Event-Based Stereo Depth Estimation Using Belief Propagation](https://doi.org/10.3389/fnins.2017.00535)*,  
Front. Neurosci. (2017), 11:535.  [YouTube](https://youtu.be/ngJpY1lcbdw)
- <a name="Martel18iscas"></a>Martel, J. N.; Mueller, J.; Conradt, J., Sandamirskaya, Y.,  
*[An Active Approach to Solving the Stereo Matching Problem using Event-Based Sensors](http://dx.doi.org/10.1109/ISCAS.2018.8351411)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2018, pp. 1-5.
- <a name="Andreopoulos18cvpr"></a>Andreopoulos, A., Kashyap, H.J., Nayak, T.K., Amir, A., Flickner, M.D.,  
*[A Low Power, High Throughput, Fully Event-Based Stereo System](http://openaccess.thecvf.com/content_cvpr_2018/papers/Andreopoulos_A_Low_Power_CVPR_2018_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR) 2018.
   - [Stereo Dataset](https://ibm.ent.box.com/s/3hiq58ww1pbbjrinh367ykfdf60xsfm8).
- <a name="Zhu18eccv"></a>Zhu, A., Chen, Y., Daniilidis, K.,  
*[Realtime Time Synchronized Event-based Stereo](https://arxiv.org/abs/1803.09025)*,  
European Conf. Computer Vision (ECCV) 2018. [YouTube](https://youtu.be/4oa7e4hsrYo)
- <a name="Zhou18eccv"></a>Zhou, Y., Gallego, G., Rebecq, H., Kneip, L., Li, H., Scaramuzza, D.,  
*[Semi-Dense 3D Reconstruction with a Stereo Event Camera](http://rpg.ifi.uzh.ch/docs/ECCV18_Zhou.pdf)*,  
European Conf. Computer Vision (ECCV) 2018. [Poster](http://rpg.ifi.uzh.ch/docs/ECCV18_Zhou_poster.pdf),  [YouTube](https://youtu.be/Qrnpj2FD1e4).

<a name="optical-flow-estimation"></a>
## Optical Flow Estimation
- [Cook et. al. IJCNN 2011](#Cook11ijcnn),  
*Interacting maps for fast visual interpretation*.  
Joint estimation of optical flow, image intensity and angular velocity with a rotating event camera.
- <a name="Benosman12neunet"></a>Benosman, R., Ieng, S.-H., Clercq, C., Bartolozzi, C., Srinivasan, M.,  
*[Asynchronous Frameless Event-Based Optical Flow](https://doi.org/10.1016/j.neunet.2011.11.001),*  
Neural Networks (2012), 27:32-37.
- <a name="Benosman14tnnls"></a>Benosman, R., Clercq, C., Lagorce, X., Ieng, S.-H., Bartolozzi, C.,  
*[Event-Based Visual Flow](https://doi.org/10.1109/TNNLS.2013.2273537),*  
IEEE Trans. Neural Netw. Learn. Syst., 25(2):407-417, 2014.
    - [Code (jAER): LocalPlanesFlow](https://sourceforge.net/p/jaer/code/HEAD/tree/jAER/trunk/src/ch/unizh/ini/jaer/projects/rbodo/opticalflow/LocalPlanesFlow.java)
- <a name="Orchard13biocas"></a>Orchard, G., Benosman, R., Etienne-Cummings, R., Thakor, N,  
*[A Spiking Neural Network Architecture for Visual Motion Estimation](https://doi.org/10.1109/BioCAS.2013.6679698)*,  
IEEE Biomedical Circuits and Systems Conf. (BioCAS), Rotterdam, 2013, pp. 298-301.
- <a name="Clady14fnins"></a> Clady, X., Clercq, C., Ieng, S.H., Houseini, F., Randazzo, M., Natale, L., Bartolozzi, C., Benosman, R.,  
*[Asynchronous visual event-based time-to-contact](https://dx.doi.org/10.3389%2Ffnins.2014.00009)*,  
Front. Neurosci. (2014), 8:9.
- <a name="Tschechne14annpr"></a>Tschechne, S., Sailer R., Neumann, H.,  
*[Bio-Inspired Optic Flow from Event-Based Neuromorphic Sensor Input](https://doi.org/10.1007/978-3-319-11656-3_16)*,  
IAPR Workshop on Artificial Neural Networks in Pattern Recognition (ANNPR) 2014, pp. 171-182.
- <a name="Barranco14ieee"></a>Barranco, F., Fermüller, C., Aloimonos, Y.,  
*[Contour motion estimation for asynchronous event-driven cameras](https://doi.org/10.1109/JPROC.2014.2347207)*,  
Proc. IEEE (2014), 102(10):1537-1556. [PDF](http://www.cfar.umd.edu/~fer/postscript/contourmotion-dvs-final.pdf)
- <a name="Barranco15iwann"></a>Barranco, F., Fermüller, C., Aloimonos, Y.,  
*[Bio-inspired Motion Estimation with Event-Driven Sensors](https://doi.org/10.1007/978-3-319-19258-1_27)*,  
Int. Work-Conf. Artificial Neural Networks (IWANN) 2015, Advances in Computational Intelligence, pp. 309-321.
- <a name="Conradt15robio"></a>Conradt, J.,  
*[On-Board Real-Time Optic-Flow for Miniature Event-Based Vision Sensors](https://doi.org/10.1109/ROBIO.2015.7419043)*,  
IEEE Int. Conf. Robotics and Biomimetics (ROBIO), 2015, pp. 1858-1863.
- <a name="Brosch15fnins"></a>Brosch, T., Tschechne, S., Neumann, H.,  
*[On event-based optical flow detection](https://doi.org/10.3389/fnins.2015.00137)*,  
Front. Neurosci. (2015), 9:137.
- <a name="Kosiorek15techrep"></a>Kosiorek, A., Adrian, D., Rausch, J., Conradt, J.,  
*[An Efficient Event-Based Optical Flow Implementation in C/C++ and CUDA](https://www.nst.ei.tum.de/fileadmin/w00bqs/www/publications/pp/2015SS-PP-RealTimeDVSOpticFlow.pdf),*  
Tech. Rep. TU Munich, 2015.
- <a name="Mueggler15icra"></a>E. Mueggler, C. Forster, N. Baumli, G. Gallego, D. Scaramuzza,  
*[Lifetime Estimation of Events from Dynamic Vision Sensors](http://dx.doi.org/10.1109/ICRA.2015.7139876)*,  
IEEE Int. Conf. Robotics and Automation (ICRA), 2015, pp. 4874-4881. [PDF](http://rpg.ifi.uzh.ch/docs/ICRA15_Mueggler.pdf), [PPT](http://rpg.ifi.uzh.ch/docs/ICRA15_Mueggler.pptm), [Code](https://www.github.com/uzh-rpg/rpg_event_lifetime)
- <a name="Rueckauer16fnins"></a>Rueckauer, B. and Delbruck, T.,  
*[Evaluation of Event-Based Algorithms for Optical Flow with Ground-Truth from Inertial Measurement Sensor](https://doi.org/10.3389/fnins.2016.00176),*  
Front. Neurosci (2016). 10:176.
    - [Code (jAER)](https://sourceforge.net/p/jaer/code/HEAD/tree/jAER/trunk/src/ch/unizh/ini/jaer/projects/rbodo/opticalflow/)
- <a name="Bardow16cvpr"></a>Bardow, P. A., Davison, A. J., Leutenegger, S.,  
*[Simultaneous Optical Flow and Intensity Estimation from an Event Camera](http://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Bardow_Simultaneous_Optical_Flow_CVPR_2016_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR) 2016. [YouTube](https://youtu.be/1zqJpiheaaI)
- <a name="Liu17iscas"></a>Liu, M., Delbruck, T.,  
*[Block-Matching Optical Flow for Dynamic Vision Sensors: Algorithm and FPGA Implementation](https://arxiv.org/pdf/1706.05415.pdf)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2017.
- <a name="Haessig17arxiv"></a>Haessig, G., Cassidy, A. Alvarez, R., Benosman, R., Orchard, G.,  
*[Spiking Optical Flow for Event-based Sensors Using IBM's TrueNorth Neurosynaptic System](https://arxiv.org/pdf/1710.09820.pdf)*,  
arXiv:1710.09820, 2017.
- <a name="Stoffregen17acra"></a>Stoffregen, T., Kleeman, L.,  
*[Simultaneous Optical Flow and Segmentation (SOFAS) using Dynamic Vision Sensor](http://www.araa.asn.au/acra/acra2017/papers/pap127s1-file1.pdf)*,  
Australasian Conference on Robotics and Automation (ACRA), 2017. [PDF](https://arxiv.org/pdf/1805.12326.pdf), [YouTube](https://youtu.be/JVkQOW_iUqs)
- [Gallego et. al. CVPR 2018](#Gallego18cvpr),  
*A Unifying Contrast Maximization Framework for Event Cameras, with Applications to Motion, Depth and Optical Flow Estimation*.
- <a name="Zhu18rss"></a>Zhu, A., Yuan, L., Chaney, K., Daniilidis, K.,  
*[EV-FlowNet: Self-Supervised Optical Flow Estimation for Event-based Cameras](http://www.roboticsproceedings.org/rss14/p62.pdf)*,  
Robotics: Science and Systems XIV (RSS), 2018. [PDF](https://arxiv.org/abs/1802.06898), [YouTube](https://youtu.be/eMHZBSoq0sE), [Code](https://github.com/daniilidis-group/EV-FlowNet)
- <a name="Liu18arxiv"></a>Liu, M., Delbruck, T.,  
*[Adaptive Time-Slice Block-Matching Optical Flow Algorithm for Dynamic Vision Sensors](http://bmvc2018.org/contents/papers/0280.pdf)*,  
British Machine Vision Conf. (BMVC), 2018. [Supplementary material](https://docs.google.com/document/d/10X0z4zznuV9j1OOjWpJGv-YCWujkF7FiYjG6efwUrP0/edit), [Video](https://youtu.be/fGJ8jyqziBI)

- <a name="Liu18arxiv"></a>Chengxi, Y., Anton M., Chethan P., Cornelia F. James A. Yorke,  Yiannis A.,  
*[Unsupervised Learning of Dense Optical Flow and Depth from Sparse Event Data](https://arxiv.org/pdf/1809.08625.pdf)*

<a name="image-reconstruction"></a>
## Intensity-Image Reconstruction from events
- <a name="Cook11ijcnn"></a>Cook, M., Gugelmann, L., Jug, F., Krautz, C., Steger, A.,  
*[Interacting maps for fast visual interpretation](https://doi.org/10.1109/IJCNN.2011.6033299)*,  
Int. Joint Conf. on Neural Networks (IJCNN), San Jose, CA, 2011, pp. 770-776. [YouTube](https://youtu.be/irX3Nd5U0hY)
    - <a name="Martel15irosw"></a>Martel, J. N. P., Cook, M.,  
    *[A Framework of Relational Networks to Build Systems with Sensors able to Perform the Joint Approximate Inference of Quantities](https://doi.org/10.5167/uzh-121743)*,  
    IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Workshop on Unconventional Computing for Bayesian Inference, 2015, Hamburg. [PDF](http://www.zora.uzh.ch/121743/1/RelationalNetSensor.pdf)
    - <a name="Martel15iscas"></a>Martel, J. N. P., Chau, M., Dudek, P., Cook, M.,  
    *[Toward joint approximate inference of visual quantities on cellular processor arrays](https://doi.org/10.1109/ISCAS.2015.7169083)*,  
    IEEE Int. Symp. Circuits and Systems (ISCAS), 2015, pp. 2061-2064.
- <a name="Kim14bmvc"></a>Kim, H., Handa, A., Benosman, R., Ieng, S.-H., Davison, A. J.,  
*[Simultaneous Mosaicing and Tracking with an Event Camera](http://www.bmva.org/bmvc/2014/papers/paper066/)*, 
British Machine Vision Conf. (BMVC), 2014. [PDF](http://www.bmva.org/bmvc/2014/files/paper066.pdf), [YouTube](https://youtu.be/l6qxeM1DbXU).
    - [Code for intensity reconstruction](https://github.com/uzh-rpg/rpg_image_reconstruction_from_events).
- <a name="Barua16wacv"></a>Barua, S., Miyatani, Y., Veeraraghavan, A.,  
*[Direct face detection and video reconstruction from event cameras](http://doi.org/10.1109/WACV.2016.7477561)*,  
IEEE Winter Conf. Applications of Computer Vision (WACV), Lake Placid, NY, 2016, pp. 1-9. [YouTube](https://youtu.be/yGDVlN-L1TU)
- [Bardow et. al. CVPR 2016](#Bardow16cvpr),  
*Simultaneous Optical Flow and Intensity Estimation from an Event Camera*.
- <a name="Reinbacher16bmvc"></a>Reinbacher, C., Graber, G., Pock, T.,  
*[Real-Time Intensity-Image Reconstruction for Event Cameras Using Manifold Regularisation](http://www.bmva.org/bmvc/2016/papers/paper009/)*,  
British Machine Vision Conf. (BMVC), 2016. [PDF](http://www.bmva.org/bmvc/2016/papers/paper009/paper009.pdf), [YouTube](https://youtu.be/rvB2URrGT94), [Code](https://github.com/VLOGroup/dvs-reconstruction)
- <a name="Moeys17iscas"></a>Moeys, D. P., Li, C., Martel, J. N. P., Bamford, S., Longinotti, L., Motsnyi, V., Bello, D. S. S., Delbruck, T.,  
*[Color Temporal Contrast Sensitivity in Dynamic Vision Sensors](http://dx.doi.org/10.1109/ISCAS.2017.8050412)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2017. [PDF](http://www.ini.uzh.ch/admin/extras/doc_get.php?id=65634).
- <a name="Munda18ijcv"></a>Munda, G., Reinbacher, C., Pock, T.,  
*[Real-Time Intensity-Image Reconstruction for Event Cameras Using Manifold Regularisation](https://doi.org/10.1007/s11263-018-1106-2)*,  
Int. J. of Computer Vision (IJCV), 2018.
- <a name="Shedligeri18arxiv"></a>Shedligeri, P.A., Shah, K., Kumar, D., Mitra, K.,  
*[Photorealistic Image Reconstruction from Hybrid Intensity and Event based Sensor](https://arxiv.org/pdf/1805.06140.pdf)*,  
arXiv:1805.06140, 2018.


<a name="egomotion"></a>
## Localization and Ego-Motion Estimation
- [Cook et. al. IJCNN 2011](#Cook11ijcnn),  
*Interacting maps for fast visual interpretation*.  
Joint estimation of optical flow, image intensity and angular velocity with a rotating event camera.
- <a name="Weikersdorfer12robio"></a>Weikersdorfer, D. and Conradt, J.,  
*[Event-based particle filtering for robot self-localization](http://doi.org/10.1109/ROBIO.2012.6491077)*,  
IEEE Int. Conf. on Robotics and Biomimetcs (ROBIO), Guangzhou, 2012, pp. 866-870. [PDF](https://mediatum.ub.tum.de/doc/1215541/835468.pdf)
- <a name="Censi13iros"></a>Censi, A., Strubel, J., Brandli, C., Delbruck, T., Scaramuzza, D.,  
*[Low-latency localization by Active LED Markers tracking using a Dynamic Vision Sensor](https://doi.org/10.1109/IROS.2013.6696456)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2013. [PDF](http://rpg.ifi.uzh.ch/docs/IROS13_Censi.pdf), [Slides](http://rpg.ifi.uzh.ch/docs/IROS13_Censi.ppt)
- <a name="Mueggler14iros"></a>Mueggler, E., Huber, B., Scaramuzza, D.,  
*[Event-based, 6-DOF Pose Tracking for High-Speed Maneuvers](https://doi.org/10.1109/IROS.2014.6942940)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Chicago, IL, 2014, pp. 2761-2768. [PDF](http://rpg.ifi.uzh.ch/docs/IROS14_Mueggler.pdf), [YouTube](https://youtu.be/LauQ6LWTkxM)
- <a name="Gallego15arxiv"></a>Gallego, G., Forster, C., Mueggler, E., Scaramuzza, D.,  
*[Event-based Camera Pose Tracking using a Generative Event Model](https://arxiv.org/pdf/1510.01972v1)*,  
arXiv:1510.01972, 2015.
- <a name="Mueggler15rss"></a>Mueggler, E., Gallego G., Scaramuzza, D.,   
*[Continuous-Time Trajectory Estimation for Event-based Vision Sensors](http://dx.doi.org/10.15607/RSS.2015.XI.036)*,  
Robotics: Science and Systems XI (RSS), 2015. [PDF](http://rpg.ifi.uzh.ch/docs/RSS15_Mueggler.pdf), [PPT](http://rpg.ifi.uzh.ch/docs/RSS15_Mueggler.pptm),  [Poster](http://rpg.ifi.uzh.ch/docs/RSS15_Mueggler_poster.pdf)
- <a name="Reverter16fnins"></a>Reverter Valeiras, D., Orchard, G., Ieng, S.-H., Benosman, R.,  
*[Neuromorphic Event-Based 3D Pose Estimation](https://doi.org/10.3389/fnins.2015.00522)*.  
Front. Neurosci. (2016), 9:522.  
- <a name="Gallego16arxiv"></a>Gallego, G., Lund, J.E.A., Mueggler, E., Rebecq, H., Delbruck, T., Scaramuzza, D.,  
*[Event-based, 6-DOF Camera Tracking from Photometric Depth Maps](http://dx.doi.org/10.1109/TPAMI.2017.2769655)*,  
IEEE Trans. Pattern Anal. Machine Intell. (TPAMI), 2017. [PDF](http://rpg.ifi.uzh.ch/docs/PAMI17_Gallego.pdf),  [YouTube](https://youtu.be/iZZ77F-hwzs?t=5)
- <a name="Reinbacher17iccp"></a>Reinbacher, C., Munda, G., Pock, T.,  
*[Real-Time Panoramic Tracking for Event Cameras](https://doi.org/10.1109/ICCPHOT.2017.7951488)*,  
IEEE Int. Conf. Computational Photography (ICCP), 2017, pp. 1-9. [PDF](https://arxiv.org/abs/1703.05161), [YouTube](https://youtu.be/Qy0brSlirmk), [Code](https://github.com/VLOGroup/dvs-panotracking)
- [Mueggler et. al. IJRR 2017](#Mueggler17ijrr).  
*The Event-Camera Dataset and Simulator: Event-based Data for Pose Estimation, Visual Odometry, and SLAM.*
- <a name="Vasco17icar"></a>Vasco, V., Glover, A., Mueggler, E., Scaramuzza, D., Natale, L., Bartolozzi, C.  
*[Independent Motion Detection with Event-driven Cameras](http://doi.org/10.1109/ICAR.2017.8023661)*,  
Int. Conf. Advanced Robotics (ICAR), 2017, pp. 530-536. [PDF](https://arxiv.org/pdf/1706.08713v2.pdf)
- <a name="Nguyen17arxiv"></a> Nguyen, A., Do, T.-T., Caldwell, D. G., Tsagarakis, N. G.,  
*[Real-Time 6DOF Pose Relocalization for Event Cameras with Stacked Spatial LSTM Networks](https://arxiv.org/abs/1708.09011)*,  
arXiv:1708.09011.
- [Maqueda et. al. CVPR 2018](#Maqueda18cvpr).  
*Event-based Vision meets Deep Learning on Steering Prediction for Self-driving Cars.*

<a name="VOSLAM"></a>
## Visual Odometry and SLAM (Simultaneous Localization And Mapping)
- <a name="Weikersdorfer13icvs"></a>Weikersdorfer, D., Hoffmann, R., Conradt. J.,  
*[Simultaneous localization and mapping for event-based vision systems](http://doi.org/10.1007/978-3-642-39402-7_14)*.  
Int. Conf. Computer Vision Systems (ICVS), 2013, pp. 133-142. [PDF](https://mediatum.ub.tum.de/doc/1191908/271955.pdf), [Slides](http://workshops.acin.tuwien.ac.at/ICVS/downloads/ICVS2013-ebslam_weikersdorfer.pdf)
- <a name="Censi14icra"></a>Censi, A. and Scaramuzza, D.,  
*[Low-latency Event-based Visual Odometry](https://doi.org/10.1109/ICRA.2014.6906931)*,  
IEEE Int. Conf. Robotics and Automation (ICRA), 2014, pp. 703-710. [PDF](http://rpg.ifi.uzh.ch/docs/ICRA14_Censi.pdf), [Slides](https://censi.science/pub/research/2013-dvsd/201405-icra15-dvsd.pdf)
- <a name="Weikersdorfer14icra"></a>Weikersdorfer, D., Adrian, D. B., Cremers, D., Conradt, J.,  
*[Event-based 3D SLAM with a depth-augmented dynamic vision sensor](https://doi.org/10.1109/ICRA.2014.6906882)*,  
IEEE Int. Conf. Robotics and Automation (ICRA), 2014, pp. 359-364.
- [Weikersdorfer, Ph.D. Thesis, 2014](#Weikersdorfer14PhD),  
*Efficiency by Sparsity: Depth-Adaptive Superpixels and Event-based SLAM*.
- <a name="Kueng16iros"></a>Kueng, B., Mueggler, E., Gallego, G., Scaramuzza, D.,  
*[Low-Latency Visual Odometry using Event-based Feature Tracks](https://doi.org/10.1109/IROS.2016.7758089)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2016, pp. 16-23. [PDF](http://rpg.ifi.uzh.ch/docs/IROS16_Kueng.pdf). [YouTube](https://youtu.be/RDu5eldW8i8)
- <a name="Kim16eccv"></a>Kim, H., Leutenegger, S., Davison, A.J.,  
*[Real-Time 3D Reconstruction and 6-DoF Tracking with an Event Camera](http://doi.org/10.1007/978-3-319-46466-4_21)*,  
European Conference on Computer Vision (ECCV), 2016, pp. 349-364. [PDF](https://www.doc.ic.ac.uk/~ajd/Publications/kim_etal_eccv2016.pdf), [YouTube](https://youtu.be/yHLyhdMSw7w)
- <a name="Rebecq17ral"></a>Rebecq, H., Horstschaefer, T., Gallego, G., Scaramuzza, D.,  
*[EVO: A Geometric Approach to Event-based 6-DOF Parallel Tracking and Mapping in Real-time](https://doi.org/10.1109/LRA.2016.2645143)*,  
IEEE Robotics and Automation Letters (RA-L), 2(2):593-600, 2017. [PDF](http://rpg.ifi.uzh.ch/docs/RAL16_EVO.pdf),  [PPT](http://rpg.ifi.uzh.ch/docs/ICRA17_EVO.pptx),  [Poster](http://rpg.ifi.uzh.ch/docs/RAL16_EVO_poster.pdf),  [Youtube](https://youtu.be/bYqD2qZJlxE).
- <a name="Gallego17ral"></a>Gallego, G. and Scaramuzza, D.,  
*[Accurate Angular Velocity Estimation with an Event Camera](https://doi.org/10.1109/LRA.2016.2647639)*,  
IEEE Robotics and Automation Letters (RA-L), 2(2):632-639, 2017.
[PDF](http://rpg.ifi.uzh.ch/docs/RAL16_Gallego.pdf),  [PPT](http://rpg.ifi.uzh.ch/docs/RAL16_Gallego.pptx),  [Youtube](https://youtu.be/v1sXWoOAs_0).
- [Mueggler et. al. IJRR 2017](#Mueggler17ijrr).  
*The Event-Camera Dataset and Simulator: Event-based Data for Pose Estimation, Visual Odometry, and SLAM.*
- [Gallego et. al. CVPR 2018](#Gallego18cvpr),  
*A Unifying Contrast Maximization Framework for Event Cameras, with Applications to Motion, Depth and Optical Flow Estimation*.


<a name="visual-inertial"></a>
## Visual-Inertial State Estimation
- <a name="Mueggler18tro"></a>Mueggler, E., Gallego, G., Rebecq, H., Scaramuzza, D.,  
*[Continuous-Time Visual-Inertial Odometry for Event Cameras](http://rpg.ifi.uzh.ch/docs/TRO18_Mueggler.pdf)*,  
IEEE Transactions on Robotics, 2018.
- [Mueggler et. al. IJRR 2017](#Mueggler17ijrr).  
*The Event-Camera Dataset and Simulator: Event-based Data for Pose Estimation, Visual Odometry, and SLAM.*
- <a name="Zhu17cvpr"></a>Zhu, A., Atanasov, N., Daniilidis, K.,  
*[Event-based Visual Inertial Odometry](https://doi.org/10.1109/CVPR.2017.616)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR) 2017. [PDF](http://openaccess.thecvf.com/content_cvpr_2017/papers/Zhu_Event-Based_Visual_Inertial_CVPR_2017_paper.pdf), [Supplementary material](http://openaccess.thecvf.com/content_cvpr_2017/supplemental/Zhu_Event-Based_Visual_Inertial_2017_CVPR_supplemental.zip), [YouTube](https://youtu.be/9zGoR67l9Wc).
- <a name="Rebecq17bmvc"></a>Rebecq, H., Horstschaefer, T., Scaramuzza, D.,  
*[Real-time Visual-Inertial Odometry for Event Cameras using Keyframe-based Nonlinear Optimization](http://rpg.ifi.uzh.ch/docs/BMVC17_Rebecq.pdf)*,  
British Machine Vision Conf. (BMVC), 2017. [PDF](http://rpg.ifi.uzh.ch/docs/BMVC17_Rebecq.pdf), [Appendix](http://rpg.ifi.uzh.ch/docs/BMVC17_Rebecq_appendix.pdf), [YouTube](https://youtu.be/F3OFzsaPtvI), [Project page](http://rpg.ifi.uzh.ch/ultimateslam.html), [PPT](http://rpg.ifi.uzh.ch/docs/BMVC17_Rebecq.pptx), [Oral presentation](https://youtu.be/iYptNMqK0tQ).
- <a name="Rosinol18ral"></a>Rosinol Vidal, A., Rebecq, H., Horstschaefer, T., Scaramuzza, D.,  
*[Ultimate SLAM? Combining Events, Images, and IMU for Robust Visual SLAM in HDR and High Speed Scenarios](https://doi.org/10.1109/LRA.2018.2793357)*,  
IEEE Robotics and Automation Letters (RA-L), 3(2):994-1001, Apr. 2018. [PDF](http://rpg.ifi.uzh.ch/docs/RAL18_VidalRebecq.pdf), [YouTube](https://youtu.be/jIvJuWdmemE), [Poster](http://rpg.ifi.uzh.ch/docs/RAL18_VidalRebecq_poster.pdf), [Project page](http://rpg.ifi.uzh.ch/ultimateslam.html), [ICRA18 video pitch](https://youtu.be/0hDGFFJQfmA).
 

<a name="visual-stabilization"></a>
## Visual Stabilization
- <a name="Delbruck14iscas"></a>Delbruck, T., Villanueva, V., Longinotti, L.,  
*[Integration of dynamic vision sensor with inertial measurement unit for electronically stabilized event-based vision](http://doi.org/10.1109/ISCAS.2014.6865714)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2014, pp. 2636-2639. [YouTube](https://youtu.be/Tzy4WF6Qp-Y)

<a name="video-processing"></a>
## Video Processing
- <a name="Brandli14iscas"></a>Brandli, C., Muller, L., Delbruck, T.,  
*[Real-time, high-speed video decompression using a frame- and event-based DAVIS sensor](https://doi.org/10.1109/ISCAS.2014.6865228)*,  
IEEE Int. Symp. on Circuits and Systems (ISCAS), 2014, pp. 686-689.


<a name="pattern-recognition"></a>
## Pattern Recognition
- Serrano-Gotarredona, R., Oster, M., Lichtsteiner, P., Linares-Barranco, A., Paz-Vicente, R., Gómez-Rodríguez, F., Camuñas-Mesa, L., Berner, R., Rivas, M., Delbrück, T., Liu, S. C., Douglas, R., Häfliger, P., Jiménez-Moreno, G., Civit, A., Serrano-Gotarredona, T., Acosta-Jiménez, A., Linares-Barranco, B.,  
*[CAVIAR: A 45k-Neuron, 5M-Synapse, 12G-connects/sec AER Hardware Sensory-Processing-Learning-Actuating System for High Speed Visual Object Recognition and Tracking](https://doi.org/10.1109/TNN.2009.2023653)*,  
IEEE Trans. on Neural Netw., 20(9):1417-1438, 2009. [PDF](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.192.1326&rep=rep1&type=pdf)
- <a name="Belbachir11tie"></a>Belbachir, A., Hofstaetter, M., Litzenberger, M., Schoen, P.,  
*[High Speed Embedded Object Analysis Using a Dual-Line Timed-Address-Event Temporal Contrast Vision Sensor](https://doi.org/10.1109/TIE.2010.2095390)*,  
IEEE Trans. Ind. Electron., 58(3):770-783, 2011.
- Camuñas-Mesa, L., Zamarreño-Ramos, C., Linares-Barranco, A., Acosta-Jiménez, A., Serrano-Gotarredona, T., Linares-Barranco, B.  
*[An Event-Driven Multi-Kernel Convolution Processor Module for Event-Driven Vision Sensors](https://doi.org/10.1109/JSSC.2011.2167409)*,  
IEEE J. of Solid-State Circuits, 47(2):504-517, 2012.
- <a name="Lee12iscas"></a>Lee, J., Delbruck, T., Park, P. K. J., Pfeiffer, M., Shin, C. W., Ryu, H., Kang, B. C.,  
*[Live demonstration: Gesture-Based remote control using stereo pair of dynamic vision sensors](https://doi.org/10.1109/ISCAS.2012.6272144)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS) 2012, pp. 736-740. [PDF](http://www.zora.uzh.ch/75315/1/Lee_et_al_Live_demonstration.pdf), [YouTube](https://youtu.be/IlKimfJN21A)
- Pérez-Carrasco, J. A., Zhao, B., Serrano, C., Acha, B., Serrano-Gotarredona, T., Chen, S., Linares-Barranco, B.,  
*[Mapping from Frame-Driven to Frame-Free Event-Driven Vision Systems by Low-Rate Rate-Coding and Coincidence Processing. Application to Feed-Forward ConvNets](https://doi.org/10.1109/TPAMI.2013.71)*,  
IEEE Trans. Pattern Anal. Machine Intell. (TPAMI), 35(11):2706-2719, 2013.
- <a name="Lee14tnnls"></a>Lee, J. H., Delbruck, T., Pfeiffer, M., Park, P. K. J., Shin, C.-W., Ryu, H., Kang, B. C.,  
*[Real-Time Gesture Interface Based on Event-Driven Processing From Stereo Silicon Retinas](https://doi.org/10.1109/TNNLS.2014.2308551)*,  
IEEE Trans. Neural Netw. Learn. Syst., 25(12):2250-2263, 2014.
- <a name="Orchard15tpami"></a>Orchard, G., Meyer, C., Etienne-Cummings, R., Posch, C., Thakor, N., Benosman, R.,  
*[HFIRST: A Temporal Approach to Object Recognition](https://doi.org/10.1109/TPAMI.2015.2392947)*,  
IEEE Trans. Pattern Anal. Machine Intell. (TPAMI), 37(10):2028-2040, 2015. [PDF](https://arxiv.org/pdf/1508.01176.pdf)
    - [Code](http://www.garrickorchard.com/code/hfirst): HFIRST: A simple spiking neural network for recognition based on the canonical frame-based HMAX model.
- Zhao, B., Ding, R., Chen, S., Linares-Barranco, B., Tang, H.,  
*[Feedforward Categorization on AER Motion Events using Cortex-like Features in a Spiking Neural Network](https://doi.org/10.1109/TNNLS.2014.2362542)*,  
IEEE Trans. Neural Netw. Learn. Syst., 26(9):1963-1978, 2015.
- Park, P.K.J. et al.,  
*[Computationally efficient, real-time motion recognition based on bio-inspired visual and cognitive processing](http://dx.doi.org/10.1109/ICIP.2015.7350936)*,  
IEEE Int. Conf. Image Processing (ICIP), Quebec City, QC, 2015, pp. 932-935.
- Park, P.K.J. et al.,  
*[Performance improvement of deep learning based gesture recognition using spatiotemporal demosaicing technique](http://dx.doi.org/10.1109/ICIP.2016.7532633)*,  
IEEE Int. Conf. Image Processing (ICIP), Phoenix, AZ, 2016, pp. 1624-1628.
- [Barua et. al. WACV 2016](#Barua16wacv). Face recognition.
- <a name="Moeys16ebccsp"></a>Moeys, D., Corradi F., Kerr, E., Vance, P., Das, G., Neil, D., Kerr, D., Delbruck, T.,  
*[Steering a Predator Robot using a Mixed Frame/Event-Driven Convolutional Neural Network](https://doi.org/10.1109/EBCCSP.2016.7605233)*,  
IEEE Int. Conf. Event-Based Control Comm. and Signal Proc. (EBCCSP), 2016. [PDF](https://arxiv.org/pdf/1606.09433.pdf), [YouTube 1](https://youtu.be/fL3YCIPxuhM), [YouTube 2](https://youtu.be/lPF3Youpmqk)
- <a name="Lagorce17tpami"></a>Lagorce, X., Orchard, G., Gallupi, F., Shi, B., Benosman, R.,  
*[HOTS: A Hierarchy Of event-based Time-Surfaces for pattern recognition](https://doi.org/10.1109/TPAMI.2016.2574707)*,  
IEEE Trans. Pattern Anal. Machine Intell. (TPAMI), 39(7):1346-1359, 2017.
- [Clady et. al. FNINS](#Clady17fnins),  
*A Motion-Based Feature for Event-Based Pattern Recognition*.
- <a name="Lungu17iscas"></a>Lungu, I.-A., Corradi, F., Delbruck, T.,  
*Live Demonstration: Convolutional Neural Network Driven by Dynamic Vision Sensor Playing RoShamBo*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2017. [YouTube](https://youtu.be/q5ua91n13TA), [Slides 36-39](http://rpg.ifi.uzh.ch/docs/ICRA17workshop/Delbruck.pdf)
- <a name="Amir17cvpr"></a>Amir, A., Taba, B., Berg, D., Melano, T., McKinstry, J., Di Nolfo, C., Nayak, T., Andreopoulos, A., Garreau, G., Mendoza, M., Kusnitz, J., Debole, M., Esser, S., Delbruck, T., Flickner, M., Modha, D.,  
*[A Low Power, Fully Event-Based Gesture Recognition System](https://doi.org/10.1109/CVPR.2017.781)*,  
 IEEE Conf. Computer Vision and Pattern Recognition (CVPR) 2017. [PDF](http://openaccess.thecvf.com/content_cvpr_2017/papers/Amir_A_Low_Power_CVPR_2017_paper.pdf), [Dataset](#dvsgesture_dataset) 
  - [YouTube: IBM Research demonstrates event-based gesture recognition using a brain-inspired chip](https://youtu.be/g08IW-qRomM)
- Stromatias, E., Soto, M., Serrano-Gotarredona, T., Linares-Barranco, B.,  
*[An Event-Based Classifier for Dynamic Vision Sensor and Synthetic Data](https://doi.org/10.3389/fnins.2017.00350)*,  
Front. Neurosci. (2017), 11:350.
- Yousefzadeh, A., Masquelier, T., Serrano-Gotarredona, T., Linares-Barranco, B.,  
*[Live demonstration: Hardware implementation of convolutional STDP for on-line visual feature learning](https://doi.org/10.1109/ISCAS.2017.8050395)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2017.
- <a name="Sironi18cvpr"></a>Sironi, A., Brambilla, M., Bourdis, N., Lagorce, X., Benosman, R.,    
*[HATS: Histograms of Averaged Time Surfaces for Robust Event-based Object Classification](http://openaccess.thecvf.com/content_cvpr_2018/papers/Sironi_HATS_Histograms_of_CVPR_2018_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR) 2018. [PDF](https://arxiv.org/abs/1803.07913).
    - [N-CARS Dataset](#ncars_dataset): A large real-world event-based dataset for car classification.
- <a name="Maqueda18cvpr"></a>Maqueda, A.I., Loquercio, A., Gallego, G., Garcia, N., Scaramuzza, D.,  
*[Event-based Vision meets Deep Learning on Steering Prediction for Self-driving Cars](http://openaccess.thecvf.com/content_cvpr_2018/papers/Maqueda_Event-Based_Vision_Meets_CVPR_2018_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR) 2018. [PDF](http://rpg.ifi.uzh.ch/docs/CVPR18_Maqueda.pdf), [Poster](http://rpg.ifi.uzh.ch/docs/CVPR18_Maqueda_poster.pdf),  [YouTube](https://youtu.be/_r_bsjkJTHA).
- [Zhu et. al. RSS 2018](#Zhu18rss),  
*EV-FlowNet: Self-Supervised Optical Flow Estimation for Event-based Cameras.*
- <a name="Haessig18arxiv"></a>Haessig, G. and Benosman, R.,  
*[A Sparse Coding Multi-Scale Precise-Timing Machine Learning Algorithm for Neuromorphic Event-Based Sensors](https://arxiv.org/pdf/1804.09236.pdf)*,  
arXiv: 1804.09236, 2018.
- <a name="LiuW18arxiv"></a>Liu, W., Chen, H., Goel, R., Huang, Y., Veeraraghavan, A., Patel, A.,  
*[Fast Retinomorphic Event-Driven Representations for Video Recognition and Reinforcement Learning](https://arxiv.org/pdf/1805.06374.pdf)*,  
arXiv: 1805.06374, 2018.
 
    
<a name="control"></a>
## Control
- <a name="Delbruck07iscas"></a>Delbruck, T. and Lichtsteiner, P.,  
*[Fast sensory motor control based on event-based hybrid neuromorphic-procedural system](https://doi.org/10.1109/ISCAS.2007.378038)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2007, pp. 845-848.
- <a name="Conradt09iscas"></a>Conradt, J., Cook, M., Berner, R., Lichtsteiner, P., Douglas, R. J., Delbruck, T.,  
*[A Pencil Balancing Robot Using a Pair of AER Dynamic Vision Sensors](https://doi.org/10.1109/ISCAS.2009.5117867)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS) 2009, pp. 781-784. [PDF](https://www.ini.uzh.ch/~conradt/publications/ISCAS2009-JConradt.pdf), [Poster](https://www.ini.uzh.ch/~conradt/publications/NIPS2008-JConradt.pdf), [Project page](https://www.ini.uzh.ch/~conradt/projects/PencilBalancer/), [YouTube 1](https://youtu.be/XVR5wEYkEGk), [YouTube 2](https://youtu.be/f9UngTdngY4), [YouTube 3](https://youtu.be/yCOnDc5r7p8)
- <a name="Conradt09iccvw"></a>Conradt, J., Berner, R., Cook, M., Delbruck, T.,  
*[An embedded AER dynamic vision sensor for low-latency pole balancing](https://doi.org/10.1109/ICCVW.2009.5457625)*,  
IEEE Int. Conf. Computer Vision Workshops (ICCVW), 2009. [PDF](http://www.ini.uzh.ch/admin/extras/doc_get.php?id=42580)
- <a name="Delbruck13fnins"></a>Delbruck, T. and Lang, M.,  
*[Robotic Goalie with 3ms Reaction Time at 4% CPU Load Using Event-Based Dynamic Vision Sensor](https://doi.org/10.3389/fnins.2013.00223)*,  
Front. Neurosci. (2013), 7:223. [PDF](http://www.zora.uzh.ch/107801/1/fnins-07-00223.pdf), [YouTube](https://youtu.be/IC5x7ftJ96w)
- <a name="Censi15acc"></a>Censi, A.,  
*[Efficient Neuromorphic Optomotor Heading Regulation](https://doi.org/10.1109/ACC.2015.7171931)*,  
American Control Conference (ACC), Chicago, IL, 2015, pp. 3854-3861.
- <a name="Mueggler15ecmr"></a>Mueggler, E., Baumli, N., Fontana, F., Scaramuzza, D.,  
*[Towards Evasive Maneuvers with Quadrotors using Dynamic Vision Sensors](https://doi.org/10.1109/ECMR.2015.7324048)*,  
Eur. Conf. Mobile Robots (ECMR), Lincoln, 2015. [PDF](http://rpg.ifi.uzh.ch/docs/ECMR15_Mueggler.pdf)
- <a name="Delbruck15iscas"></a>Delbruck, T., Pfeiffer, M., Juston, R., Orchard, G., Mueggler, E., Linares-Barranco, A., Tilden, M. W.,  
*[Human vs. computer slot car racing using an event and frame-based DAVIS vision sensor](https://doi.org/10.1109/ISCAS.2015.7169170)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2015, pp. 2409-2412. [YouTube 1](https://youtu.be/CnGPGiZuFRI), [YouTube 2](https://youtu.be/ALneVn-Ls2Q)
- [Moeys et. al. EBCCSP 2016](#Moeys16ebccsp).  *VISUALISE Predator/Prey Dataset*.
- <a name="Vasco16humanoids"></a>Vasco, V., Glover, A., Tirupachuri, Y., Solari, F., Chessa M., Bartolozzi C.,  
*[Vergence control with a neuromorphic iCub](https://doi.org/10.1109/HUMANOIDS.2016.7803355)*,  
IEEE Int. Conf. Humanoid Robotics (Humanoids), 2016, pp. 732-738.


<a name="space"></a>
## Space Applications
- <a name="Cohen17amos"></a>Cohen, G., Afshar, S., van Schaik, A., Wabnitz, A., Bessell, T., Rutten, M., Morreale, B.,  
*[Event-based Sensing for Space Situational Awareness](https://amostech.com/TechnicalPapers/2017/Optical-Systems/Cohen.pdf)*,  
Proc. Advanced Maui Optical and Space Surveillance (AMOS) Technologies Conf., 2017.
- <a name="Cheung18fusion"></a>
Cheung, B., Rutten, M., Davey, S., Cohen, G.,  
*[Probabilistic Multi Hypothesis Tracker for an Event Based Sensor](http://dx.doi.org/10.23919/ICIF.2018.8455718)*,  
Int. Conf. Information Fusion (FUSION) 2018, pp. 1-8.


<a name="slip_detection"></a>
## Slip detection (Manipulation)
- <a name="Rigi18sensors"></a>Rigi, A., Baghaei Naeini, F., Makris, D., Zweiri, Y.,  
*[A Novel Event-Based Incipient Slip Detection Using Dynamic Active-Pixel Vision Sensor (DAVIS)](https://doi.org/10.3390/s18020333)*,  
Sensors 2018, 18, 333.


<br><br>
<a name="datasets"></a>
# Datasets and Simulators (sorted by topic)
- [Datasets from the Sensors group at INI](http://sensors.ini.uzh.ch/databases.html) (Institute of Neuroinformatics), Zurich:
    - DVS09 - 	DVS128 Dynamic Vision Sensor Silicon Retina
    - DVSFLOW16 - 	DVS/DAVIS Optical Flow Dataset
    - DVSACT16 -	DVS Datasets for Object Tracking, Action Recognition and Object Recognition
    - PRED18 - 	VISUALISE Predator/Prey Dataset
    - DDD17 - 	DAVIS Driving Dataset 2017
    - ROSHAMBO17 - 	RoShamBo Rock Scissors Paper game DVS dataset
    - DHPE17 - 	DAVIS Human Pose Estimation and Action Recognition
    
### Optical Flow
- [DVS/DAVIS Optical Flow Dataset](https://docs.google.com/document/d/1r9sRYANGuDTUcfSSq-sL4sd79SfjHGNRul_10uztDaI/pub) associated to the paper [Rueckauer and Delbruck, FNINS 2016](#Rueckauer16fnins).
- [Binas et. al. ICML 2017](#Binas17icml). *DDD17: End-To-End DAVIS Driving Dataset*.
- [Bardow et al. CVPR2016](#Bardow16cvpr), [Four sequences](http://wp.doc.ic.ac.uk/pb2114/datasets/)
- [Zhu et al. RAL2018](#Zhu18mvsec): *MVSEC The Multi Vehicle Stereo Event Camera Dataset*.

### Visual Odometry and SLAM
- [Combined Dynamic Vision / RGB-D Dataset](http://ci.nst.ei.tum.de/EBSLAM3D/dataset/) associated to the paper [Weikersdorfer et. al. ICRA 2014](#Weikersdorfer14icra).
- Barranco, F., Fermuller, C., Aloimonos, Y.,  
*[A Dataset for Visual Navigation with Neuromorphic Methods](https://dx.doi.org/10.3389%2Ffnins.2016.00049),*  
Front. Neurosci. (2016), 10:49.
- <a name="Mueggler17ijrr"></a>E. Mueggler, H. Rebecq, G. Gallego, T. Delbruck, D. Scaramuzza,  
*[The Event-Camera Dataset and Simulator: Event-based Data for Pose Estimation, Visual Odometry, and SLAM](http://rpg.ifi.uzh.ch/davis_data.html),*  
Int. J. Robotics Research, 36:2, pp. 142-149, 2017. [PDF](https://arxiv.org/pdf/1610.08336.pdf), [PDF IJRR](http://dx.doi.org/10.1177/0278364917691115), [Dataset](http://rpg.ifi.uzh.ch/davis_data.html).
- <a name="Binas17icml"></a>Binas, J., Neil, D., Liu, S.-C., Delbruck, T.,  
*[DDD17: End-To-End DAVIS Driving Dataset](https://www.openreview.net/pdf?id=HkehpKVG-),*  
Int. Conf. Machine Learning, Sydney, Australia, PMLR 70, 2017. [Dataset](http://sensors.ini.uzh.ch/databases.html)
- <a name="Zhu18mvsec"></a>Zhu, A., Thakur, D., Ozaslan, T., Pfrommer, B., Kumar, V., Daniilidis, K.,  
*[The Multi Vehicle Stereo Event Camera Dataset: An Event Camera Dataset for 3D Perception](https://doi.org/10.1109/LRA.2018.2800793),*  
IEEE Robotics and Automation Letters 3(3):2032-2039, Feb. 2018. [PDF](https://arxiv.org/abs/1801.10202), [Dataset](https://daniilidis-group.github.io/mvsec/), [YouTube](https://youtu.be/9FaUvvzaHW8).

### Recognition
- <a name="Orchard15fnins"></a>Orchard, G., Jayawant, A., Cohen, G.K., Thakor, N.,  
*[Converting Static Image Datasets to Spiking Neuromorphic Datasets Using Saccades](https://doi.org/10.3389/fnins.2015.00437),*  
Front. Neurosci. (2015), 9:437. [YouTube](https://youtu.be/2RBKNhxHvdw)
    - [Neuromorphic-MNIST (N-MNIST) dataset](http://www.garrickorchard.com/datasets/n-mnist) is a spiking version of the original frame-based MNIST dataset (of handwritten digits). [YouTube](https://youtu.be/6qK97qM5aB4)
    - [The Neuromorphic-Caltech101 (N-Caltech101) dataset](http://www.garrickorchard.com/datasets/n-caltech101) is a spiking version of the original frame-based Caltech101 dataset. [YouTube](https://youtu.be/dxit9Ce5f_E)
- Serrano-Gotarredona,T. and Linares-Barranco, B.,  
*[Poker-DVS and MNIST-DVS. Their History, How They were Made, and Other Details](http://dx.doi.org/10.3389/fnins.2015.00481)*,  
Front. Neurosci. (2015), 9:481.
    - [MNIST-DVS and FLASH-MNIST-DVS datasets](http://www2.imse-cnm.csic.es/caviar/MNISTDVS.html) are based on the original frame-based MNIST dataset. MNIST-DVS are DVS128 recordings of moving MNIST digits (at 3 scales), while FLASH-MNIST-DVS datasets are recorded by flashing the digits on a monitor.
    - [POKER-DVS](http://www2.imse-cnm.csic.es/caviar/POKERDVS.html). From a set of DVS recordings of very fast poker card browsing, 32x32 pixel windows tracking the symbols are cropped. On average each symbol lasts about 10-30ms.
    - [SLOW-POKER-DVS](http://www2.imse-cnm.csic.es/caviar/SLOWPOKERDVS.html). Paper printed poker card symbols are moved at "human speed" in front of a DVS camera and recorded at 128x128 resolution.
- [VISUALISE Predator/Prey Dataset](https://www.dropbox.com/sh/x6nm6zl9rrd7yzn/AAB_Fa5F-Y4fSo1nrIJxc8Xoa?dl=0) associated to the paper [Moeys et. al. EBCCSP 2016](#Moeys16ebccsp)
- <a name="Hu16fnins"></a>Hu, Y., Liu, H., Pfeiffer, M., Delbruck, T.,  
*[DVS Benchmark Datasets for Object Tracking, Action Recognition, and Object Recognition](https://doi.org/10.3389/fnins.2016.00405),*  
Front. Neurosci. (2016), 10:405. [Dataset](http://dgyblog.com/projects-term/dvs-dataset.html)
- <a name="Liu16fnins">Liu, Q., Pineda-García, G., Stromatias, E., Serrano-Gotarredona, T., Furber, SB.,  
*[Benchmarking Spike-Based Visual Recognition: A Dataset and Evaluation](https://doi.org/10.3389/fnins.2016.00496)*,  
Front. Neurosci. (2016), 10:496. [Dataset](https://github.com/qian-liu/benchmarking), [Dataset](https://github.com/NEvision/NE15)
- <a name="dvsgesture_dataset"></a>[DVS128 Gesture Dataset](http://research.ibm.com/dvsgesture/): The dataset that was used to build the real-time gesture recognition system described in [Amir et al. CVPR 2017](#Amir17cvpr).
- <a name="ncars_dataset"></a>[N-CARS Dataset](http://www.prophesee.ai/dataset-n-cars/): A large real-world event-based dataset for car classification.     [Sironi et al. CVPR 2018](#Sironi18cvpr).
- [Mitrokhin et. al. IROS 2018](#Mitrokhin18iros) *Event-based Moving Object Detection and Tracking*. [Project page and Dataset](http://prg.cs.umd.edu/BetterFlow.html)

<br><br>
<a name="software"></a>
# Software

<a name="drivers"></a>
## Drivers
- [jAER (java Address-Event Representation) project](http://jaerproject.org/). *Real time sensory-motor processing for event-based sensors and systems*. [github page](https://github.com/SensorsINI/jaer). [Wiki](https://sourceforge.net/p/jaer/wiki/Home/)
- [caer (AER event-based framework, written in C, targeting embedded systems)](https://github.com/inilabs/caer)
- [libcaer (Minimal C library to access, configure and get/send AER data from sensors or to/from neuromorphic processors)](https://github.com/inilabs/libcaer)
- [ROS (Robotic Operating System)](https://github.com/uzh-rpg/rpg_dvs_ros)
- [YARP (Yet Another Robot Platform)](https://github.com/robotology/event-driven)


<a name="calibration"></a>
## Calibration
- [Lens focus adjustment](https://github.com/uzh-rpg/rpg_dvs_ros/tree/master/dvs_calibration#focus-adjustment) or [this other source](https://github.com/ethz-asl/kalibr/wiki/calibrating-the-vi-sensor#2-setting-the-focus).
- For the DAVIS: use the grayscale frames to calibrate the optics of both frames and events.
    - ROS camera calibrator ([monocular](http://wiki.ros.org/camera_calibration/Tutorials/MonocularCalibration) or [stereo](http://wiki.ros.org/camera_calibration/Tutorials/StereoCalibration))
     - [kalibr software](https://github.com/ethz-asl/kalibr/wiki/multiple-camera-calibration) by ASL - ETH.
- For the DAVIS camera and IMU calibration: [kalibr software](https://github.com/ethz-asl/kalibr/wiki/camera-imu-calibration) by ASL - ETH, using the grayscale frames.
- For the DVS (events-only):
    - [Calibration using blinking LEDs or computer screens](https://github.com/uzh-rpg/rpg_dvs_ros/tree/master/dvs_calibration) by RPG - UZH.
    - [DVS camera calibration](https://github.com/gorchard/DVScalibration) by G. Orchard.
    - [DVS camera calibration](https://github.com/VLOGroup/dvs-calibration) by VLOGroup at TU Graz.


<a name="software-algorithms"></a>
## Algorithms
- [Several event-processing filters](https://sourceforge.net/p/jaer/wiki/FilterIndex_1/) in the [jAER (java Address-Event Representation) project](http://jaerproject.org/)
- [A collection of tracking and detection algorithms](https://github.com/robotology/event-driven) using the YARP framework
- **Optical Flow**
    - [LocalPlanesFlow](https://sourceforge.net/p/jaer/code/HEAD/tree/jAER/trunk/src/ch/unizh/ini/jaer/projects/rbodo/opticalflow/LocalPlanesFlow.java), inspired by the paper [Benosman et. al. TNNLS 2014](#Benosman14tnnls).
    - [Several algorithms compared](https://sourceforge.net/p/jaer/code/HEAD/tree/jAER/trunk/src/ch/unizh/ini/jaer/projects/rbodo/opticalflow/) in the paper by [Rueckauer and Delbruck, FNINS 2016](#Rueckauer16fnins).
    - [Event-Lifetime estimation](https://www.github.com/uzh-rpg/rpg_event_lifetime), associated to the paper [Mueggler et. al. ICRA 2015](#Mueggler15icra).
    
- **Intensity-Image reconstruction**
    - [Code for intensity reconstruction](https://github.com/uzh-rpg/rpg_image_reconstruction_from_events), inspired by the paper [Kim et. al. BMVC 2014](#Kim14bmvc).
    - [DVS reconstruction code](https://github.com/VLOGroup/dvs-reconstruction) associated to the paper [Reinbacher et. al. BMVC 2016](#Reinbacher16bmvc).

- **Localization and Ego-Motion Estimation**
    - [Panoramic tracking code](https://github.com/VLOGroup/dvs-panotracking) associated to the paper [Reinbacher et. al. ICCP 2017](#Reinbacher17iccp).
    
- **Pattern Recognition**
    - [A simple spiking neural network for recognition](http://www.garrickorchard.com/code/hfirst) associated to the paper [Orchard et. al. TPAMI 2015](#Orchard15tpami).

<a name="software-utilities"></a>
## Utilities
- [Process AEDAT](https://github.com/SensorsINI/processAEDAT): useful scripts to work with data from jAER and cAER.
- [Matlab functions in jAER project](https://sourceforge.net/p/jaer/code/HEAD/tree/scripts/matlab/)
- [AEDAT Tools](https://github.com/simbamford/AedatTools/): scripts for Matlab and Python to work with aedat files. 
- [Matlab AER functions](https://github.com/gorchard/Matlab_AER_vision_functions) by G. Orchard. Some basic functions for filtering and displaying AER vision data, as well as making videos.
- [Python code for AER vision data](https://github.com/gorchard/event-Python) by G. Orchard.
- [edvstools](https://github.com/Danvil/edvstools), by D. Weikersdorfer: A collection of tools for the embedded Dynamic Vision Sensor eDVS.
- [Tarsier](https://github.com/neuromorphic-paris/tarsier) Framework for event-based Vision in C++.
- [CelexMatlabToolbox](https://github.com/yucicheung/CelexMatlabToolbox) by Yuxin Zhang. Tools to decode events generated by CeleX IV DVS, visualize them and denoise.


<br><br>
<a name="processors-platforms"></a>
# Neuromorphic Processors and Platforms
- <a name="Hofstaetter11icecs"></a>Hoffstaetter, M., Belbachir, N., Bodenstorfer, E., Schoen, P.,  
*[Multiple Input Digital Arbiter with Timestamp Assignment for Asynchronous Sensor Arrays](https://doi.org/10.1109/ICECS.2006.379767)*,
IEEE Int. Conf. Electronics, Circuits and Systems (ICECS), Nice, France, 2006.
- <a name="Belbachir08icecs"></a>Belbachir, A., Hofstaetter, M., Reisinger, K., Litzenberger, M., Schoen, P.,  
*[High-Precision Timestamping and Ultra High-Speed Arbitration of Transient Pixels' Events](https://doi.org/10.1109/ICECS.2008.4674996)*,  
Int. Conf. on Electronics, Circuits and Systems", 2008, pp. 886-889.
- <a name="Hofstaetter09biocas"></a>Hoffstaetter, M., Schoen, P., Posch, C.,  Bauer, D.,  
*[An integrated 20-bit 33/5M events/s AER sensor interface with 10ns time-stamping and hardware-accelerated event pre-processing](https://doi.org/10.1109/BIOCAS.2009.5372034)*,
IEEE BioCAS, 2009.
- <a name="Hofstaetter11icecs"></a>Hoffstaetter, M., Litzenberger, M., Matolin, D., Posch, C.,  
*[Hardware-accelerated address-event processing for high-speed visual object recognition](https://doi.org/10.1109/ICECS.2011.6122221)*,  
IEEE Int. Conf. Electronics, Circuits, and Systems (ICECS), 2011.
- [Dynamic Neuromorphic Asynchronous Processor (DYNAP) by aiCTX AG](https://ai-ctx.com/products/dynap/)
  - <a name="Qiao15fnins"></a>Qiao, N., Mostafa, H., Corradi, F., Osswald, M., Stefanini, F., Sumislawska, D., Indiveri, G.,  
  *[A reconfigurable on-line learning spiking neuromorphic processor comprising 256 neurons and 128K synapses](https://doi.org/10.3389/fnins.2015.00141),*  
  Front. Neurosci. (2015), 9:141. [PDF](https://capocaccia.ethz.ch/capo/raw-attachment/wiki/2015/hybrid15/frontiers14-nlp.pdf)
  - <a name="Indiveri15iedm"></a>Indiveri, G., Qiao, N., Corradi, F.,  
  *[Neuromorphic Architectures for Spiking	 Deep Neural Networks](https://doi.org/10.1109/IEDM.2015.7409623)*,  
  IEEE Int. Electron Devices Meeting (IEDM), Washington, DC, 2015, pp. 4.2.1-4.2.4. [PDF](http://ncs.ethz.ch/pubs/pdf/Indiveri_etal15.pdf)
- <a name="Wiesmann12cvprw"></a>Wiesmann, G., Schraml, S., Litzenberger, M., Belbachir, A. N., Hofstatter, M., Bartolozzi, C.,  
*[Event-driven embodied system for feature extraction and object recognition in robotic applications](https://doi.org/10.1109/CVPRW.2012.6238898),*  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2012, pp. 76-82.
- <a name="Galluppi14icra"></a>Galluppi, F., Denk, C., Meiner, M. C., Stewart, T. C., Plana, L. A., Eliasmith, C., Furber, S., Conradt, J.,  
*[Event-based neural computing on an autonomous mobile platform](https://doi.org/10.1109/ICRA.2014.6907270),*  
IEEE Int. Conf. Robotics and Automation (ICRA), 2014, pp. 2862-2867. [PDF](http://compneuro.uwaterloo.ca/files/publications/galluppi.2014.pdf)
- <a name="Graf14CSEDU"></a>Graf, R., King, R., Belbachir, A.,  
*[Braille Vision Using Braille Display and Bio-inspired Camera](http://dx.doi.org/10.5220/0004949302140219)*,  
Int. Conf. Computer Supported Education (CSEDU), SCITEPRESS Digital Library, (2014), pp. 214 - 219.


<br><br>
<a name="workshops"></a>
# Workshops and Tutorials
- [ICRA 2015 Workshop on Innovative Sensing for Robotics](http://innovative-sensing.mit.edu/), with a focus on Neuromorphic Sensors.
- [Event-Based Vision for High-Speed Robotics (slides)](http://www.rit.edu/kgcoe/iros15workshop/papers/IROS2015-WASRoP-Invited-04-slides.pdf) IROS 2015, Workshop on Alternative Sensing for Robot Perception.
- [ICRA 2017 First International Workshop on Event-based Vision](http://rpg.ifi.uzh.ch/ICRA17_event_vision_workshop.html).
- [The Telluride Neuromorphic Cognition Engineering Workshops](http://telluride.iniforum.ch/accounts/login/?next=/).
- [Capo Caccia Workshops toward Cognitive Neuromorphic Engineering](http://capocaccia.iniforum.ch/).
- [IEEE Embedded Vision Workshop Series](https://embeddedvisionworkshop.wordpress.com), with focus on Biologically-inspired vision and embedded systems.


<br><br>
<a name="theses"></a>
## Theses and Dissertations

<a name="theses-phd"></a>
### Dissertations
- <a name="Mahowald92PhD"></a>Mahowald, M.,  
*[VLSI Analogs of Neuronal Visual Processing: A Synthesis of Form and Function](http://resolver.caltech.edu/CaltechTHESIS:09122011-094355148)*,  
Ph.D. thesis, California Inst. Of Technology, Pasadena, CA, 1992. [PDF](
http://www.ini.uzh.ch/~tobi/papers/mishathesis.pdf)  
She won the Caltech's Clauser prize for the best PhD thesis for this work, which included the silicon retina, AER communication, and a beautiful stereopsis chip.
- <a name="Delbruck93PhD"></a>Delbrück, T.,  
*[Investigations of Analog VLSI Visual Transduction and Motion Processing](http://resolver.caltech.edu/CaltechETD:etd-07022004-144710)*,  
Ph.D. Thesis. California Inst. Of Technology, Pasadena, CA, 1993. [PDF](https://www.ini.uzh.ch/~tobi/anaprose/thesis/tobithesis.pdf)
- <a name="Lichtsteiner06PhD"></a>Lichtsteiner, P.,  
*[A temporal contrast vision sensor](https://doi.org/10.3929/ethz-a-005279479)*,  
Ph.D. Thesis, ETH Zurich, Zurich, Switzerland, 2006. [PDF](http://www.ini.uzh.ch/~tobi/papers/lichtsteinerThesis2006.pdf)
- <a name="Matolin10PhD"></a>Matolin, D.,  
*[Asynchronous CMOS image sensor with extended dynamic range and suppression of time-redundant data](http://docplayer.org/docview/27/9947799/#file=/storage/27/9947799/9947799.pdf)*,  
Ph.D. Thesis, TU Dresden & AIT, deutsch, 2010.
- <a name="Berner11PhD"></a>Berner, R.,  
*[Building Blocks for Event-Based Sensors](https://doi.org/10.3929/ethz-a-006838001)*,  
Ph.D. Thesis, ETH Zurich, Zurich, Switzerland, 2011. [PDF](https://www.research-collection.ethz.ch/bitstream/handle/20.500.11850/153098/eth-5044-02.pdf?sequence=2&isAllowed=y)
- <a name="Ni13PhD"></a>Ni, Z.,  
*[Asynchronous Event Based Vision:  Algorithms and Applications to Microrobotics](https://tel.archives-ouvertes.fr/tel-00916995/document/)*,  
Ph.D. Thesis, Université de Pierre et Marie Curie, Paris, France, 2013.
- <a name="Carneiro14PhD"></a>Carneiro, J.,  
*[Asynchronous Event-Based 3D Vision](http://www.theses.fr/2014PA066593.pdf)*,  
Ph.D. Thesis, Université de Pierre et Marie Curie, Paris, France, 2014.
- <a name="Weikersdorfer14PhD"></a>Weikersdorfer, D.,  
*[Efficiency by Sparsity: Depth-Adaptive Superpixels and Event-based SLAM](http://nbn-resolving.de/urn:nbn:de:bvb:91-diss-20140701-1173294-0-6)*,  
Ph.D. Thesis, Technical University of Munich, Munich, Germany, 2014. [PDF](https://mediatum.ub.tum.de/download/1173294/1173294.pdf)
- <a name="Borer14PhD"></a>Borer, D. J.,  
*[4D Flow Visualization with Dynamic Vision Sensors](http://dx.doi.org/10.3929/ethz-a-010344783)*,  
Ph.D. Thesis, ETH-Zurich, Zurich, Switzerland, 2014. [PDF](https://www.research-collection.ethz.ch/bitstream/handle/20.500.11850/95489/eth-47156-02.pdf?sequence=2&isAllowed=y)
- <a name="Yang15PhD"></a>Yang, M.,  
*[Silicon Retina and Cochlea with Asynchronous Delta Modulator for Spike Encoding](https://doi.org/10.3929/ethz-a-010636883)*,  
Ph.D. Thesis, ETH-Zurich, Zurich, Switzerland, 2015.
- <a name="Brandli15PhD"></a>Brändli, C.,  
*[Event-Based Machine Vision](http://dx.doi.org/10.3929/ethz-a-010402138)*,  
Ph.D. Thesis, ETH-Zurich, Zurich, Switzerland, 2015. [PDF](https://www.research-collection.ethz.ch/bitstream/handle/20.500.11850/99543/eth-47528-02.pdf?sequence=2&isAllowed=y)
- <a name="Lagorce15PhD"></a>Lagorce, X.,  
*[Computational methods for event-based signals and applications](https://tel.archives-ouvertes.fr/tel-01592392)*,  
Ph.D. Thesis, Université de Pierre et Marie Curie, Paris, France, 2015. [PDF](https://tel.archives-ouvertes.fr/tel-01592392v2/document)
- <a name="Moeys16PhD"></a>Moeys, D. P.,  
*[Analog and digital implementations of retinal processing for robot navigation systems](https://doi.org/10.3929/ethz-a-010897825)*,  
Ph.D. Thesis, ETH-Zurich, Zurich, Switzerland, 2016. [PDF](https://www.research-collection.ethz.ch/bitstream/handle/20.500.11850/156363/eth-50898-02.pdf?sequence=2&isAllowed=y)
- <a name="Cohen16PhD"></a>Cohen, G. K.,  
*[Event-Based Feature Detection, Recognition and Classification](https://tel.archives-ouvertes.fr/tel-01426001)*,  
Ph.D. Thesis, Université de Pierre et Marie Curie, Paris, France, 2016. [PDF](https://tel.archives-ouvertes.fr/tel-01426001/document)
- <a name="Li17PhD"></a>Li, C.,  
*[Two-stream vision sensors](https://doi.org/10.3929/ethz-b-000164862)*,  
Ph.D. Thesis, ETH-Zurich, Zurich, Switzerland, 2017.
- <a name="Neil17PhD"></a>Neil, D.,  
*[Deep Neural Networks and Hardware Systems for Event-driven Data](https://doi.org/10.3929/ethz-b-000168865)*,  
Ph.D. Thesis, ETH-Zurich, Zurich, Switzerland, 2017. [PDF](https://www.research-collection.ethz.ch/bitstream/handle/20.500.11850/168865/phd_thesis.pdf?sequence=3&isAllowed=y)
- <a name="Mueggler17PhD"></a>Mueggler, E.,  
*[Event-based Vision for High-Speed Robotics](http://rpg.ifi.uzh.ch/docs/PhD17_Mueggler.pdf)*,  
Ph.D. Thesis, University of Zurich, Zurich, Switzerland, 2017.
- <a name="Kim17PhD"></a>Kim, H.,  
*[Real-time visual SLAM with an event camera](http://hdl.handle.net/10044/1/59704)*,  
Ph.D. Thesis, Imperial College London, United Kingdom, 2017.
- See also [Theses from Delbruck's group at INI](https://www.ini.uzh.ch/~tobi/wiki/doku.php?id=publications#phd_thesis)

<a name="theses-master"></a>
### Masters' Theses
- <a name="Reisinger06MSc"></a>Reisinger, K.,  
*[EMC testing on Silicon Retinas](http://catalogplus.tuwien.ac.at/primo_library/libweb/action/display.do?tabs=detailsTab&ct=display&fn=search&doc=UTW_alma2164793430003336&indx=1&recIds=UTW_alma2164793430003336&recIdxs=0&elementId=0&renderMode=poppedOut&displayMode=full&frbrVersion=&vl(D487844771UI4)=20-YEAR&vl(487848257UI0)=creator&vl(drStartMonth6)=00&vl(487849216UI1)=title&&vl(drEndYear6)=Jahr&dscnt=0&vl(1UIStartWith0)=contains&vl(976016785UI2)=any&vl(1UIStartWith2)=contains&mode=Advanced&vid=UTW&vl(boolOperator1)=AND&tab=default_tab&vl(487849261UI3)=all_items&vl(freeText1)=silicon+retina&vl(drStartDay6)=00&vl(drStartYear6)=Jahr&dstmp=1518094639224&frbg=&vl(487849310UI5)=ger&vl(1UIStartWith1)=contains&srt=rank&vl(boolOperator0)=AND&vl(drEndMonth6)=00&Submit=Suche&vl(freeText2)=&vl(boolOperator2)=AND&dum=true&vl(freeText0)=Reisinger&vl(drEndDay6)=00)*,  
MSc. Thesis, TU Wien & AIT, 2006.
- <a name="Nowakowska11MSc"></a>Nowakowska, A.,  
*[Recognition of a vision approach for fall detection using a biologically inspired dynamic stereo vision sensor](http://repositum.tuwien.ac.at/obvutwhs/download/pdf/1623418?originalFilename=true)*,  
MSc. Thesis, TU Wien & AIT, 2011.
- <a name="Reingruber11MSc"></a>Reingruber, H.,  
*[An Asynchronous Data Interface for Event-based Stereo Matching](http://repositum.tuwien.ac.at/obvutwhs/download/pdf/1621666?originalFilename=true)*,  
MSc. Thesis, TU Wien & AIT, 2011.
- <a name="Zima12MSc"></a>Zima, M.,  
*[Hand/Arm Gesture Recognition based on Address-Event-Representation Data](http://repositum.tuwien.ac.at/obvutwhs/download/pdf/1623095?originalFilename=true)*,  
MSc. Thesis, TU Wien & AIT, 2012.
- <a name="Huber14MSc"></a>Huber, B.,  
*[High-Speed Pose Estimation using a Dynamic Vision Sensor](http://www.kutter-fonds.ethz.ch/App_Themes/default/datalinks/BasilHuber_UniZ_MT2014.pdf)*,  
MSc. Thesis, University of Zurich, 2014.
- <a name="Horstschaefer16MSc"></a>Horstschaefer, T.,  
*[Parallel Tracking, Depth Estimation, and Image Reconstruction with an Event Camera](http://www.kutter-fonds.ethz.ch/App_Themes/default/datalinks/2016_MT_Horstschaefer1.pdf)*,  
MSc. Thesis, University of Zurich, 2016.


<br><br>
<a name="people"></a>
# People / Organizations
- [Institute of NeuroInformatics](https://www.ini.uzh.ch/) (INI) of the University of Zurich (UZH) and ETH Zurich.
- [iniVation AG](https://www.inivation.com/) (commercialization of neuromorphic vision technology from INI).
- [Dynamic Vision Sensor (DVS) - asynchronous temporal contrast silicon retina](http://siliconretina.ini.uzh.ch/wiki/index.php)
- [Robotics and Perception Group](http://rpg.ifi.uzh.ch/research_dvs.html) (RPG-UZH).
- [Institut de la Vision](http://neuromorphic-vision.com/) Neuromorphics group Paris.
- [AIT Austrian Institute of Technology](https://www.ait.ac.at/en/research-fields/new-sensor-technologies/) Sensing & vision solutions group in Vienna.
- [Sinapse](http://sinapse.nus.edu.sg/) Singapore Institute for Neurotechnology.

<br><br>
<a name="contributing"></a>
# Contributing
Please see [CONTRIBUTING](https://github.com/uzh-rpg/event-based_vision_resources/blob/master/Contributing.md) for details.
***
