# Event-based Vision Resources

## Table of Contents (sorted by topic):
- [Devices](#devices)
- [Neuromorphic Systems](#neuromorphic-systems)
- [Drivers](#drivers)
- [Calibration](#calibration)

- [Algorithms](#algorithms)
    - [Feature Detection and Tracking](#feature-detection)
    - [Depth Estimation (3D Reconstruction)](#depth-estimation)
    	- [Monocular](#depth-mono)
    	- [Stereo](#depth-stereo)
    - [Optical Flow Estimation](#optical-flow)
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
- [Neuromorphic Processors and Platforms](#processors-platforms)
- [Workshops](#workshops)
- [Tutorials](#tutorials)
- [People / Organizations](#people)
- [Contributing](#contributing)

___

<a name="devices"></a>
## Devices
- **DVS (Dynamic Vision Sensor)**: Lichtsteiner, P., Posch, C., and Delbruck, T., *[A 128x128 120dB 15μs latency asynchronous temporal contrast vision sensor](http://doi.org/10.1109/JSSC.2007.914337)*, IEEE J. Solid-State Circuits, 43(2):566-576, 2008.
    - [Product page at iniLabs](https://inilabs.com/products/dynamic-vision-sensors/)
    - [Introductory videos about the DVS](https://inilabs.com/videos/dvs-introduction/)
- **DAVIS (Dynamic and Active-Pixel Vision Sensor)** :
Brandli, C., Berner, R., Yang, M., Liu, S.-C., Delbruck, T., *[A 240x180 130 dB 3 µs Latency Global Shutter Spatiotemporal Vision Sensor](https://doi.org/10.1109/JSSC.2014.2342715)*, IEEE J. Solid-State Circuits, 49(10):2333-2341, 2014.
    - [Product page at iniLabs](https://inilabs.com/products/dynamic-and-active-pixel-vision-sensor/)
    - **Color-DAVIS**: Li, C., Brandli, C., Berner, R., Liu, H., Yang, M., Liu, S.-C., Delbruck, T., *[Design of an RGBW Color VGA Rolling and Global Shutter Dynamic and Active-Pixel Vision Sensor](https://doi.org/10.1109/ISCAS.2015.7168734)*, IEEE Int. Symp. Circuits and Systems (ISCAS), Lisbon, 2015, pp. 718-721.
- **ATIS (Asynchronous Time-based Image Sensor)**: Posch, C., Matolin, D., Wohlgenannt, R. (2011). *[A QVGA 143 dB Dynamic Range Frame-Free PWM Image Sensor With Lossless Pixel-Level Video Compression and Time-Domain CDS](http://doi.org/10.1109/JSSC.2010.2085952)*, IEEE J. Solid-State Circuits, 46(1):259-275, 2011.
    - [Chronocam](http://www.chronocam.com/)
- Samsung's DVS (Gen2). [Yoel Yaffe](https://www.linkedin.com/in/yoel-yaffe-a606841/), Samsung Israel Research Center, Samsung Electronics.
- CeleX ([Hillhouse Technology](http://www.hillhouse-tech.com/), Singapore). [YouTube](https://youtu.be/Wlzc-5sgm1g)
- [Insightness AG](http://www.insightness.com/). [The Silicon Eye](http://www.insightness.com/?p=361) Technology


<a name="neuromorphic-systems"></a>
## Neuromorphic Systems
- Delbruck, T., [Frame-free dynamic digital vision]()*, Int. Symp. Secure-Life Electronics, Advanced Electronics for Quality Life and Society, University of Tokyo, Tokyo, Japan, Mar. 6-7, 2008, pp. 21-26. Introduces the software architecture of jAER and shows examples of several event-based processing algorithms.
- Liu, S.-C. and Delbruck, T., *[Neuromorphic sensory systems](https://doi.org/10.1016/j.conb.2010.03.007)*, Current Opinion in Neurobiology, 20:3(288-295), 2010.
- Delbruck, T., *[Fun with asynchronous vision sensors and processing](https://www.ini.uzh.ch/~tobi/wiki/lib/exe/fetch.php?media=delbruck_funwithasynsensors_2012.pdf)*. Computer Vision - ECCV 2012. Workshops and Demonstrations. Springer Berlin/Heidelberg, 2012. A position paper and summary of recent accomplishments of the INI Sensors' group.
- Liu, S.-C., Delbruck, T., Indiveri, G., Whatley, A., Douglas, R., *[Event-Based Neuromorphic Systems](http://eu.wiley.com/WileyCDA/WileyTitle/productCd-1118927621.html)*, Wiley. ISBN: 978-1-118-92762-5, 2014.
- Delbruck, T., *[Neuromorophic Vision Sensing and Processing (Invited paper)](https://doi.org/10.1109/ESSDERC.2016.7599576)*, 46th Eur. Solid-State Device Research Conference (ESSDERC), Lausanne, 2016, pp. 7-14.


<a name="drivers"></a>
## Drivers
- [jAER (java Address-Event Representation) project](http://jaerproject.org/)
- [caer (AER event-based framework, written in C, targeting embedded systems)](https://github.com/inilabs/caer)
- [libcaer (Minimal C library to access, configure and get/send AER data from sensors or to/from neuromorphic processors)](https://github.com/inilabs/libcaer)
- [ROS (Robotic Operating System)](https://github.com/uzh-rpg/rpg_dvs_ros)


<a name="calibration"></a>
## Calibration
- [Focus adjustment](https://github.com/uzh-rpg/rpg_dvs_ros/tree/master/dvs_calibration#focus-adjustment) or [this other source](https://github.com/ethz-asl/kalibr/wiki/calibrating-the-vi-sensor#2-setting-the-focus).
- For the DAVIS: use the grayscale frames to calibrate the optics of both frames and events.
    - ROS camera calibrator ([monocular](http://wiki.ros.org/camera_calibration/Tutorials/MonocularCalibration) or [stereo](http://wiki.ros.org/camera_calibration/Tutorials/StereoCalibration))
     - [kalibr software](https://github.com/ethz-asl/kalibr/wiki/multiple-camera-calibration) by ASL - ETH.
- For the DAVIS camera and IMU calibration: [kalibr software](https://github.com/ethz-asl/kalibr/wiki/camera-imu-calibration) by ASL - ETH, using the grayscale frames.
- For the DVS (events-only):
    - [Calibration using blinking LEDs or computer screens](https://github.com/uzh-rpg/rpg_dvs_ros/tree/master/dvs_calibration) by RPG - UZH.
    - [DVS camera calibration](https://github.com/gorchard/DVScalibration) by G. Orchard.
    - [DVS camera calibration](https://github.com/VLOGroup/dvs-calibration) by VLOGroup at TU Graz.


<a name="algorithms"></a>
# Algorithms

<a name="feature-detection"></a>
## Feature Detection and Tracking
- Litzenberger, M., Posch, C., Bauer, D., Belbachir, A. N., Schon. P., Kohn, B., Garn, H., *[Embedded Vision System for Real-Time Object Tracking using an Asynchronous Transient Vision Sensor](https://doi.org/10.1109/DSPWS.2006.265448)*, IEEE 12th Digital Signal Proc. Workshop and 4th IEEE Signal Proc. Education Workshop, Teton National Park, WY, 2006, pp. 173-178.
- Litzenberger, M., Kohn, B., Belbachir, A.N., Donath, N., Gritsch, G., Garn, H., Posch, C., Schraml, S., *[Estimation of Vehicle Speed Based on Asynchronous Data from a Silicon Retina Optical Sensor](https://doi.org/10.1109/ITSC.2006.1706816)*, IEEE Intelligent Transportation Systems Conf., Toronto, Ont., 2006, pp. 653-658. [PDF](http://belbachir.info/PDF/itsc2006.pdf)
- Drazen, D., Lichtsteiner, P., Haefliger, P., Delbruck, T., Jensen, A., *[Toward real-time particle tracking using an event-based dynamic vision sensor](https://doi.org/10.1007/s00348-011-1207-y)*, Experiments in Fluids (2011), 51:1465-1469. [PDF](http://www.zora.uzh.ch/60624/1/Drazen_EIF_2011.pdf)
- Ni, Z., Bolopion, A., Agnus, J., Benosman, R., Regnier, S., *[Asynchronous event-based visual shape tracking for stable haptic feedback in microrobotics](https://doi.org/10.1109/TRO.2012.2198930)*, IEEE Trans. Robot. (2012), 28(5):1081-1089.
- Piatkowska, E., Belbachir, A. N., Schraml, S., Gelautz, M., *[Spatiotemporal multiple persons tracking using Dynamic Vision Sensor](https://doi.org/10.1109/CVPRW.2012.6238892)*, IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), Providence, RI, 2012, pp. 35-40. [PDF](https://publik.tuwien.ac.at/files/PubDat_209369.pdf)
- Borer, D.,  Rosgen, T., *[Large-scale Particle Tracking with Dynamic Vision Sensors]()*, ISFV16 - 16th Int. Symp. Flow Visualization, Okinawa 2014. [Project page](http://www.ifd.mavt.ethz.ch/research/group-roesgen/dynamic-vision-sensors.html), [PDF](http://www.ifd.mavt.ethz.ch/content/dam/ethz/special-interest/mavt/fluid-dynamics/ifd-dam/research/documents/posters/experimental-methods/daniel_borer_dynamic_vision_sensor.pdf)
- Lagorce, X., Meyer, C., Ieng, S. H., Filliat, D., Benosman, R., *[Live demonstration: Neuromorphic event-based multi-kernel algorithm for high speed visual features tracking](https://doi.org/10.1109/BioCAS.2014.6981681)*, IEEE Biomedical Circuits and Systems Conference (BioCAS), Lausanne, 2014, pp. 178-178.
- Lagorce, X., Meyer, C., Ieng, S. H., Filliat, D., Benosman, R., *[Asynchronous Event-Based Multikernel Algorithm for High-Speed Visual Features Tracking](https://doi.org/10.1109/TNNLS.2014.2352401)*, IEEE Trans. Neural Netw. Learn. Syst. (2015), 26(8):1710-1720.
- Clady, X., Ieng, S.-H., Benosman, R., *[Asynchronous event-based corner detection and matching](https://doi.org/10.1016/j.neunet.2015.02.013)*, Neural Networks (2015), 66:91-106.
- Lagorce, X., Meyer, C., Ieng, S. H., Filliat, D., Benosman, R., *[Asynchronous Event-Based Multikernel Algorithm for High-Speed Visual Features Tracking](https://doi.org/10.1109/TNNLS.2014.2352401)*,  IEEE Trans. Neural Netw. Learn. Syst. (2015), 26(8):1710-1720.
- Ni, Z., Ieng, S. H., Posch, C., Regnier, S., Benosman, R., *[Visual Tracking Using Neuromorphic Asynchronous Event-Based Cameras](https://doi.org/10.1162/NECO_a_00720)*, Neural Computation (2015), 27(4):925-953.
- Barranco, F., Teo, C. L., Fermüller, C., Aloimonos, Y., *[Contour Detection and Characterization for Asynchronous Event Sensors](https://doi.org/10.1109/ICCV.2015.63)*, IEEE Int. Conf. Computer Vision (ICCV), 2015, Santiago, Chile, pp. 486-494. [PDF](http://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Barranco_Contour_Detection_and_ICCV_2015_paper.pdf)
- Liu, H., Moeys, D. P., Das, G., Neil, D., Liu, S.-C., Delbruck, T., *[Combined frame- and event-based detection and tracking](https://doi.org/10.1109/ISCAS.2016.7539103)*, IEEE Int. Symp. Circuits and Systems (ISCAS), Montreal, QC, 2016, pp. 2511-2514.
- Tedaldi, D., Gallego, G., Mueggler, E., Scaramuzza, D., *[Feature detection and tracking with the dynamic and active-pixel vision sensor (DAVIS)](https://doi.org/10.1109/EBCCSP.2016.7605086)*, IEEE Int. Conf. Event-Based Control Comm. and Signal Proc. (EBCCSP), Krakow, Poland, 2016. [PDF](http://rpg.ifi.uzh.ch/docs/EBCCSP16_Tedaldi.pdf), [YouTube](https://www.youtube.com/watch?v=nglfEkiK308)
- Braendli, C., Strubel, J., Keller, S., Scaramuzza, D., Delbruck, T., *[ELiSeD - An Event-Based Line Segment Detector](https://doi.org/10.1109/EBCCSP.2016.7605244)*, Int. Conf. on Event-Based Control Comm. and Signal Proc. (EBCCSP), Krakow, Poland, 2016. [PDF](http://rpg.ifi.uzh.ch/docs/EBCCSP16_Braendli.pdf)
- Zhu, A., Atanasov, N., Daniilidis, K., *[Event-based Feature Tracking with Probabilistic Data Associations](https://fling.seas.upenn.edu/~alexzhu/dynamic/event-based-feature-tracking-with-probabilistic-data-association/)*, IEEE Int. Conf. Robotics and Automation (ICRA), Singapore, 2017. [YouTube](https://youtu.be/m93XCqAS6Fc)


<a name="depth-estimation"></a>
## Depth Estimation (3D Reconstruction)

<a name="depth-mono"></a>
### Monocular Depth Estimation
- Rebecq, H., Gallego, G., Scaramuzza, D., *[EMVS: Event-based Multi-View Stereo](http://www.bmva.org/bmvc/2016/papers/paper063/)*, British Machine Vision Conference (BMVC), York, 2016. [PDF](http://rpg.ifi.uzh.ch/docs/BMVC16_Rebecq.pdf), [YouTube](https://www.youtube.com/watch?v=EUX3Tfx0KKE), [3D Reconstruction Experiments from a Train using an Event Camera](https://www.youtube.com/watch?v=fA4MiSzYHWA)

### Monocular Depth Estimation using Structured Light
- Brandli, C., Mantel, T.A., Hutter, M., Hoepflinger, M.A., Berner, R., Siegwart, R., Delbruck, T., *[Adaptive Pulsed Laser Line Extraction for Terrain Reconstruction using a Dynamic Vision Sensor](https://doi.org/10.3389/fnins.2013.00275)*, Front. Neurosci. (2014) 7:275. [PDF](http://www.zora.uzh.ch/107736/1/fnins-07-00275.pdf), [YouTube](https://youtu.be/20OGD5Wwe9Q)
- Matsuda, N., Cossairt, O., Gupta, M., *[MC3D: Motion Contrast 3D Scanning](https://doi.org/10.1109/ICCPHOT.2015.7168370)*, IEEE Conf. Computational Photography (ICCP), Houston,TX, 2015, pp. 1-10. [PDF](http://compphotolab.northwestern.edu/wordpress/wp-content/uploads/2015/04/dvs_031.pdf), [YouTube](https://youtu.be/m7qOEsTyVwU), [Project page](http://compphotolab.northwestern.edu/project/mc3d-motion-contrast-3d-laser-scanner/)


<a name="depth-stereo"></a>
### Stereo Depth Estimation
- Kogler, J., Sulzbachner, C., Kubinger, W., *[Bio-inspired stereo vision system with silicon retina imagers](https://doi.org/10.1007/978-3-642-04667-4_18)*, Int. Conf. Computer Vision Systems (ICVS), 2009, pp. 174-183. [PDF](http://adose-eu.org/documents/Paper/2009_10_13-15.pdf)
- Schraml, C., Schon, P., Milosevic, N., *[Smartcam for real-time stereo vision - address-event based embedded system](http://doi.org/10.5220/0002057604660471)*, Int. Conf. Computer Vision Theory and Applications (VISAPP), Barcelona, Spain, 2007, pp. 466-471.
- Schraml, S., Belbachir, A. N., Milosevic, N., Schon, P., *[Dynamic stereo vision system for real-time tracking](https://doi.org/10.1109/ISCAS.2010.5537289)*, IEEE Int. Symp. Circuits and Systems (ISCAS), Paris, 2010, pp. 1409-1412.
- Kogler, J., Sulzbachner, C., Humenberger, M., Eibensteiner, F., *[Address-Event Based Stereo Vision with Bio-Inspired Silicon Retina Imagers](http://doi.org/10.5772/12941)*, Advances in Theory and Applications of Stereo Vision (2011), pp. 165-188.
- Kogler, J., Humenberger, M., Sulzbachner, C., *[Event-Based Stereo Matching Approaches for Frameless Address Event Stereo Data](http://doi.org/10.1007/978-3-642-24028-7_62)*, Int. Symp. Visual Computing (ISVC) 2011, Advances in Visual Computing, pp. 674-685.
- Benosman, R., Ieng, S. H., Rogister, P., Posch, C., *[Asynchronous Event-Based Hebbian Epipolar Geometry](https://doi.org/10.1109/TNN.2011.2167239)*, IEEE Trans. Neural Netw. (2011), 22(11):1723-1734.
- [Lee et. al., ISCAS 2012](#Lee12iscas)
- Rogister, P. , Benosman, R., Ieng, S.-H., Lichtsteiner, P., Delbruck, T., *[Asynchronous Event-Based Binocular Stereo Matching](https://doi.org/10.1109/TNNLS.2011.2180025)*, IEEE Trans. Neural Netw. Learn. Syst., 23(2):347-353, 2012.
- Carneiro, J., Ieng, S.-H., Posch, C., Benosman, R., *[Event-based 3D reconstruction from neuromorphic retinas](https://doi.org/10.1016/j.neunet.2013.03.006)*, Neural Networks (2013), 45:27-38.
- Carneiro, J., *[Asynchronous Event-Based 3D Vision](http://www.theses.fr/2014PA066593.pdf)*, Ph.D. Thesis, Université de Pierre et Marie Curie - Institut de la Vision, Paris, France, 2014.
- Piatkowska, E., Belbachir, A. N., Gelautz, M., *[Asynchronous Stereo Vision for Event-Driven Dynamic Stereo Sensor Using an Adaptive Cooperative Approach](https://doi.org/10.1109/ICCVW.2013.13)*," IEEE Int. Conf. Computer Vision Workshops (ICCVW), Sydney, NSW, 2013, pp. 45-50.
- Piatkowska, E., Belbachir, A. N., Gelautz, M., *[Cooperative and asynchronous stereo vision for dynamic vision sensors](http://dx.doi.org/10.1088/0957-0233/25/5/055108)*, Meas. Sci. Technol. (2014), 25(5).
- Lee, J. H., Delbruck, T., Pfeiffer, M., Park, P. K. J., Shin, C.-W., Ryu, H., Kang, B. C., *[Real-Time Gesture Interface Based on Event-Driven Processing From Stereo Silicon Retinas](https://doi.org/10.1109/TNNLS.2014.2308551)*, IEEE Trans. Neural Netw. Learn. Syst. (2014), 25(2):2250-2263.
- Camuñas-Mesa, L. A., Serrano-Gotarredona, T., Ieng, S. H., Benosman, R. B., and Linares-Barranco, B., *[On the use of orientation filters for 3D reconstruction in event–driven stereo vision](https://doi.org/10.3389/fnins.2014.00048)*, Front. Neurosci. (2014) 8:48.
- Camuñas-Mesa, L. A., Serrano-Gotarredona, T., Linares-Barranco, B., Ieng, S., Benosman, R., *[Event-Driven Stereo Vision with Orientation Filters](https://doi.org/10.1109/ISCAS.2014.6865114)*, IEEE Int. Symp. Circuits and Systems (ISCAS), Melbourne VIC, 2014, pp. 257-260.
- Belbachir, A. N., Schraml, S., Mayerhofer, M., Hofstatter, M., *[A Novel HDR Depth Camera for Real-time 3D 360-degree Panoramic Vision](https://doi.org/10.1109/CVPRW.2014.69)*, IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2014, pp. 419-426. [PDF](http://www.cv-foundation.org/openaccess/content_cvpr_workshops_2014/W13/papers/Belbachir_A_Novel_HDR_2014_CVPR_paper.pdf)
- Eibensteiner, F., Kogler, J., Scharinger, J., *[A High-Performance Hardware Architecture for a Frameless Stereo Vision Algorithm Implemented on a FPGA Platform](https://doi.org/10.1109/CVPRW.2014.97)*, IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), Columbus, OH, 2014, pp. 637-644.
- Schraml, S., Belbachir, A. N., Bischof, H., *[Event-Driven Stereo Matching for Real-Time 3D Panoramic Vision](https://doi.org/10.1109/CVPR.2015.7298644)*, IEEE Conf. Computer Vision and Pattern Recognition (CVPR), Boston, MA, 2015, pp. 466-474. [PDF](http://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Schraml_Event-Driven_Stereo_Matching_2015_CVPR_paper.pdf). [Slides](https://www.anyline.io/wp-content/uploads/2016/03/event-driven-stereo-for-3d-360deg-panoramic-vision.pdf).
- S. Schraml, A. N. Belbachir and H. Bischof, *[An Event-Driven Stereo System for Real-Time 3-D 360° Panoramic Vision](https://doi.org/10.1109/TIE.2015.2477265)*, IEEE Trans. Ind. Electron. (2016), 63(1):418-428.
- Firouzi, M. and Conradt, J., *[Asynchronous Event-based Cooperative Stereo Matching Using Neuromorphic Silicon Retinas](http://doi.org/10.1007/s11063-015-9434-5)*. Neural Processing Letters, 2016, 43(2):311-326. [PDF](https://mediatum.ub.tum.de/doc/1254531/131347.pdf)
- Osswald, M., Ieng, S.-H., Benosman, R., Indiveri, G., *[A spiking neural network model of 3D perception for event-based neuromorphic stereo vision systems](http://doi.org/10.1038/srep40703)*, Scientific Reports 7, Article number: 40703 (2017).



<a name="optical-flow"></a>
## Optical Flow Estimation
- *[Cook et. al. IJCNN 2011](#Cook11ijcnn)*; in case of rotational motion.
- Benosman, R., Ieng, S.-H., Clercq, C., Bartolozzi, C., and Srinivasan, M., *[Asynchronous Frameless Event-Based Optical Flow](https://doi.org/10.1016/j.neunet.2011.11.001)*. Neural Networks (2012), 27:32-37.
- Benosman, R., Clercq, C., Lagorce, X., Ieng, S.-H., and Bartolozzi, C., *[Event-Based Visual Flow](https://doi.org/10.1109/TNNLS.2013.2273537)*. IEEE Trans. Neural Netw. Learn. Syst. (2014), 25(2):407-417.
    - [Code (jAER): LocalPlanesFlow](https://sourceforge.net/p/jaer/code/HEAD/tree/jAER/trunk/src/ch/unizh/ini/jaer/projects/rbodo/opticalflow/LocalPlanesFlow.java)
- Orchard, G., Thakor, N. V., Etienne-Cummings, R., *[Real-time motion estimation using spatiotemporal filtering in FPGA](https://doi.org/10.1109/BioCAS.2013.6679700)*, IEEE Biomedical Circuits and Systems Conf. (BioCAS), Rotterdam, 2013, pp. 306-309.
- Tschechne, S., Sailer R., Neumann, H., *[Bio-Inspired Optic Flow from Event-Based Neuromorphic Sensor Input](https://doi.org/10.1007/978-3-319-11656-3_16)*, IAPR Workshop on Artificial Neural Networks in Pattern Recognition (ANNPR) 2014, pp. 171-182.
- Barranco, F., Fermüller, C., Aloimonos, Y., *[Contour motion estimation for asynchronous event-driven cameras](https://doi.org/10.1109/JPROC.2014.2347207)*, Proc. IEEE (2014), 102(10):1537-1556. [PDF](http://www.cfar.umd.edu/~fer/postscript/contourmotion-dvs-final.pdf)
- Barranco, F., Fermüller, C., Aloimonos, Y., *[Bio-inspired Motion Estimation with Event-Driven Sensors](https://doi.org/10.1007/978-3-319-19258-1_27)*, Int. Work-Conf. Artificial Neural Networks (IWANN) 2015, Advances in Computational Intelligence, pp. 309-321.
- Conradt, J., *[On-Board Real-Time Optic-Flow for Miniature Event-Based Vision Sensors](https://doi.org/10.1109/ROBIO.2015.7419043)*, 2015 IEEE Int. Conf. Robotics and Biomimetics (ROBIO), Zhuhai, China, 2015, pp. 1858-1863.
- Brosch, T., Tschechne, S., Neumann, H., *[On event-based optical flow detection](https://doi.org/10.3389/fnins.2015.00137)*, Front. Neurosci. (2015), 9:137.
- Kosiorek, A., Adrian, D., Rausch, J., Conradt, J., *[An Efficient Event-Based Optical Flow Implementation in C/C++ and CUDA](https://www.nst.ei.tum.de/fileadmin/w00bqs/www/publications/pp/2015SS-PP-RealTimeDVSOpticFlow.pdf)*. Tech. Rep. TU Munich, 2015.
- E. Mueggler, C. Forster, N. Baumli, G. Gallego, D. Scaramuzza, *[Lifetime Estimation of Events from Dynamic Vision Sensors](http://dx.doi.org/10.1109/ICRA.2015.7139876)*, IEEE Int. Conf. Robotics and Automation (ICRA), Seattle (WA), USA, 2015, pp. 4874-4881. [PDF](http://rpg.ifi.uzh.ch/docs/ICRA15_Mueggler.pdf), [Code](https://www.github.com/uzh-rpg/rpg_event_lifetime)
- <a name="Rueckauer16fnins"></a>Rueckauer, B. and Delbruck, T., *[Evaluation of Event-Based Algorithms for Optical Flow with Ground-Truth from Inertial Measurement Sensor](https://doi.org/10.3389/fnins.2016.00176)*. Front. Neurosci (2016). 10:176.
    - [Code (jAER)](https://sourceforge.net/p/jaer/code/HEAD/tree/jAER/trunk/src/ch/unizh/ini/jaer/projects/rbodo/opticalflow/)
- <a name="Bardow16cvpr"></a>Bardow, P. A., Davison, A. J., Leutenegger, S., *[Simultaneous Optical Flow and Intensity Estimation](http://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Bardow_Simultaneous_Optical_Flow_CVPR_2016_paper.pdf)*, IEEE Conf. Computer Vision and Pattern Recognition (CVPR), Las Vegas, USA, 2016. [YouTube](https://youtu.be/1zqJpiheaaI)
- Liu, M., Delbruck, T., *[Block-Matching Optical Flow for Dynamic Vision Sensors: Algorithm and FPGA Implementation](https://arxiv.org/pdf/1706.05415.pdf)*, IEEE Int. Symp. Circuits and Systems (ISCAS), Baltimore, MD, 2017.


<a name="image-reconstruction"></a>
## Intensity-Image Reconstruction from events
- <a name="Cook11ijcnn"></a>Cook, M., Gugelmann, L., Jug, F., Krautz, C., Steger, A., *[Interacting maps for fast visual interpretation](https://doi.org/10.1109/IJCNN.2011.6033299)*, Int. Joint Conf. on Neural Networks (IJCNN), San Jose, CA, 2011, pp. 770-776. [YouTube](https://youtu.be/irX3Nd5U0hY)
  - Martel, J. N. P., Cook, M., *[A Framework of Relational Networks to Build Systems with Sensors able to Perform the Joint Approximate Inference of Quantities](https://doi.org/10.5167/uzh-121743)*, IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Workshop on Unconventional Computing for Bayesian Inference, 2015, Hamburg. [PDF](http://www.zora.uzh.ch/121743/1/RelationalNetSensor.pdf)
  - Martel, J. N. P., Chau, M., Dudek, P., Cook, M., *[Toward joint approximate inference of visual quantities on cellular processor arrays](https://doi.org/10.1109/ISCAS.2015.7169083)*, IEEE Int. Symp. Circuits and Systems (ISCAS), Lisbon, 2015, pp. 2061-2064.
- Kim, H., Handa, A., Benosman, R., Ieng, S.-H., Davison, A.J., *[Simultaneous Mosaicing and Tracking with an Event Camera](http://www.bmva.org/bmvc/2014/papers/paper066/)*, British Machine Vision Conference, 2014. [PDF](http://www.bmva.org/bmvc/2014/files/paper066.pdf), [YouTube](https://youtu.be/l6qxeM1DbXU).
    - [Code for intensity reconstruction](https://github.com/uzh-rpg/rpg_image_reconstruction_from_events).
- <a name="Barua16wacv"></a>Barua, S., Miyatani, Y., Veeraraghavan, A., *[Direct face detection and video reconstruction from event cameras](http://doi.org/10.1109/WACV.2016.7477561)*, IEEE Winter Conf. Applications of Computer Vision (WACV), Lake Placid, NY, 2016, pp. 1-9. [YouTube](https://youtu.be/yGDVlN-L1TU)
- *[Bardow et. al. CVPR 2016](#Bardow16cvpr)*
- Reinbacher, C., Graber, G., Pock, T., *[Real-Time Intensity-Image Reconstruction for Event Cameras Using Manifold Regularisation](http://www.bmva.org/bmvc/2016/papers/paper009/)*, British Machine Vision Conference (BMVC), York, 2016. [PDF](http://www.bmva.org/bmvc/2016/papers/paper009/paper009.pdf), [YouTube](https://youtu.be/rvB2URrGT94), [Code](https://github.com/VLOGroup/dvs-reconstruction)
- Moeys, D. P., Li, C., Martel, J. N. P., Bamford, S., Longinotti, L., Motsnyi, V., Bello, D. S. S., Delbruck, T., *Color Temporal Contrast Sensitivity in Dynamic Vision Sensors*, IEEE Int. Symp. Circuits and Systems (ISCAS), Baltimore, MD, 2017. [PDF](http://www.ini.uzh.ch/admin/extras/doc_get.php?id=65634).


<a name="egomotion"></a>
## Localization and Ego-Motion Estimation
- *[Cook et. al. IJCNN 2011](#Cook11ijcnn)*; in case of rotational motion.
- Weikersdorfer, D. and Conradt, J., *[Event-based particle filtering for robot self-localization](http://doi.org/10.1109/ROBIO.2012.6491077)*, IEEE Int. Conf. on Robotics and Biomimetcs (ROBIO), Guangzhou, 2012, pp. 866-870. [PDF](https://mediatum.ub.tum.de/doc/1215541/835468.pdf)
- Censi, A., Strubel, J., Brandli, C., Delbruck, T., Scaramuzza, D., *[Low-latency localization by Active LED Markers tracking using a Dynamic Vision Sensor](https://doi.org/10.1109/IROS.2013.6696456)*, IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Tokyo, 2013. [PDF](http://rpg.ifi.uzh.ch/docs/IROS13_Censi.pdf), [Slides](http://rpg.ifi.uzh.ch/docs/IROS13_Censi.ppt)
- Mueggler, E., Huber, B., Scaramuzza, D., *[Event-based, 6-DOF Pose Tracking for High-Speed Maneuvers](https://doi.org/10.1109/IROS.2014.6942940)*, IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Chicago, IL, 2014, pp. 2761-2768. [PDF](http://rpg.ifi.uzh.ch/docs/IROS14_Mueggler.pdf), [YouTube](https://youtu.be/LauQ6LWTkxM)
- Gallego, G., Forster, C., Mueggler, E., Scaramuzza, D., *[Event-based Camera Pose Tracking using a Generative Event Model](https://arxiv.org/pdf/1510.01972v1)*, arXiv:1510.01972, 2015.
- Mueggler, E., Gallego G., Scaramuzza, D., *[Continuous-Time Trajectory Estimation for Event-based Vision Sensors](http://dx.doi.org/10.15607/RSS.2015.XI.036)*. Robotics: Science and Systems XI (RSS), Rome, Italy, 2015. [PDF]
- Gallego, G., Lund, J.E.A., Mueggler, E., Rebecq, H., Delbruck, T., Scaramuzza, D., *[Event-based, 6-DOF Camera Tracking for High-Speed Applications](https://arxiv.org/pdf/1607.03468.pdf)*, (Under review), 2016. [YouTube](https://youtu.be/iZZ77F-hwzs)
- Reinbacher, C., Munda, G., Pock, T., *[Real-Time Panoramic Tracking for Event Cameras](https://doi.org/10.1109/ICCPHOT.2017.7951488)*, IEEE Int. Conf. Computational Photography (ICCP), Stanford, CA, USA, 2017, pp. 1-9. [PDF](https://arxiv.org/abs/1703.05161), [YouTube](https://youtu.be/Qy0brSlirmk), [Code](https://github.com/VLOGroup/dvs-panotracking)


<a name="VOSLAM"></a>
## Visual Odometry and SLAM (Simultaneous Localization And Mapping)
- Weikersdorfer, D., Hoffmann, R., Conradt. J., *[Simultaneous localization and mapping for event-based vision systems](http://doi.org/10.1007/978-3-642-39402-7_14)*. Int. Conf. Computer Vision Systems (ICVS), 2013, pp. 133-142. [PDF](https://mediatum.ub.tum.de/doc/1191908/271955.pdf), [Slides](http://workshops.acin.tuwien.ac.at/ICVS/downloads/ICVS2013-ebslam_weikersdorfer.pdf)
- Censi, A. and Scaramuzza, D., *[Low-latency Event-based Visual Odometry](https://doi.org/10.1109/ICRA.2014.6906931)*, IEEE Int. Conf. Robotics and Automation (ICRA), Hong-Kong, 2014, pp. 703-710. [PDF](http://rpg.ifi.uzh.ch/docs/ICRA14_Censi.pdf), [Slides](https://censi.science/pub/research/2013-dvsd/201405-icra15-dvsd.pdf)
- <a name="Weikersdorfer14icra"></a>Weikersdorfer, D., Adrian, D. B., Cremers, D., Conradt, J., *[Event-based 3D SLAM with a depth-augmented dynamic vision sensor](https://doi.org/10.1109/ICRA.2014.6906882)*, IEEE Int. Conf. Robotics and Automation (ICRA), Hong-Kong, 2014, pp. 359-364.
- Weikersdorfer, D., *[Efficiency by Sparsity: Depth-Adaptive Superpixels and Event-based SLAM](http://nbn-resolving.de/urn:nbn:de:bvb:91-diss-20140701-1173294-0-6)*. Ph.D. Thesis, Technical University of Munich, Munich, Germany, 2014. [PDF](https://mediatum.ub.tum.de/download/1173294/1173294.pdf)
- Kueng, B., Mueggler, E., Gallego, G., Scaramuzza, D., *[Low-Latency Visual Odometry using Event-based Feature Tracks](https://doi.org/10.1109/IROS.2016.7758089)*, IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Daejeon, South Korea, 2016, pp. 16-23. [PDF](http://rpg.ifi.uzh.ch/docs/IROS16_Kueng.pdf). [YouTube](https://youtu.be/RDu5eldW8i8)
- Kim, H., Leutenegger, S., Davison, A.J., *[Real-Time 3D Reconstruction and 6-DoF Tracking with an Event Camera](http://doi.org/10.1007/978-3-319-46466-4_21)*, European Conference on Computer Vision (ECCV), 2016, pp. 349-364. [PDF](https://www.doc.ic.ac.uk/~ajd/Publications/kim_etal_eccv2016.pdf), [YouTube](https://youtu.be/yHLyhdMSw7w)
- Rebecq, H., Horstschaefer, T., Gallego, G., Scaramuzza, D., *[EVO: A Geometric Approach to Event-based 6-DOF Parallel Tracking and Mapping in Real-time](https://doi.org/10.1109/LRA.2016.2645143)*, IEEE Robotics and Automation Letters (RA-L), 2:2(593-600), 2017. [PDF](http://rpg.ifi.uzh.ch/docs/RAL16_EVO.pdf), [Youtube](https://youtu.be/bYqD2qZJlxE).
- Gallego, G. and Scaramuzza, D., *[Accurate Angular Velocity Estimation with an Event Camera](https://doi.org/10.1109/LRA.2016.2647639)*. IEEE Robotics and Automation Letters (RA-L), 2:2(632-639), 2017.
[PDF](http://rpg.ifi.uzh.ch/docs/RAL16_Gallego.pdf), [Youtube](https://youtu.be/v1sXWoOAs_0).


<a name="visual-inertial"></a>
## Visual-Inertial State Estimation
- Mueggler, E., Gallego, G., Rebecq, H., Scaramuzza, D., *[Continuous-Time Visual-Inertial Trajectory Estimation with Event Cameras](https://arxiv.org/pdf/1702.07389.pdf)*, (Under review), 2017.
- Zhu, A., Atanasov, N., Daniilidis, K., Event-based Visual Inertial Odometry, IEEE Conf. Computer Vision and Pattern Recognition (CVPR) 2017.


<a name="visual-stabilization"></a>
## Visual Stabilization
- Delbruck, T., Villanueva, V., and Longinotti, L., *[Integration of dynamic vision sensor with inertial measurement unit for electronically stabilized event-based vision](http://doi.org/10.1109/ISCAS.2014.6865714)*, IEEE Int. Symp. Circuits and Systems (ISCAS) 2014, 2636-2639. [YouTube](https://youtu.be/Tzy4WF6Qp-Y)

<a name="video-processing"></a>
## Video Processing
- Brandli, C., Muller, L., Delbruck, T., *[Real-time, high-speed video decompression using a frame- and event-based DAVIS sensor](https://doi.org/10.1109/ISCAS.2014.6865228)*, IEEE Int. Symp. on Circuits and Systems (ISCAS), Melbourne VIC, 2014, pp. 686-689.


<a name="pattern-recognition"></a>
## Pattern Recognition
- <a name="Lee12iscas"></a>Lee, J., Delbruck, T., Park, P. K. J., Pfeiffer, M., Shin, C. W., Ryu, H., Kang, B. C., *[Live demonstration: Gesture-Based remote control using stereo pair of dynamic vision sensors](https://doi.org/10.1109/ISCAS.2012.6272144)*, IEEE Int. Symp. Circuits and Systems (ISCAS) 2012, Seoul, South Korea, pp. 736-740. [PDF](http://www.zora.uzh.ch/75315/1/Lee_et_al_Live_demonstration.pdf), [YouTube](https://youtu.be/IlKimfJN21A)
- [Barua et. al. WACV 2016](#Barua16wacv). Face recognition.
- Orchard, G., Meyer, C., Etienne-Cummings, R., Posch, C., Thakor, N., Benosman, R., *[HFIRST: A Temporal Approach to Object Recognition](https://doi.org/10.1109/TPAMI.2015.2392947)*, IEEE Trans. Pattern Anal. Machine Intell. (TPAMI), 2015, 37(10):2028-2040. [PDF](https://arxiv.org/pdf/1508.01176.pdf)
    - [Code](http://www.garrickorchard.com/code/hfirst): HFIRST: A simple spiking neural network for recognition based on the canonical frame-based HMAX model.
- <a name="Moeys16ebccsp"></a>Moeys, D., Corradi F., Kerr, E., Vance, P., Das, G., Neil, D., Kerr, D., Delbruck, T., *[Steering a Predator Robot using a Mixed Frame/Event-Driven Convolutional Neural Network](https://doi.org/10.1109/EBCCSP.2016.7605233)*, IEEE Int. Conf. Event-Based Control Comm. and Signal Proc. (EBCCSP), Krakow, Poland, 2016. [PDF](https://arxiv.org/pdf/1606.09433.pdf), [YouTube 1](https://youtu.be/fL3YCIPxuhM), [YouTube 2](https://youtu.be/lPF3Youpmqk)
- Lagorce, X., Orchard, G., Gallupi, F., Shi, B., Benosman, R., *[HOTS: A Hierarchy Of event-based Time-Surfaces for pattern recognition](https://doi.org/10.1109/TPAMI.2016.2574707)*, IEEE Trans. Pattern Anal. Machine Intell. (TPAMI), 2017, 39(7):1346-1359.
- Lungu, I.-A., Corradi, F., Delbruck, T., *Live Demonstration: Convolutional Neural Network Driven by Dynamic Vision Sensor Playing RoShamBo*, IEEE Int. Symp. Circuits and Systems (ISCAS), Baltimore, MD, 2017. [YouTube](https://youtu.be/q5ua91n13TA), [Slides 36-39](http://rpg.ifi.uzh.ch/docs/ICRA17workshop/Delbruck.pdf)


<a name="control"></a>
## Control
- Delbruck, T. and Lichtsteiner, P., *[Fast sensory motor control based on event-based hybrid neuromorphic-procedural system](https://doi.org/10.1109/ISCAS.2007.378038)*, IEEE Int. Symp. Circuits and Systems, New Orleans, LA, 2007, pp. 845-848.
- Conradt, J., Cook, M., Berner, R., Lichtsteiner, P., Douglas, R. J., Delbruck, T., *[A Pencil Balancing Robot Using a Pair of AER Dynamic Vision Sensors](https://doi.org/10.1109/ISCAS.2009.5117867)*, IEEE Int. Symp. Circuits and Systems (ISCAS) 2009, pp. 781-784, 2009. [PDF](https://www.ini.uzh.ch/~conradt/publications/ISCAS2009-JConradt.pdf), [Poster](https://www.ini.uzh.ch/~conradt/publications/NIPS2008-JConradt.pdf), [Project page](https://www.ini.uzh.ch/~conradt/projects/PencilBalancer/), [YouTube 1](https://youtu.be/XVR5wEYkEGk), [YouTube 2](https://youtu.be/f9UngTdngY4), [YouTube 3](https://youtu.be/yCOnDc5r7p8)
- Conradt, J., Berner, R., Cook, M., Delbruck, T., *[An embedded AER dynamic vision sensor for low-latency pole balancing](https://doi.org/10.1109/ICCVW.2009.5457625)*, IEEE Int. Conf. Computer Vision Workshops (ICCVW), Kyoto, Japan, 2009. [PDF](http://www.ini.uzh.ch/admin/extras/doc_get.php?id=42580)
- Delbruck, T., Lang, M., *[Robotic Goalie with 3ms Reaction Time at 4% CPU Load Using Event-Based Dynamic Vision Sensor](https://doi.org/10.3389/fnins.2013.00223)*, Front. Neurosci. (2013) 7:223. [PDF](http://www.zora.uzh.ch/107801/1/fnins-07-00223.pdf), [YouTube](https://youtu.be/IC5x7ftJ96w)
- Censi, A., *[Efficient Neuromorphic Optomotor Heading Regulation](https://doi.org/10.1109/ACC.2015.7171931)*, The 2015 American Control Conference (ACC), Chicago, IL, 2015, pp. 3854-3861.
- Mueggler, E., Baumli, N., Fontana, F., Scaramuzza, D., *[Towards Evasive Maneuvers with Quadrotors using Dynamic Vision Sensors](https://doi.org/10.1109/ECMR.2015.7324048)*, Eur. Conf. Mobile Robots (ECMR), Lincoln, 2015. [PDF](http://rpg.ifi.uzh.ch/docs/ECMR15_Mueggler.pdf)
- Delbruck, T., Pfeiffer, M., Juston, R., Orchard, G., Mueggler, E., Linares-Barranco, A., Tilden, M. W., *[Human vs. computer slot car racing using an event and frame-based DAVIS vision sensor](https://doi.org/10.1109/ISCAS.2015.7169170)*, IEEE Int. Symp. Circuits and Systems (ISCAS), Lisbon, 2015, pp. 2409-2412. [YouTube 1](https://youtu.be/CnGPGiZuFRI), [YouTube 2](https://youtu.be/ALneVn-Ls2Q)
- [Moeys et. al. EBCCSP 2016](#Moeys16ebccsp)


<a name="datasets"></a>
## Datasets
- [Several datasets from the Sensors group at INI](http://sensors.ini.uzh.ch/databases.html) (Institute of Neuroinformatics), Zurich:
    - [DVS128 Dynamic Vision Sensor Silicon Retina data](https://sourceforge.net/p/jaer/wiki/AER%20data/)
- [Combined Dynamic Vision / RGB-D Dataset](http://ci.nst.ei.tum.de/EBSLAM3D/dataset/) associated to the paper [Weikersdorfer et. al. ICRA 2014](#Weikersdorfer14icra).
- Orchard, G., Jayawant, A., Cohen, G.K., Thakor, N., *[Converting Static Image Datasets to Spiking Neuromorphic Datasets Using Saccades](https://doi.org/10.3389/fnins.2015.00437)*. Front. Neurosci. (2015), 9:437. [YouTube](https://youtu.be/2RBKNhxHvdw)
    - [Neuromorphic-MNIST (N-MNIST) dataset](http://www.garrickorchard.com/datasets/n-mnist) is a spiking version of the original frame-based MNIST dataset (of handwritten digits). [YouTube](https://youtu.be/6qK97qM5aB4)
    - [The Neuromorphic-Caltech101 (N-Caltech101) dataset](http://www.garrickorchard.com/datasets/n-caltech101) is a spiking version of the original frame-based Caltech101 dataset. [YouTube](https://youtu.be/dxit9Ce5f_E)
- [DVS/DAVIS Optical Flow Dataset](https://docs.google.com/document/d/1r9sRYANGuDTUcfSSq-sL4sd79SfjHGNRul_10uztDaI/pub) associated to the paper [Rueckauer and Delbruck, FNINS 2016](#Rueckauer16fnins).
- Barranco, F., Fermuller, C., Aloimonos, Y., *[A Dataset for Visual Navigation with Neuromorphic Methods](https://dx.doi.org/10.3389%2Ffnins.2016.00049)*. Front. Neurosci. (2016), 10:49.
- E. Mueggler, H. Rebecq, G. Gallego, T. Delbruck, D. Scaramuzza, *[The Event-Camera Dataset and Simulator: Event-based Data for Pose Estimation, Visual Odometry, and SLAM](http://rpg.ifi.uzh.ch/davis_data.html)*, Int. J. Robotics Research, 36:2, pp. 142-149, 2017. [PDF](https://arxiv.org/pdf/1610.08336.pdf), [PDF IJRR](http://dx.doi.org/10.1177/0278364917691115), [Dataset](http://rpg.ifi.uzh.ch/davis_data.html).
- [VISUALISE Predator/Prey Dataset](https://www.dropbox.com/sh/x6nm6zl9rrd7yzn/AAB_Fa5F-Y4fSo1nrIJxc8Xoa?dl=0) associated to the paper [Moeys et. al. EBCCSP 2016](#Moeys16ebccsp)
- Hu, Y., Liu, H., Pfeiffer, M., Delbruck, T., *[DVS Benchmark Datasets for Object Tracking, Action Recognition, and Object Recognition](https://doi.org/10.3389/fnins.2016.00405)*, Front. Neurosci. 10:405. [Dataset](http://dgyblog.com/projects-term/dvs-dataset.html)
- Binas, J., Neil, D., Liu, S.-C., Delbruck, T., *[DDD17: End-To-End DAVIS Driving Dataset](https://www.openreview.net/pdf?id=HkehpKVG-)*. In Proc. 34th Int. Conf. Machine Learning, Sydney, Australia, PMLR 70, 2017. [Dataset](http://sensors.ini.uzh.ch/databases.html)


<a name="software"></a>
## Software
- [Matlab functions in jAER project](https://sourceforge.net/p/jaer/code/HEAD/tree/scripts/matlab/)
- [edvstools](https://github.com/Danvil/edvstools), by D. Weikersdorfer: A collection of tools for the embedded Dynamic Vision Sensor eDVS.
- [Matlab AER functions](https://github.com/gorchard/Matlab_AER_vision_functions) by G. Orchard. Some basic functions for filtering and displaying AER vision data, as well as making videos.
- [Python code for AER vision data](https://github.com/gorchard/event-Python) by G. Orchard.


<a name="processors-platforms"></a>
## Neuromorphic Processors and Platforms
- [Dynamic Neuromorphic Asynchronous Processor (DYNAP) by iniLabs](https://inilabs.com/products/dynap/)
  - Qiao, N., Mostafa, H., Corradi, F., Osswald, M., Stefanini, F., Sumislawska, D., Indiveri, G. *[A reconfigurable on-line learning spiking neuromorphic processor comprising 256 neurons and 128K synapses](https://doi.org/10.3389/fnins.2015.00141)*, Front. Neurosci. (2015) 9:141. [PDF](https://capocaccia.ethz.ch/capo/raw-attachment/wiki/2015/hybrid15/frontiers14-nlp.pdf)
  - Indiveri, G., Qiao, N., Corradi, F., *[Neuromorphic Architectures for Spiking Deep Neural Networks](https://doi.org/10.1109/IEDM.2015.7409623)*, IEEE Int. Electron Devices Meeting (IEDM), Washington, DC, 2015, pp. 4.2.1-4.2.4. [PDF](http://ncs.ethz.ch/pubs/pdf/Indiveri_etal15.pdf)
- Wiesmann, G., Schraml, S., Litzenberger, M., Belbachir, A. N., Hofstatter, M., Bartolozzi, C., *[Event-driven embodied system for feature extraction and object recognition in robotic applications](https://doi.org/10.1109/CVPRW.2012.6238898)*, IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), Providence, RI, 2012, pp. 76-82.
- Galluppi, F., Denk, C., Meiner, M. C., Stewart, T. C., Plana, L. A., Eliasmith, C., Furber, S., Conradt, J., *[Event-based neural computing on an autonomous mobile platform](https://doi.org/10.1109/ICRA.2014.6907270)*, IEEE Int. Conf. Robotics and Automation (ICRA), Hong Kong, 2014, pp. 2862-2867. [PDF](http://compneuro.uwaterloo.ca/files/publications/galluppi.2014.pdf)


<a name="workshops"></a>
## Workshops
- [ICRA 2015 Workshop on Innovative Sensing for Robotics](http://innovative-sensing.mit.edu/), with a focus on Neuromorphic Sensors.
- [ICRA 2017 First International Workshop on Event-based Vision](http://rpg.ifi.uzh.ch/ICRA17_event_vision_workshop.html).
- [The Telluride Neuromorphic Cognition Engineering Workshops](http://telluride.iniforum.ch/accounts/login/?next=/).
- [Capo Caccia Workshops toward Cognitive Neuromorphic Engineering](http://capocaccia.iniforum.ch/).


<a name="tutorials"></a>
## Tutorials
- [Event-Based Vision for High-Speed Robotics (slides)](http://www.rit.edu/kgcoe/iros15workshop/papers/IROS2015-WASRoP-Invited-04-slides.pdf) IROS 2015, Workshop on Alternative Sensing for Robot Perception.


<a name="people"></a>
## People / Organizations
- [Institute of NeuroInformatics](https://www.ini.uzh.ch/) (INI)  of the University of Zurich (UZH) and ETH Zurich.
- [iniLabs](http://www.inilabs.com) (Comerzialization of neuromorphic technology from INI).
- [Dynamic Vision Sensor (DVS) - asynchronous temporal contrast silicon retina](http://siliconretina.ini.uzh.ch/wiki/index.php)
- [Robotics and Perception Group](http://rpg.ifi.uzh.ch/research_dvs.html) (RPG-UZH).


<a name="contributing"></a>
# Contributing
Please see [CONTRIBUTING](https://github.com/uzh-rpg/event-based_vision_resources/blob/master/Contributing.md) for details.
