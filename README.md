# Event-based Vision Resources

## Table of Contents:
- [Devices and Manufacturers](#devices)
- [Companies working on Event-based Vision](#companies_sftwr)
- [Neuromorphic Systems](#neuromorphic-systems)

- [Algorithms](#algorithms)
    - [Feature Detection and Tracking](#feature-detection)
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

- [Datasets and Simulators](#datasets)
- [Software](#software)
    - [Drivers](#drivers)
    - [Calibration](#calibration)
    - [Algorithms](#software-algorithms)
    - [Utilities](#software-utilities)

- [Neuromorphic Processors and Platforms](#processors-platforms)
- [Workshops and Tutorials](#workshops)
- [Theses and Dissertations](#theses)
- [People / Organizations](#people)
- [Contributing](#contributing)

___
<br>

<a name="devices"></a>
# Devices & Companies Manufacturing them
- **DVS (Dynamic Vision Sensor)**: Lichtsteiner, P., Posch, C., and Delbruck, T., *[A 128x128 120dB 15μs latency asynchronous temporal contrast vision sensor](http://doi.org/10.1109/JSSC.2007.914337)*, IEEE J. Solid-State Circuits, 43(2):566-576, 2008.
    - [Product page at iniLabs](https://inilabs.com/products/dynamic-vision-sensors/). [Buy a DVS](https://inilabs.com/buy/)
    - [Introductory videos about the DVS](https://inilabs.com/videos/dvs-introduction/)
    - [iniLabs](https://inilabs.com) invents, produces and sells neuromorphic technologies for *research*.
- **DAVIS (Dynamic and Active-Pixel Vision Sensor)** :
Brandli, C., Berner, R., Yang, M., Liu, S.-C., Delbruck, T., *[A 240x180 130 dB 3 µs Latency Global Shutter Spatiotemporal Vision Sensor](https://doi.org/10.1109/JSSC.2014.2342715)*, IEEE J. Solid-State Circuits, 49(10):2333-2341, 2014.
    - [Product page at iniLabs](https://inilabs.com/products/dynamic-and-active-pixel-vision-sensor/). [Buy a DAVIS](https://inilabs.com/buy/)
    - **Color-DAVIS**: Li, C., Brandli, C., Berner, R., Liu, H., Yang, M., Liu, S.-C., Delbruck, T., *[Design of an RGBW Color VGA Rolling and Global Shutter Dynamic and Active-Pixel Vision Sensor](https://doi.org/10.1109/ISCAS.2015.7168734)*, IEEE Int. Symp. Circuits and Systems (ISCAS), Lisbon, 2015, pp. 718-721.
- **ATIS (Asynchronous Time-based Image Sensor)**: Posch, C., Matolin, D., Wohlgenannt, R. (2011). *[A QVGA 143 dB Dynamic Range Frame-Free PWM Image Sensor With Lossless Pixel-Level Video Compression and Time-Domain CDS](http://doi.org/10.1109/JSSC.2010.2085952)*, IEEE J. Solid-State Circuits, 46(1):259-275, 2011.
    - [Chronocam](http://www.chronocam.com/)
- Posch, C., Serrano-Gotarredona, T., Linares-Barranco, B., Delbruck, T.,  
*[Retinomorphic Event-Based Vision Sensors: Bioinspired Cameras With Spiking Output](https://doi.org/10.1109/JPROC.2014.2346153),*  
Proc. IEEE (2014), 102(10):1470-1484.
- **Samsung's DVS (Gen2)**
    - Son, B., et al., *[4.1 A 640×480 dynamic vision sensor with a 9µm pixel and 300Meps address-event representation](https://doi.org/10.1109/ISSCC.2017.7870263)*, IEEE Int. Solid-State Circuits Conf. (ISSCC), San Francisco, CA, 2017, pp. 66-67.
    - [Slides](http://rpg.ifi.uzh.ch/docs/ICRA17workshop/Samsung.pdf) and [Video](https://youtu.be/9t4vGSVqSAI) by [Yoel Yaffe](https://www.linkedin.com/in/yoel-yaffe-a606841/), Samsung Israel Research Center, Samsung Electronics.
- CeleX ([Hillhouse Technology](http://www.hillhouse-tech.com/), Singapore). [YouTube](https://youtu.be/Wlzc-5sgm1g)
- [Insightness AG](http://www.insightness.com/). [The Silicon Eye](http://www.insightness.com/?p=361) Technology
    - [Slides](http://rpg.ifi.uzh.ch/docs/ICRA17workshop/Insightness.pdf) and [Video](https://youtu.be/6YyOW6DDGKw) by [Christian Brandli](http://www.insightness.com/#team), CEO and co-founder of Insightness.
- [iniVation](http://inivation.com) invents, produces and sells neuromorphic technologies with a special focus on event-based vision into *business*. 
    - [Slides](http://rpg.ifi.uzh.ch/docs/ICRA17workshop/Jakobsen.pdf) by [S. E. Jakobsen](http://inivation.com/team/), CEO and co-founder of iniVation.

<a name="companies_sftwr"></a>
# Companies working on Event-based Vision
- [iniLabs](https://inilabs.com) invents, produces and sells neuromorphic technologies for *research*.
- [Samsung](www.samsung.com) develops Gen2 and Gen3 dynamic vision sensors and event-based vision solutions.
  - [IBM Research](http://www.research.ibm.com/articles/brain-chip.shtml) ([Synapse project](http://www.research.ibm.com/cognitive-computing/brainpower/)) and Samsung partenered to combine the [TrueNorth chip (brain) with a DVS (eye)](https://www.cnet.com/news/samsung-turns-ibms-brain-like-chip-into-a-digital-eye/).
- [Chronocam](http://www.chronocam.com/) develops bio-inspired and self-adapting approach to the need for visual sensing and processing in autonomous vehicles, connected devices, security and surveillance systems.
- [Insightness AG](http://www.insightness.com/) builds visual systems to give mobile devices spatial awareness. [The Silicon Eye](http://www.insightness.com/?p=361) Technology.
- [SLAMcore](https://www.slamcore.com/) develops Localisation and mapping solutions for AR/VR, robotics & autonomous vehicles.
- [iniVation](http://inivation.com) invents, produces and sells neuromorphic technologies with a special focus on event-based vision into *business*.
- [Hillhouse Technology](http://www.hillhouse-tech.com/) offer integrated sensory platforms that incorporate various components and technologies, including a processing chipset and an image sensor (a dynamic vision sensor called CeleX).

<br><br>
<a name="neuromorphic-systems"></a>
# Neuromorphic Systems
- Serrano-Gotarredona, T. , Andreou, A.G. , and Linares-Barranco, B., *[AER Image Filtering Architecture for Vision Processing Systems](https://doi.org/10.1109/81.788808)*, IEEE Trans. Circuits and Systems (Part I): Fundamental Theory and Applications, 46(9):1064-1071, 1999.
- Serrano-Gotarredona, R., Oster, M., Lichtsteiner, P., Linares-Barranco, A., Paz-Vicente, R., Gomez-Rodriguez, F., Riis, H.K., Delbruck, T., Liu, S.-H., Zahnd, S., Whatley, A.M., Douglas, R., Hafliger, P., Jimenez-Moreno, G., Civit, A.,  Serrano-Gotarredona, T., Acosta-Jimenez, A., and Linares-Barranco, B., *[AER building blocks for multi-layer multi-chip neuromorphic vision systems](http://papers.nips.cc/paper/2889-aer-building-blocks-for-multi-layer-multi-chip-neuromorphic-vision-systems.pdf)*, Advances in neural information processing systems, 1217-1224, 2006.
- <a name="Delbruck08issle"></a>Delbruck, T.,  
*[Frame-free dynamic digital vision](http://www.zora.uzh.ch/17620/)*, 
Int. Symp. Secure-Life Electronics, Advanced Electronics for Quality Life and Society, University of Tokyo, Tokyo, Japan, Mar. 6-7, 2008, pp. 21-26. Introduces the software architecture of jAER and shows examples of several event-based processing algorithms.
- Serrano-Gotarredona, R.,  Oster, M., Lichtsteiner, P.,  Linares-Barranco, A.,  Paz-Vicente, R.,  Gómez-Rodríguez, F.,  Camuñas-Mesa, L., Berner, R.,  Rivas, M.,  Delbrück, T.,  Liu, S.-C.,  Douglas, R.,  Häfliger, P.,  Jiménez-Moreno, G.,   Civit, A., Serrano-Gotarredona, T., Acosta-Jiménez, A., Linares-Barranco, B. *[CAVIAR: A 45k-Neuron, 5M-Synapse, 12G-connects/sec AER Hardware Sensory-Processing-Learning-Actuating System for High Speed Visual Object Recognition and Tracking,](https://doi.org/10.1109/TNN.2009.2023653)*, IEEE Trans. on Neural Networks, 20(9): 1417-1438, 2009.
- <a name="Liu10conb"></a>Liu, S.-C. and Delbruck, T.,  
*[Neuromorphic sensory systems](https://doi.org/10.1016/j.conb.2010.03.007)*,  
Current Opinion in Neurobiology, 20:3(288-295), 2010.
- <a name="Delbruck12eccvw"></a>Delbruck, T.,  
*[Fun with asynchronous vision sensors and processing](https://www.ini.uzh.ch/~tobi/wiki/lib/exe/fetch.php?media=delbruck_funwithasynsensors_2012.pdf)*.  
Computer Vision - ECCV 2012. Workshops and Demonstrations. Springer Berlin/Heidelberg, 2012. A position paper and summary of recent accomplishments of the INI Sensors' group.
- Zamarreño-Ramos, C., Linares-Barranco, A., Serrano-Gotarredona, T., and Linares-Barranco, B., *[Multi-Casting Mesh AER: A Scalable Assembly Approach for Reconfigurable Neuromorphic Structured AER Systems. Application to ConvNets](https://doi.org/10.1109/TBCAS.2012.2195725)* IEEE Trans. on Biomedical Circuits and Systems, 7(1): 82-102, 2013.
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
- <a name="Ni11jmcro"></a>Ni, Z., Pacoret, Benosman, R., Ieng, S., Reginer, S.,  
*[Asynchronous event-based high speed vision for microparticle tracking](http://doi.org/10.1111/j.1365-2818.2011.03565.x)*,  
J. Microscopy (2011), 245(1):236-244.
- <a name="Ni12tro"></a>Ni, Z., Bolopion, A., Agnus, J., Benosman, R., Regnier, S.,  
*[Asynchronous event-based visual shape tracking for stable haptic feedback in microrobotics](https://doi.org/10.1109/TRO.2012.2198930)*,  
IEEE Trans. Robot. (2012), 28(5):1081-1089.
- <a name="Piatkowska12cvprw"></a>Piatkowska, E., Belbachir, A. N., Schraml, S., Gelautz, M.,  
*[Spatiotemporal multiple persons tracking using Dynamic Vision Sensor](https://doi.org/10.1109/CVPRW.2012.6238892)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), Providence, RI, 2012, pp. 35-40. [PDF](https://publik.tuwien.ac.at/files/PubDat_209369.pdf)
- [Ni, Ph.D. Thesis, 2013](#Ni13PhD),  
*Asynchronous Event Based Vision:  Algorithms and Applications to Microrobotics*.
- <a name="Borer14isfv"></a>Borer, D.,  Rosgen, T.,  
*[Large-scale Particle Tracking with Dynamic Vision Sensors]()*,  
ISFV16 - 16th Int. Symp. Flow Visualization, Okinawa 2014. [Project page](http://www.ifd.mavt.ethz.ch/research/group-roesgen/dynamic-vision-sensors.html), [PDF](http://www.ifd.mavt.ethz.ch/content/dam/ethz/special-interest/mavt/fluid-dynamics/ifd-dam/research/documents/posters/experimental-methods/daniel_borer_dynamic_vision_sensor.pdf)
- <a name="Lagorce14biocas"></a>Lagorce, X., Meyer, C., Ieng, S. H., Filliat, D., Benosman, R.,  
*[Live demonstration: Neuromorphic event-based multi-kernel algorithm for high speed visual features tracking](https://doi.org/10.1109/BioCAS.2014.6981681)*,  
IEEE Biomedical Circuits and Systems Conference (BioCAS), Lausanne, 2014, pp. 178-178.
- <a name="Lagorce15tnnls"></a>Lagorce, X., Meyer, C., Ieng, S. H., Filliat, D., Benosman, R.,  
*[Asynchronous Event-Based Multikernel Algorithm for High-Speed Visual Features Tracking](https://doi.org/10.1109/TNNLS.2014.2352401)*,  
IEEE Trans. Neural Netw. Learn. Syst. (2015), 26(8):1710-1720.
- <a name="Clady15neunet"></a>Clady, X., Ieng, S.-H., Benosman, R.,  
*[Asynchronous event-based corner detection and matching](https://doi.org/10.1016/j.neunet.2015.02.013)*,  
Neural Networks (2015), 66:91-106.
- <a name="Ni15neco"></a>Ni, Z., Ieng, S. H., Posch, C., Regnier, S., Benosman, R.,  
*[Visual Tracking Using Neuromorphic Asynchronous Event-Based Cameras](https://doi.org/10.1162/NECO_a_00720)*,  
Neural Computation (2015), 27(4):925-953.
- <a name="LinaresBarranco15iscas"></a>Linares-Barranco, A., Gómez-Rodríguez, F., Villanueva, V., Longinotti, L., Delbrück, T.,    
*[A USB3.0 FPGA event-based filtering and tracking framework for dynamic vision sensors](https://doi.org/10.1109/ISCAS.2015.7169172)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), Lisbon, 2015, pp. 2417-2420.
- <a name="Barranco15iccv"></a>Barranco, F., Teo, C. L., Fermüller, C., Aloimonos, Y.,  
*[Contour Detection and Characterization for Asynchronous Event Sensors](https://doi.org/10.1109/ICCV.2015.63)*,  
IEEE Int. Conf. Computer Vision (ICCV), 2015, Santiago, Chile, pp. 486-494. [PDF](http://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Barranco_Contour_Detection_and_ICCV_2015_paper.pdf)
- <a name="Liu16iscas"></a>Liu, H., Moeys, D. P., Das, G., Neil, D., Liu, S.-C., Delbruck, T.,  
*[Combined frame- and event-based detection and tracking](https://doi.org/10.1109/ISCAS.2016.7539103)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), Montreal, QC, 2016, pp. 2511-2514.
- <a name="Tedaldi16ebccsp"></a>Tedaldi, D., Gallego, G., Mueggler, E., Scaramuzza, D.,  
*[Feature detection and tracking with the dynamic and active-pixel vision sensor (DAVIS)](https://doi.org/10.1109/EBCCSP.2016.7605086)*,  
IEEE Int. Conf. Event-Based Control Comm. and Signal Proc. (EBCCSP), Krakow, Poland, 2016. [PDF](http://rpg.ifi.uzh.ch/docs/EBCCSP16_Tedaldi.pdf), [YouTube](https://www.youtube.com/watch?v=nglfEkiK308)
- <a name="Brandli16ebccsp"></a>Braendli, C., Strubel, J., Keller, S., Scaramuzza, D., Delbruck, T.,  
*[ELiSeD - An Event-Based Line Segment Detector](https://doi.org/10.1109/EBCCSP.2016.7605244)*,  
Int. Conf. on Event-Based Control Comm. and Signal Proc. (EBCCSP), Krakow, Poland, 2016. [PDF](http://rpg.ifi.uzh.ch/docs/EBCCSP16_Braendli.pdf)
- <a name="Glover16iros"></a>Glover, A. and Bartolozzi, C.,  
*[Event-driven ball detection and gaze fixation in clutter](https://doi.org/10.1109/IROS.2016.7759345)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Daejeon, South Korea, 2016, pp. 2203-2208. [YouTube](https://youtu.be/xS-7xYRYSLc), [Code](https://github.com/robotology/event-driven)
- <a name="Vasco16iros"></a>Vasco, V., Glover, A., Bartolozzi, C.,  
*[Fast event-based Harris corner detection exploiting the advantages of event-driven cameras](https://doi.org/10.1109/IROS.2016.7759610)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Daejeon, South Korea, 2016, pp. 4144-4149. [YouTube](https://youtu.be/YkI7AfBDBKE), [Code](https://github.com/robotology/event-driven)
- <a name="Clady17fnins"></a> Clady, X., Maro, J.-M., Barré, S., Benosman, R. B.,  
*[A Motion-Based Feature for Event-Based Pattern Recognition](https://doi.org/10.3389/fnins.2016.00594)*.  
Front. Neurosci. (2017), 10:594.
- <a name="Zhu17icra"></a>Zhu, A., Atanasov, N., Daniilidis, K.,  
*[Event-based Feature Tracking with Probabilistic Data Associations](https://fling.seas.upenn.edu/~alexzhu/dynamic/event-based-feature-tracking-with-probabilistic-data-association/)*,  
IEEE Int. Conf. Robotics and Automation (ICRA), Singapore, 2017. [YouTube](https://youtu.be/m93XCqAS6Fc)
- <a name="Mueggler17bmvc"></a>Mueggler, E., Bartolozzi, C., Scaramuzza, D.,  
*Fast Event-based Corner Detection*,  
British Machine Vision Conf. (BMVC), London, 2017. [PDF](http://rpg.ifi.uzh.ch/docs/BMVC17_Mueggler.pdf), [YouTube](https://youtu.be/tgvM4ELesgI)
- <a name="Glover17iros"></a>Glover, A. and Bartolozzi, C.,  
*Robust Visual Tracking with a Freely-moving Event Camera*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Vancouver, Canada, 2017. [YouTube](https://youtu.be/xS-7xYRYSLc), [Code](https://github.com/robotology/event-driven)
- Barrios-Avilés, J., Iakymchuk, T., Samaniego, J., Rosado-Muñoz, A.,  
*[An Event-based Fast Movement Detection Algorithm for a Positioning Robot Using POWERLINK Communication](https://arxiv.org/abs/1707.07188)*,  
arXiv 1707.07188.
- Li, J., Shi, F., Liu, W., Zou, D., Wang, Q., Park, Paul-K.J., Hyunsurk, E.R.,  
*Adaptive Temporal Pooling for Object Detection using Dynamic Vision Sensor*,  
British Machine Vision Conf. (BMVC), London, 2017. [PDF](https://www.dropbox.com/s/m77i7cqqy7xbg51/0099.pdf?dl=1)

<a name="depth-estimation"></a>
## Depth Estimation (3D Reconstruction)

<a name="depth-mono"></a>
### Monocular Depth Estimation
- <a name="Rebecq16bmvc"></a>Rebecq, H., Gallego, G., Scaramuzza, D.,  
*[EMVS: Event-based Multi-View Stereo](http://www.bmva.org/bmvc/2016/papers/paper063/)*,  
British Machine Vision Conf. (BMVC), York, 2016. [PDF](http://rpg.ifi.uzh.ch/docs/BMVC16_Rebecq.pdf), [YouTube](https://www.youtube.com/watch?v=EUX3Tfx0KKE), [3D Reconstruction Experiments from a Train using an Event Camera](https://www.youtube.com/watch?v=fA4MiSzYHWA)
- [Kim et. al. ECCV 2016](#Kim16eccv),  
*Real-Time 3D Reconstruction and 6-DoF Tracking with an Event Camera*.


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
Int. Conf. Computer Vision Theory and Applications (VISAPP), Barcelona, Spain, 2007, pp. 466-471.
- <a name="Kogler09icvs"></a>Kogler, J., Sulzbachner, C., Kubinger, W.,  
*[Bio-inspired stereo vision system with silicon retina imagers](https://doi.org/10.1007/978-3-642-04667-4_18)*,  
Int. Conf. Computer Vision Systems (ICVS), 2009, pp. 174-183. [PDF](http://adose-eu.org/documents/Paper/2009_10_13-15.pdf)
- <a name="Schraml10iscas"></a>Schraml, S., Belbachir, A. N., Milosevic, N., Schon, P.,  
*[Dynamic stereo vision system for real-time tracking](https://doi.org/10.1109/ISCAS.2010.5537289)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), Paris, 2010, pp. 1409-1412.
- <a name="Kogler11atasc"></a>Kogler, J., Sulzbachner, C., Humenberger, M., Eibensteiner, F.,  
*[Address-Event Based Stereo Vision with Bio-Inspired Silicon Retina Imagers](http://doi.org/10.5772/12941)*,  
Advances in Theory and Applications of Stereo Vision (2011), pp. 165-188.
- <a name="Kogler11icvs"></a>Kogler, J., Humenberger, M., Sulzbachner, C.,  
*[Event-Based Stereo Matching Approaches for Frameless Address Event Stereo Data](http://doi.org/10.1007/978-3-642-24028-7_62)*,  
Int. Symp. Visual Computing (ISVC) 2011, Advances in Visual Computing, pp. 674-685.
- <a name="Benosman11tnn"></a>Benosman, R., Ieng, S. H., Rogister, P., Posch, C.,  
*[Asynchronous Event-Based Hebbian Epipolar Geometry](https://doi.org/10.1109/TNN.2011.2167239)*,  
IEEE Trans. Neural Netw. (2011), 22(11):1723-1734.
- [Lee et. al., ISCAS 2012](#Lee12iscas)
- <a name="Rogister12tnnls"></a>Rogister, P. , Benosman, R., Ieng, S.-H., Lichtsteiner, P., Delbruck, T.,  
*[Asynchronous Event-Based Binocular Stereo Matching](https://doi.org/10.1109/TNNLS.2011.2180025)*,  
IEEE Trans. Neural Netw. Learn. Syst., 23(2):347-353, 2012.
- <a name="Carneiro13neunet"></a>Carneiro, J., Ieng, S.-H., Posch, C., Benosman, R.,  
*[Event-based 3D reconstruction from neuromorphic retinas](https://doi.org/10.1016/j.neunet.2013.03.006)*,  
Neural Networks (2013), 45:27-38.
- [Carneiro, Ph.D. Thesis, 2014](#Carneiro14PhD),  
*Asynchronous Event-Based 3D Vision*.
- <a name="Piatkowska13iccvw"></a>Piatkowska, E., Belbachir, A. N., Gelautz, M.,  
*[Asynchronous Stereo Vision for Event-Driven Dynamic Stereo Sensor Using an Adaptive Cooperative Approach](https://doi.org/10.1109/ICCVW.2013.13)*,  
IEEE Int. Conf. Computer Vision Workshops (ICCVW), Sydney, NSW, 2013, pp. 45-50.
- <a name="Piatkowska14mst"></a>Piatkowska, E., Belbachir, A. N., Gelautz, M.,  
*[Cooperative and asynchronous stereo vision for dynamic vision sensors](http://dx.doi.org/10.1088/0957-0233/25/5/055108)*,  
Meas. Sci. Technol. (2014), 25(5).
- <a name="Lee14tnnls"></a>Lee, J. H., Delbruck, T., Pfeiffer, M., Park, P. K. J., Shin, C.-W., Ryu, H., Kang, B. C., 
*[Real-Time Gesture Interface Based on Event-Driven Processing From Stereo Silicon Retinas](https://doi.org/10.1109/TNNLS.2014.2308551)*,  
IEEE Trans. Neural Netw. Learn. Syst. (2014), 25(2):2250-2263.
- <a name="Camunas14fnins"></a>Camuñas-Mesa, L. A., Serrano-Gotarredona, T., Ieng, S. H., Benosman, R. B., Linares-Barranco, B.,  
*[On the use of orientation filters for 3D reconstruction in event–driven stereo vision](https://doi.org/10.3389/fnins.2014.00048)*,  
Front. Neurosci. (2014) 8:48.
- <a name="Camunas14iscas"></a>Camuñas-Mesa, L. A., Serrano-Gotarredona, T., Linares-Barranco, B., Ieng, S., Benosman, R.,  
*[Event-Driven Stereo Vision with Orientation Filters](https://doi.org/10.1109/ISCAS.2014.6865114)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), Melbourne VIC, 2014, pp. 257-260.
- <a name="Belbachir14cvprw"></a>Belbachir, A. N., Schraml, S., Mayerhofer, M., Hofstatter, M.,  
*[A Novel HDR Depth Camera for Real-time 3D 360-degree Panoramic Vision](https://doi.org/10.1109/CVPRW.2014.69)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2014, pp. 419-426. [PDF](http://www.cv-foundation.org/openaccess/content_cvpr_workshops_2014/W13/papers/Belbachir_A_Novel_HDR_2014_CVPR_paper.pdf)
- <a name="Eibensteiner14cvprw"></a>Eibensteiner, F., Kogler, J., Scharinger, J.,  
*[A High-Performance Hardware Architecture for a Frameless Stereo Vision Algorithm Implemented on a FPGA Platform](https://doi.org/10.1109/CVPRW.2014.97)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), Columbus, OH, 2014, pp. 637-644.
- <a name="Schraml15cvpr"></a>Schraml, S., Belbachir, A. N., Bischof, H.,  
*[Event-Driven Stereo Matching for Real-Time 3D Panoramic Vision](https://doi.org/10.1109/CVPR.2015.7298644)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), Boston, MA, 2015, pp. 466-474. [PDF](http://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Schraml_Event-Driven_Stereo_Matching_2015_CVPR_paper.pdf). [Slides](https://www.anyline.io/wp-content/uploads/2016/03/event-driven-stereo-for-3d-360deg-panoramic-vision.pdf).
- <a name="Schraml16tie"></a>S. Schraml, A. N. Belbachir,  Bischof, H.,  
*[An Event-Driven Stereo System for Real-Time 3-D 360° Panoramic Vision](https://doi.org/10.1109/TIE.2015.2477265)*,  
IEEE Trans. Ind. Electron. (2016), 63(1):418-428.
- <a name="Firouzi16npl"></a>Firouzi, M. and Conradt, J.,  
*[Asynchronous Event-based Cooperative Stereo Matching Using Neuromorphic Silicon Retinas](http://doi.org/10.1007/s11063-015-9434-5),*  
Neural Processing Letters, 2016, 43(2):311-326. [PDF](https://mediatum.ub.tum.de/doc/1254531/131347.pdf)
- <a name="Osswald17srep"></a>Osswald, M., Ieng, S.-H., Benosman, R., Indiveri, G.,  
*[A spiking neural network model of 3D perception for event-based neuromorphic stereo vision systems](http://doi.org/10.1038/srep40703)*,  
Scientific Reports 7, Article number: 40703 (2017).
- <a name="Piatkowska17cvprw"></a>Piatkowska, E., Kogler, J., Belbachir, N., Gelautz, M.,  
*[Improved Cooperative Stereo Matching for Dynamic Vision Sensors with Ground Truth Evaluation](http://doi.org/10.1109/CVPRW.2017.51)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), Honolulu, HI, USA, 2017, pp. 370-377. [PDF](http://openaccess.thecvf.com/content_cvpr_2017_workshops/w4/papers/Piatkowska_Improved_Cooperative_Stereo_CVPR_2017_paper.pdf).
- <a name="Dikov17lmlncs"></a>Dikov, G., Firouzi, M., Röhrbein, F., Conradt, J., Richter, C.,  
*[Spiking Cooperative Stereo-Matching at 2 ms Latency with Neuromorphic Hardware](https://doi.org/10.1007/978-3-319-63537-8_11)*,  
Conf. Biomimetic and Biohybrid Systems. Living Machines 2017: Biomimetic and Biohybrid Systems, pp. 119-137. Lecture Notes in Computer Science, vol 10384. Springer, Cham.  [PDF](https://www.researchgate.net/publication/318449954_Spiking_Cooperative_Stereo-Matching_at_2_ms_Latency_with_Neuromorphic_Hardware),  [Videos](https://figshare.com/s/0d9fb146149b832ed8ec)
- <a name="Eibensteiner17radio"></a>Eibensteiner, F., Brachtendorf, H. G., Scharinger, J.,  
*[Event-driven stereo vision algorithm based on silicon retina sensors](http://doi.org/10.1109/RADIOELEK.2017.7937602)*,  
27th Int. Conf. Radioelektronika, Brno, 2017, pp. 1-6.
- <a name="Zou17bmvc"></a>Zou, D., Shi, F., Liu, W., Li, J., Wang, Q., Park P.-K.J., Hyunsurk, E. R.,  
*Robust Dense Depth Maps Generations from Sparse DVS Stereos*,  
British Machine Vision Conf. (BMVC), London, 2017. [PDF](https://www.dropbox.com/s/ee6dn8zy4odpfwl/0096.pdf?dl=1), [Supp. Material](https://www.dropbox.com/s/eztqo109iue6ned/Active%20Papers%20Paper%2096%20%20Supplementary%20File.zip?dl=1).

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
IEEE Trans. Neural Netw. Learn. Syst. (2014), 25(2):407-417.
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
IEEE Int. Conf. Robotics and Biomimetics (ROBIO), Zhuhai, China, 2015, pp. 1858-1863.
- <a name="Brosch15fnins"></a>Brosch, T., Tschechne, S., Neumann, H.,  
*[On event-based optical flow detection](https://doi.org/10.3389/fnins.2015.00137)*,  
Front. Neurosci. (2015), 9:137.
- <a name="Kosiorek15techrep"></a>Kosiorek, A., Adrian, D., Rausch, J., Conradt, J.,  
*[An Efficient Event-Based Optical Flow Implementation in C/C++ and CUDA](https://www.nst.ei.tum.de/fileadmin/w00bqs/www/publications/pp/2015SS-PP-RealTimeDVSOpticFlow.pdf),*  
Tech. Rep. TU Munich, 2015.
- <a name="Mueggler15icra"></a>E. Mueggler, C. Forster, N. Baumli, G. Gallego, D. Scaramuzza,  
*[Lifetime Estimation of Events from Dynamic Vision Sensors](http://dx.doi.org/10.1109/ICRA.2015.7139876)*,  
IEEE Int. Conf. Robotics and Automation (ICRA), Seattle (WA), USA, 2015, pp. 4874-4881. [PDF](http://rpg.ifi.uzh.ch/docs/ICRA15_Mueggler.pdf), [Code](https://www.github.com/uzh-rpg/rpg_event_lifetime)
- <a name="Rueckauer16fnins"></a>Rueckauer, B. and Delbruck, T.,  
*[Evaluation of Event-Based Algorithms for Optical Flow with Ground-Truth from Inertial Measurement Sensor](https://doi.org/10.3389/fnins.2016.00176),*  
Front. Neurosci (2016). 10:176.
    - [Code (jAER)](https://sourceforge.net/p/jaer/code/HEAD/tree/jAER/trunk/src/ch/unizh/ini/jaer/projects/rbodo/opticalflow/)
- <a name="Bardow16cvpr"></a>Bardow, P. A., Davison, A. J., Leutenegger, S.,  
*[Simultaneous Optical Flow and Intensity Estimation from an Event Camera](http://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Bardow_Simultaneous_Optical_Flow_CVPR_2016_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), Las Vegas, USA, 2016. [YouTube](https://youtu.be/1zqJpiheaaI)
- <a name="Liu17iscas"></a>Liu, M., Delbruck, T.,  
*[Block-Matching Optical Flow for Dynamic Vision Sensors: Algorithm and FPGA Implementation](https://arxiv.org/pdf/1706.05415.pdf)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), Baltimore, MD, 2017.


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
    IEEE Int. Symp. Circuits and Systems (ISCAS), Lisbon, 2015, pp. 2061-2064.
- <a name="Kim14bmvc"></a>Kim, H., Handa, A., Benosman, R., Ieng, S.-H., Davison, A. J.,  
*[Simultaneous Mosaicing and Tracking with an Event Camera](http://www.bmva.org/bmvc/2014/papers/paper066/)*, 
British Machine Vision Conference, 2014. [PDF](http://www.bmva.org/bmvc/2014/files/paper066.pdf), [YouTube](https://youtu.be/l6qxeM1DbXU).
    - [Code for intensity reconstruction](https://github.com/uzh-rpg/rpg_image_reconstruction_from_events).
- <a name="Barua16wacv"></a>Barua, S., Miyatani, Y., Veeraraghavan, A.,  
*[Direct face detection and video reconstruction from event cameras](http://doi.org/10.1109/WACV.2016.7477561)*,  
IEEE Winter Conf. Applications of Computer Vision (WACV), Lake Placid, NY, 2016, pp. 1-9. [YouTube](https://youtu.be/yGDVlN-L1TU)
- [Bardow et. al. CVPR 2016](#Bardow16cvpr),  
*Simultaneous Optical Flow and Intensity Estimation from an Event Camera*.
- <a name="Reinbacher16bmvc"></a>Reinbacher, C., Graber, G., Pock, T.,  
*[Real-Time Intensity-Image Reconstruction for Event Cameras Using Manifold Regularisation](http://www.bmva.org/bmvc/2016/papers/paper009/)*,  
British Machine Vision Conf. (BMVC), York, 2016. [PDF](http://www.bmva.org/bmvc/2016/papers/paper009/paper009.pdf), [YouTube](https://youtu.be/rvB2URrGT94), [Code](https://github.com/VLOGroup/dvs-reconstruction)
- <a name="Moeys17iscas"></a>Moeys, D. P., Li, C., Martel, J. N. P., Bamford, S., Longinotti, L., Motsnyi, V., Bello, D. S. S., Delbruck, T.,  
*Color Temporal Contrast Sensitivity in Dynamic Vision Sensors*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), Baltimore, MD, 2017. [PDF](http://www.ini.uzh.ch/admin/extras/doc_get.php?id=65634).


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
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Tokyo, 2013. [PDF](http://rpg.ifi.uzh.ch/docs/IROS13_Censi.pdf), [Slides](http://rpg.ifi.uzh.ch/docs/IROS13_Censi.ppt)
- <a name="Mueggler14iros"></a>Mueggler, E., Huber, B., Scaramuzza, D.,  
*[Event-based, 6-DOF Pose Tracking for High-Speed Maneuvers](https://doi.org/10.1109/IROS.2014.6942940)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Chicago, IL, 2014, pp. 2761-2768. [PDF](http://rpg.ifi.uzh.ch/docs/IROS14_Mueggler.pdf), [YouTube](https://youtu.be/LauQ6LWTkxM)
- <a name="Gallego15arxiv"></a>Gallego, G., Forster, C., Mueggler, E., Scaramuzza, D.,  
*[Event-based Camera Pose Tracking using a Generative Event Model](https://arxiv.org/pdf/1510.01972v1)*,  
arXiv:1510.01972, 2015.
- <a name="Mueggler15rss"></a>Mueggler, E., Gallego G., Scaramuzza, D.,   
*[Continuous-Time Trajectory Estimation for Event-based Vision Sensors](http://dx.doi.org/10.15607/RSS.2015.XI.036)*,  
Robotics: Science and Systems XI (RSS), Rome, Italy, 2015. [PDF]
- <a name="Gallego16arxiv"></a>Gallego, G., Lund, J.E.A., Mueggler, E., Rebecq, H., Delbruck, T., Scaramuzza, D.,  
*[Event-based, 6-DOF Camera Tracking for High-Speed Applications](https://arxiv.org/pdf/1607.03468.pdf)*,  
(Under review), 2016. [YouTube](https://youtu.be/iZZ77F-hwzs)
- <a name="Reinbacher17iccp"></a>Reinbacher, C., Munda, G., Pock, T.,  
*[Real-Time Panoramic Tracking for Event Cameras](https://doi.org/10.1109/ICCPHOT.2017.7951488)*,  
IEEE Int. Conf. Computational Photography (ICCP), Stanford, CA, USA, 2017, pp. 1-9. [PDF](https://arxiv.org/abs/1703.05161), [YouTube](https://youtu.be/Qy0brSlirmk), [Code](https://github.com/VLOGroup/dvs-panotracking)
- [Mueggler et. al. IJRR 2017](#Mueggler17ijrr).  
*The Event-Camera Dataset and Simulator: Event-based Data for Pose Estimation, Visual Odometry, and SLAM.*
- <a name="Vasco17icar"></a>Vasco, V., Glover, A., Mueggler, E., Scaramuzza, D., Natale, L., Bartolozzi, C.  
*[Independent Motion Detection with Event-driven Cameras](http://doi.org/10.1109/ICAR.2017.8023661)*,  
Int. Conf. Advanced Robotics (ICAR), Hong Kong, China, 2017, pp. 530-536. [PDF](https://arxiv.org/pdf/1706.08713v2.pdf)
- <a name="Nguyen17arxiv"></a> Nguyen, A., Do, T.-T., Caldwell, D. G., Tsagarakis, N. G.,  
*[Real-Time Pose Estimation for Event Cameras with Stacked Spatial LSTM Networks](https://arxiv.org/abs/1708.09011)*,  
arXiv 1708.09011.

<a name="VOSLAM"></a>
## Visual Odometry and SLAM (Simultaneous Localization And Mapping)
- <a name="Weikersdorfer13icvs"></a>Weikersdorfer, D., Hoffmann, R., Conradt. J.,  
*[Simultaneous localization and mapping for event-based vision systems](http://doi.org/10.1007/978-3-642-39402-7_14)*.  
Int. Conf. Computer Vision Systems (ICVS), 2013, pp. 133-142. [PDF](https://mediatum.ub.tum.de/doc/1191908/271955.pdf), [Slides](http://workshops.acin.tuwien.ac.at/ICVS/downloads/ICVS2013-ebslam_weikersdorfer.pdf)
- <a name="Censi14icra"></a>Censi, A. and Scaramuzza, D.,  
*[Low-latency Event-based Visual Odometry](https://doi.org/10.1109/ICRA.2014.6906931)*,  
IEEE Int. Conf. Robotics and Automation (ICRA), Hong-Kong, 2014, pp. 703-710. [PDF](http://rpg.ifi.uzh.ch/docs/ICRA14_Censi.pdf), [Slides](https://censi.science/pub/research/2013-dvsd/201405-icra15-dvsd.pdf)
- <a name="Weikersdorfer14icra"></a>Weikersdorfer, D., Adrian, D. B., Cremers, D., Conradt, J.,  
*[Event-based 3D SLAM with a depth-augmented dynamic vision sensor](https://doi.org/10.1109/ICRA.2014.6906882)*,  
IEEE Int. Conf. Robotics and Automation (ICRA), Hong-Kong, 2014, pp. 359-364.
- [Weikersdorfer, Ph.D. Thesis, 2014](#Weikersdorfer14PhD),  
*Efficiency by Sparsity: Depth-Adaptive Superpixels and Event-based SLAM*.
- <a name="Kueng16iros"></a>Kueng, B., Mueggler, E., Gallego, G., Scaramuzza, D.,  
*[Low-Latency Visual Odometry using Event-based Feature Tracks](https://doi.org/10.1109/IROS.2016.7758089)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Daejeon, South Korea, 2016, pp. 16-23. [PDF](http://rpg.ifi.uzh.ch/docs/IROS16_Kueng.pdf). [YouTube](https://youtu.be/RDu5eldW8i8)
- <a name="Kim16eccv"></a>Kim, H., Leutenegger, S., Davison, A.J.,  
*[Real-Time 3D Reconstruction and 6-DoF Tracking with an Event Camera](http://doi.org/10.1007/978-3-319-46466-4_21)*,  
European Conference on Computer Vision (ECCV), 2016, pp. 349-364. [PDF](https://www.doc.ic.ac.uk/~ajd/Publications/kim_etal_eccv2016.pdf), [YouTube](https://youtu.be/yHLyhdMSw7w)
- <a name="Rebecq17ral"></a>Rebecq, H., Horstschaefer, T., Gallego, G., Scaramuzza, D.,  
*[EVO: A Geometric Approach to Event-based 6-DOF Parallel Tracking and Mapping in Real-time](https://doi.org/10.1109/LRA.2016.2645143)*,  
IEEE Robotics and Automation Letters (RA-L), 2:2(593-600), 2017. [PDF](http://rpg.ifi.uzh.ch/docs/RAL16_EVO.pdf), [Youtube](https://youtu.be/bYqD2qZJlxE).
- <a name="Gallego17ral"></a>Gallego, G. and Scaramuzza, D.,  
*[Accurate Angular Velocity Estimation with an Event Camera](https://doi.org/10.1109/LRA.2016.2647639)*,  
IEEE Robotics and Automation Letters (RA-L), 2:2(632-639), 2017.
[PDF](http://rpg.ifi.uzh.ch/docs/RAL16_Gallego.pdf), [Youtube](https://youtu.be/v1sXWoOAs_0).
- [Mueggler et. al. IJRR 2017](#Mueggler17ijrr).  
*The Event-Camera Dataset and Simulator: Event-based Data for Pose Estimation, Visual Odometry, and SLAM.*

<a name="visual-inertial"></a>
## Visual-Inertial State Estimation
- <a name="Mueggler17arxiv"></a>Mueggler, E., Gallego, G., Rebecq, H., Scaramuzza, D.,  
*[Continuous-Time Visual-Inertial Trajectory Estimation with Event Cameras](https://arxiv.org/pdf/1702.07389.pdf)*,  
(Under review), 2017.
- [Mueggler et. al. IJRR 2017](#Mueggler17ijrr).  
*The Event-Camera Dataset and Simulator: Event-based Data for Pose Estimation, Visual Odometry, and SLAM.*
- <a name="Zhu17cvpr"></a>Zhu, A., Atanasov, N., Daniilidis, K.,  
*Event-based Visual Inertial Odometry*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR) 2017. [PDF](http://openaccess.thecvf.com/content_cvpr_2017/papers/Zhu_Event-Based_Visual_Inertial_CVPR_2017_paper.pdf), [Supplementary material](http://openaccess.thecvf.com/content_cvpr_2017/supplemental/Zhu_Event-Based_Visual_Inertial_2017_CVPR_supplemental.zip)
- <a name="Rebecq17bmvc"></a>Rebecq, H., Horstschaefer, T., Scaramuzza, D.,  
*Real-time Visual-Inertial Odometry for Event Cameras using Keyframe-based Nonlinear Optimization*,  
British Machine Vision Conf. (BMVC), London, 2017. [PDF](http://rpg.ifi.uzh.ch/docs/BMVC17_Rebecq.pdf), [Appendix](http://rpg.ifi.uzh.ch/docs/BMVC17_Rebecq_appendix.pdf), [YouTube](https://youtu.be/F3OFzsaPtvI)
- <a name="Rosinol17arxiv"></a>Rosinol Vidal, A., Rebecq, H., Horstschaefer, T., Scaramuzza, D.,  
*Hybrid, Frame and Event based Visual Inertial Odometry for Robust, Autonomous Navigation of Quadrotors*,  
Under Review, 2017. [PDF](https://arxiv.org/pdf/1709.06310), [YouTube](https://youtu.be/jIvJuWdmemE)

<a name="visual-stabilization"></a>
## Visual Stabilization
- <a name="Delbruck14iscas"></a>Delbruck, T., Villanueva, V., Longinotti, L.,  
*[Integration of dynamic vision sensor with inertial measurement unit for electronically stabilized event-based vision](http://doi.org/10.1109/ISCAS.2014.6865714)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS) 2014, 2636-2639. [YouTube](https://youtu.be/Tzy4WF6Qp-Y)

<a name="video-processing"></a>
## Video Processing
- <a name="Brandli14iscas"></a>Brandli, C., Muller, L., Delbruck, T.,  
*[Real-time, high-speed video decompression using a frame- and event-based DAVIS sensor](https://doi.org/10.1109/ISCAS.2014.6865228)*,  
IEEE Int. Symp. on Circuits and Systems (ISCAS), Melbourne VIC, 2014, pp. 686-689.


<a name="pattern-recognition"></a>
## Pattern Recognition
- <a name="Lee12iscas"></a>Lee, J., Delbruck, T., Park, P. K. J., Pfeiffer, M., Shin, C. W., Ryu, H., Kang, B. C.,  
*[Live demonstration: Gesture-Based remote control using stereo pair of dynamic vision sensors](https://doi.org/10.1109/ISCAS.2012.6272144)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS) 2012, Seoul, South Korea, pp. 736-740. [PDF](http://www.zora.uzh.ch/75315/1/Lee_et_al_Live_demonstration.pdf), [YouTube](https://youtu.be/IlKimfJN21A)
- [Barua et. al. WACV 2016](#Barua16wacv). Face recognition.
- <a name="Orchard15tpami"></a>Orchard, G., Meyer, C., Etienne-Cummings, R., Posch, C., Thakor, N., Benosman, R.,  
*[HFIRST: A Temporal Approach to Object Recognition](https://doi.org/10.1109/TPAMI.2015.2392947)*,  
IEEE Trans. Pattern Anal. Machine Intell. (TPAMI), 2015, 37(10):2028-2040. [PDF](https://arxiv.org/pdf/1508.01176.pdf)
    - [Code](http://www.garrickorchard.com/code/hfirst): HFIRST: A simple spiking neural network for recognition based on the canonical frame-based HMAX model.
- <a name="Moeys16ebccsp"></a>Moeys, D., Corradi F., Kerr, E., Vance, P., Das, G., Neil, D., Kerr, D., Delbruck, T.,  
*[Steering a Predator Robot using a Mixed Frame/Event-Driven Convolutional Neural Network](https://doi.org/10.1109/EBCCSP.2016.7605233)*,  
IEEE Int. Conf. Event-Based Control Comm. and Signal Proc. (EBCCSP), Krakow, Poland, 2016. [PDF](https://arxiv.org/pdf/1606.09433.pdf), [YouTube 1](https://youtu.be/fL3YCIPxuhM), [YouTube 2](https://youtu.be/lPF3Youpmqk)
- <a name="Lagorce17tpami"></a>Lagorce, X., Orchard, G., Gallupi, F., Shi, B., Benosman, R.,  
*[HOTS: A Hierarchy Of event-based Time-Surfaces for pattern recognition](https://doi.org/10.1109/TPAMI.2016.2574707)*,  
IEEE Trans. Pattern Anal. Machine Intell. (TPAMI), 2017, 39(7):1346-1359.
- [Clady et. al. FNINS](#Clady17fnins),  
*A Motion-Based Feature for Event-Based Pattern Recognition*.
- <a name="Lungu17iscas"></a>Lungu, I.-A., Corradi, F., Delbruck, T.,  
*Live Demonstration: Convolutional Neural Network Driven by Dynamic Vision Sensor Playing RoShamBo*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), Baltimore, MD, 2017. [YouTube](https://youtu.be/q5ua91n13TA), [Slides 36-39](http://rpg.ifi.uzh.ch/docs/ICRA17workshop/Delbruck.pdf)
- <a name="Amir17cvpr"></a>Amir, A., Taba, B., Berg, D., Melano, T., McKinstry, J., Di Nolfo, C., Nayak, T., Andreopoulos, A., Garreau, G., Mendoza, M., Kusnitz, J., Debole, M., Esser, S., Delbruck, T., Flickner, M., Modha, D.,  
*A Low Power, Fully Event-Based Gesture Recognition System*,  
 IEEE Conf. Computer Vision and Pattern Recognition (CVPR) 2017. [PDF](http://openaccess.thecvf.com/content_cvpr_2017/papers/Amir_A_Low_Power_CVPR_2017_paper.pdf).  
  - [YouTube: IBM Research demonstrates event-based gesture recognition using a brain-inspired chip](https://youtu.be/g08IW-qRomM)

<a name="control"></a>
## Control
- <a name="Delbruck07iscas"></a>Delbruck, T. and Lichtsteiner, P.,  
*[Fast sensory motor control based on event-based hybrid neuromorphic-procedural system](https://doi.org/10.1109/ISCAS.2007.378038)*,  
IEEE Int. Symp. Circuits and Systems, New Orleans, LA, 2007, pp. 845-848.
- <a name="Conradt09iscas"></a>Conradt, J., Cook, M., Berner, R., Lichtsteiner, P., Douglas, R. J., Delbruck, T.,  
*[A Pencil Balancing Robot Using a Pair of AER Dynamic Vision Sensors](https://doi.org/10.1109/ISCAS.2009.5117867)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS) 2009, pp. 781-784, 2009. [PDF](https://www.ini.uzh.ch/~conradt/publications/ISCAS2009-JConradt.pdf), [Poster](https://www.ini.uzh.ch/~conradt/publications/NIPS2008-JConradt.pdf), [Project page](https://www.ini.uzh.ch/~conradt/projects/PencilBalancer/), [YouTube 1](https://youtu.be/XVR5wEYkEGk), [YouTube 2](https://youtu.be/f9UngTdngY4), [YouTube 3](https://youtu.be/yCOnDc5r7p8)
- <a name="Conradt09iccvw"></a>Conradt, J., Berner, R., Cook, M., Delbruck, T.,  
*[An embedded AER dynamic vision sensor for low-latency pole balancing](https://doi.org/10.1109/ICCVW.2009.5457625)*,  
IEEE Int. Conf. Computer Vision Workshops (ICCVW), Kyoto, Japan, 2009. [PDF](http://www.ini.uzh.ch/admin/extras/doc_get.php?id=42580)
- <a name="Delbruck13fnins"></a>Delbruck, T. and Lang, M.,  
*[Robotic Goalie with 3ms Reaction Time at 4% CPU Load Using Event-Based Dynamic Vision Sensor](https://doi.org/10.3389/fnins.2013.00223)*,  
Front. Neurosci. (2013) 7:223. [PDF](http://www.zora.uzh.ch/107801/1/fnins-07-00223.pdf), [YouTube](https://youtu.be/IC5x7ftJ96w)
- <a name="Censi15acc"></a>Censi, A.,  
*[Efficient Neuromorphic Optomotor Heading Regulation](https://doi.org/10.1109/ACC.2015.7171931)*,  
American Control Conference (ACC), Chicago, IL, 2015, pp. 3854-3861.
- <a name="Mueggler15ecmr"></a>Mueggler, E., Baumli, N., Fontana, F., Scaramuzza, D.,  
*[Towards Evasive Maneuvers with Quadrotors using Dynamic Vision Sensors](https://doi.org/10.1109/ECMR.2015.7324048)*,  
Eur. Conf. Mobile Robots (ECMR), Lincoln, 2015. [PDF](http://rpg.ifi.uzh.ch/docs/ECMR15_Mueggler.pdf)
- <a name="Delbruck15iscas"></a>Delbruck, T., Pfeiffer, M., Juston, R., Orchard, G., Mueggler, E., Linares-Barranco, A., Tilden, M. W.,  
*[Human vs. computer slot car racing using an event and frame-based DAVIS vision sensor](https://doi.org/10.1109/ISCAS.2015.7169170)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), Lisbon, 2015, pp. 2409-2412. [YouTube 1](https://youtu.be/CnGPGiZuFRI), [YouTube 2](https://youtu.be/ALneVn-Ls2Q)
- [Moeys et. al. EBCCSP 2016](#Moeys16ebccsp).  *VISUALISE Predator/Prey Dataset*.
- <a name="Vasco16humanoids"></a>Vasco, V., Glover, A., Tirupachuri, Y., Solari, F., Chessa M., Bartolozzi C.,  
*[Vergence control with a neuromorphic iCub](https://doi.org/10.1109/HUMANOIDS.2016.7803355)*,  
IEEE Int. Conf. Humanoid Robotics (Humanoids), Cancun, Mexico, 2016, pp. 732-738.

<br><br>
<a name="datasets"></a>
# Datasets and Simulators (sorted by topic)
- [Several datasets from the Sensors group at INI](http://sensors.ini.uzh.ch/databases.html) (Institute of Neuroinformatics), Zurich:
    - [DVS128 Dynamic Vision Sensor Silicon Retina data](https://sourceforge.net/p/jaer/wiki/AER%20data/)
    
### Optical Flow
- [DVS/DAVIS Optical Flow Dataset](https://docs.google.com/document/d/1r9sRYANGuDTUcfSSq-sL4sd79SfjHGNRul_10uztDaI/pub) associated to the paper [Rueckauer and Delbruck, FNINS 2016](#Rueckauer16fnins).
- [Binas et. al. ICML 2017](#Binas17icml). *DDD17: End-To-End DAVIS Driving Dataset*.

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

### Recognition
- <a name="Orchard15fnins"></a>Orchard, G., Jayawant, A., Cohen, G.K., Thakor, N.,  
*[Converting Static Image Datasets to Spiking Neuromorphic Datasets Using Saccades](https://doi.org/10.3389/fnins.2015.00437),*  
Front. Neurosci. (2015), 9:437. [YouTube](https://youtu.be/2RBKNhxHvdw)
    - [Neuromorphic-MNIST (N-MNIST) dataset](http://www.garrickorchard.com/datasets/n-mnist) is a spiking version of the original frame-based MNIST dataset (of handwritten digits). [YouTube](https://youtu.be/6qK97qM5aB4)
    - [The Neuromorphic-Caltech101 (N-Caltech101) dataset](http://www.garrickorchard.com/datasets/n-caltech101) is a spiking version of the original frame-based Caltech101 dataset. [YouTube](https://youtu.be/dxit9Ce5f_E)
- [VISUALISE Predator/Prey Dataset](https://www.dropbox.com/sh/x6nm6zl9rrd7yzn/AAB_Fa5F-Y4fSo1nrIJxc8Xoa?dl=0) associated to the paper [Moeys et. al. EBCCSP 2016](#Moeys16ebccsp)
- <a name="Hu16fnins"></a>Hu, Y., Liu, H., Pfeiffer, M., Delbruck, T.,  
*[DVS Benchmark Datasets for Object Tracking, Action Recognition, and Object Recognition](https://doi.org/10.3389/fnins.2016.00405),*  
Front. Neurosci. (2016) 10:405. [Dataset](http://dgyblog.com/projects-term/dvs-dataset.html)
- <a name="Liu16fnins">Liu, Q., Pineda-García, G., Stromatias, E., Serrano-Gotarredona, T., Furber, SB.,  
*[Benchmarking Spike-Based Visual Recognition: A Dataset and Evaluation](https://doi.org/10.3389/fnins.2016.00496)*,  
Front. Neurosci. (2016) 10:496. [Dataset](https://github.com/qian-liu/benchmarking), [Dataset](https://github.com/NEvision/NE15)


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


<br><br>
<a name="processors-platforms"></a>
# Neuromorphic Processors and Platforms
- [Dynamic Neuromorphic Asynchronous Processor (DYNAP) by iniLabs](https://inilabs.com/products/dynap/)
  - <a name="Qiao15fnins"></a>Qiao, N., Mostafa, H., Corradi, F., Osswald, M., Stefanini, F., Sumislawska, D., Indiveri, G.,  
  *[A reconfigurable on-line learning spiking neuromorphic processor comprising 256 neurons and 128K synapses](https://doi.org/10.3389/fnins.2015.00141),*  
  Front. Neurosci. (2015) 9:141. [PDF](https://capocaccia.ethz.ch/capo/raw-attachment/wiki/2015/hybrid15/frontiers14-nlp.pdf)
  - <a name="Indiveri15iedm"></a>Indiveri, G., Qiao, N., Corradi, F.,  
  *[Neuromorphic Architectures for Spiking	 Deep Neural Networks](https://doi.org/10.1109/IEDM.2015.7409623)*,  
  IEEE Int. Electron Devices Meeting (IEDM), Washington, DC, 2015, pp. 4.2.1-4.2.4. [PDF](http://ncs.ethz.ch/pubs/pdf/Indiveri_etal15.pdf)
- <a name="Wiesmann12cvprw"></a>Wiesmann, G., Schraml, S., Litzenberger, M., Belbachir, A. N., Hofstatter, M., Bartolozzi, C.,  
*[Event-driven embodied system for feature extraction and object recognition in robotic applications](https://doi.org/10.1109/CVPRW.2012.6238898),*  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), Providence, RI, 2012, pp. 76-82.
- <a name="Galluppi14icra"></a>Galluppi, F., Denk, C., Meiner, M. C., Stewart, T. C., Plana, L. A., Eliasmith, C., Furber, S., Conradt, J.,  
*[Event-based neural computing on an autonomous mobile platform](https://doi.org/10.1109/ICRA.2014.6907270),*  
IEEE Int. Conf. Robotics and Automation (ICRA), Hong Kong, 2014, pp. 2862-2867. [PDF](http://compneuro.uwaterloo.ca/files/publications/galluppi.2014.pdf)


<br><br>
<a name="workshops"></a>
# Workshops and Tutorials
- [ICRA 2015 Workshop on Innovative Sensing for Robotics](http://innovative-sensing.mit.edu/), with a focus on Neuromorphic Sensors.
- [Event-Based Vision for High-Speed Robotics (slides)](http://www.rit.edu/kgcoe/iros15workshop/papers/IROS2015-WASRoP-Invited-04-slides.pdf) IROS 2015, Workshop on Alternative Sensing for Robot Perception.
- [ICRA 2017 First International Workshop on Event-based Vision](http://rpg.ifi.uzh.ch/ICRA17_event_vision_workshop.html).
- [The Telluride Neuromorphic Cognition Engineering Workshops](http://telluride.iniforum.ch/accounts/login/?next=/).
- [Capo Caccia Workshops toward Cognitive Neuromorphic Engineering](http://capocaccia.iniforum.ch/).


<br><br>
<a name="theses"></a>
# Theses and Dissertations
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
- See also [Theses from Delbruck's group at INI](https://www.ini.uzh.ch/~tobi/wiki/doku.php?id=publications#phd_thesis)


<br><br>
<a name="people"></a>
# People / Organizations
- [Institute of NeuroInformatics](https://www.ini.uzh.ch/) (INI)  of the University of Zurich (UZH) and ETH Zurich.
- [iniLabs](http://www.inilabs.com) (Comerzialization of neuromorphic technology from INI).
- [Dynamic Vision Sensor (DVS) - asynchronous temporal contrast silicon retina](http://siliconretina.ini.uzh.ch/wiki/index.php)
- [Robotics and Perception Group](http://rpg.ifi.uzh.ch/research_dvs.html) (RPG-UZH).

<br><br>
<a name="contributing"></a>
# Contributing
Please see [CONTRIBUTING](https://github.com/uzh-rpg/event-based_vision_resources/blob/master/Contributing.md) for details.
***
