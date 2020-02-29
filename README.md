# Event-based Vision Resources

## Table of Contents:
- [Survey paper](#survey_paper)
- [Devices and Manufacturers](#devices)
- [Companies working on Event-based Vision](#companies_sftwr)
- [Neuromorphic Systems](#neuromorphic-systems)
- [Review papers](#reviewpapers)
    - [Bio-inspiration](#reviewpapers-bio)
    - [Algorithms, Applications](#reviewpapers-algs)

- [Applications / Algorithms](#algorithms)
    - [Feature Detection and Tracking](#feature-detection)
        - [Corners](#corner-detection)
        - [Particles in fluids](#particle-detection)
    - [Optical Flow Estimation](#optical-flow-estimation)
        - [Scene Flow Estimation](#scene-flow-estimation)
    - [Reconstruction of Visual Information](#visualization)
        - [Intensity-Image Reconstruction](#image-reconstruction)
        - [Video Synthesis](#video-synthesis)
        - [Super-resolution](#super-resolution)
        - [Tone mapping](#tone-mapping)
        - [Visual Stabilization](#visual-stabilization)
    - [Depth Estimation (3D Reconstruction)](#depth-estimation)
        - [Monocular](#depth-mono)
        - [Stereo](#depth-stereo)
        - [Stereoscopic panoramic imaging](#depth-stereo-pano)
    - [SLAM (Simultaneous Localization And Mapping)](#slam)
        - [Localization, Ego-motion estimation](#slam-localization)
        - [Visual Odometry](#visual-odometry)
        - [Visual-Inertial Odometry](#visual-inertial)
    - [Segmentation](#segmentation)
        - [Object Segmentation](#object-segmentation)
        - [Motion Segmentation](#motion-segmentation)
    - [Pattern recognition](#pattern-recognition)
        - [Object Recognition](#object-recognition)
        - [Gesture Recognition](#gesture-recognition)
        - [Representation / Feature Extraction](#learning-representation-features)
        - [Regression Tasks](#learning-regression)
        - [Learning Methods / Frameworks](#learning-methods-frameworks)
    - [Control](#control)
    - [Space Applications](#space)
    - [Tactile Sensing Applications](#tactile_sensing)

- [Signal Processing](#signal_processing)

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
    - [Master's Theses](#theses-master)
- [People / Organizations](#people)
- [Contributing](#contributing)

___
<br>

<a name="survey_paper"></a>
# Survey paper
- <a name="Gallego19arxiv"></a>Gallego, G., Delbruck, T., Orchard, G., Bartolozzi, C., Taba, B., Censi, A., Leutenegger, S., Davison, A., Conradt, J., Daniilidis, K., Scaramuzza, D.,  
*[**Event-based Vision: A Survey**](http://rpg.ifi.uzh.ch/docs/EventVisionSurvey.pdf)*,  
arXiv 2019.

<a name="devices"></a>
# Devices & Companies Manufacturing them
- **DVS (Dynamic Vision Sensor)**: Lichtsteiner, P., Posch, C., and Delbruck, T., *[A 128x128 120dB 15μs latency asynchronous temporal contrast vision sensor](http://doi.org/10.1109/JSSC.2007.914337)*, IEEE J. Solid-State Circuits, 43(2):566-576, 2008.
    - [Product page at iniVation](https://inivation.com/dvs/). [**Buy a DVS**](https://inivation.com/buy/)
    - [Product specifications](https://inivation.com/support/product-specifications/)    
    - [User guide](https://inivation.github.io/inivation-docs/Hardware user guides/User_guide_-_DVS128.html)
    - [Introductory videos about the DVS technology](https://inivation.com/dvs/videos/)
    - [iniVation AG](https://inivation.com/) invents, produces and sells neuromorphic technologies with a special focus on event-based vision into *business*. [Slides](http://rpg.ifi.uzh.ch/docs/ICRA17workshop/Jakobsen.pdf) by [S. E. Jakobsen](https://inivation.com/company/), board member of iniVation.
- **Samsung's DVS**
    - [Slides](http://rpg.ifi.uzh.ch/docs/CVPR19workshop/CVPRW19_Eric_Ryu_Samsung.pdf) and [Video](https://youtu.be/7fAPckjQSGE) by [Hyunsurk Eric Ryu](https://www.linkedin.com/in/hyunsurk-eric-ryu-82745712), Samsung Electronics  (2019).
    - Son, B., et al., *[A 640×480 dynamic vision sensor with a 9µm pixel and 300Meps address-event representation](https://doi.org/10.1109/ISSCC.2017.7870263)*, IEEE Int. Solid-State Circuits Conf. (ISSCC), San Francisco, CA, 2017, pp. 66-67.
    - [SmartThings Vision](https://www.samsung.com/se/smartthings/smartthings-vision-u999/) commercial product for home monitoring.
    - [Paper at IEDM 2019](#Park19iedm), about low-latency applications using Samsung's VGA DVS.
- **DAVIS (Dynamic and ç-Pixel Vision Sensor)** :
Brandli, C., Berner, R., Yang, M., Liu, S.-C., Delbruck, T., *[A 240x180 130 dB 3 µs Latency Global Shutter Spatiotemporal Vision Sensor](https://doi.org/10.1109/JSSC.2014.2342715)*, IEEE J. Solid-State Circuits, 49(10):2333-2341, 2014.
    - [Product page at iniVation](https://inivation.com/dvs/).  [**Buy a DAVIS**](https://inivation.com/buy/)
    - [Product specifications](https://inivation.com/support/product-specifications/)
    - [User guide](https://inivation.github.io/inivation-docs/Hardware%20user%20guides/User_guide_-_DAVIS240.html)
    - **Color-DAVIS**: Li, C., Brandli, C., Berner, R., Liu, H., Yang, M., Liu, S.-C., Delbruck, T., *[Design of an RGBW Color VGA Rolling and Global Shutter Dynamic and Active-Pixel Vision Sensor](https://doi.org/10.1109/ISCAS.2015.7168734)*, IEEE Int. Symp. Circuits and Systems (ISCAS), 2015, pp. 718-721.
- [**Insightness's Silicon Eye**](https://youtu.be/Y0mIb_MehK8) QVGA event sensor.
    - [The Silicon Eye Technology](http://www.insightness.com/?p=361)
    - [Slides](http://rpg.ifi.uzh.ch/docs/CVPR19workshop/CVPRW19_Insightness.pdf) and [Video](https://youtu.be/9IJwF9xYEoU) by [Stefan Isler](http://www.insightness.com/#team) (2019).
    - [Slides](http://rpg.ifi.uzh.ch/docs/ICRA17workshop/Insightness.pdf) and [Video](https://youtu.be/6YyOW6DDGKw) by [Christian Brandli](http://www.insightness.com/#team), CEO and co-founder of Insightness (2017).
- **ATIS (Asynchronous Time-based Image Sensor)**: Posch, C., Matolin, D., Wohlgenannt, R. (2011). *[A QVGA 143 dB Dynamic Range Frame-Free PWM Image Sensor With Lossless Pixel-Level Video Compression and Time-Domain CDS](http://doi.org/10.1109/JSSC.2010.2085952)*, IEEE J. Solid-State Circuits, 46(1):259-275, 2011. [PDF](https://www.neuromorphic-vision.com/public/publications/2/publication.pdf)
    - [Prophesee](http://www.prophesee.ai) (Formerly [Chronocam](http://www.chronocam.com/))  [**Buy a Prophesee EVK**](https://www.prophesee.ai/event-based-evk/)
    - [Prophesee Cameras Specifications](https://www.prophesee.ai/event-based-evk/)
    - [AIT Austrian Institute of Technology](https://www.ait.ac.at/en/research-fields/new-sensor-technologies/optical-sensor-systems-for-industrial-processes/)
- **[CelePixel](http://www.celepixel.com/)**, Shanghai. CeleX-V: the first 1 Mega-pixel event-camera sensor.
- **Sensitive DVS (sDVS)**
    - Leñero-Bardallo, J. A., Serrano-Gotarredona, T., Linares-Barranco, B., *[A 3.6us Asynchronous Frame-Free Event-Driven Dynamic-Vision-Sensor](https://doi.org/10.1109/JSSC.2011.2118490)*,  IEEE J. of Solid-State Circuits, 46(6):1443-1455, 2011.
    - Serrano-Gotarredona, T. and Linares-Barranco, B., *[A 128x128 1.5% Contrast Sensitivity 0.9% FPN 3us Latency 4mW Asynchronous Frame-Free Dynamic Vision Sensor Using Transimpedance Amplifiers](https://doi.org/10.1109/JSSC.2012.2230553)*,  IEEE J. Solid-State Circuits, 48(3):827-838, 2013.
- **DLS (Dynamic Line Sensor)**: Posch, C., Hofstaetter, M., Matolin, D., Vanstraelen, G., Schoen, P., Donath, N., and Litzenberger, M., *[A dual-line optical transient sensor with on-chip precision time-stamp generation](https://doi.org/10.1109/ISSCC.2007.373513)*, IEEE Int. Solid-State Circuits Conf. - Digest of Technical Papers, Lisbon Falls, MN, US, 2007.
    - [Fact sheet at AIT](https://www.ait.ac.at/fileadmin/mc/digital_safety_security/downloads/Factsheet_-_Linescan-Chip_DLS_en.pdf).
- **LWIR DVS**: Posch, C., Matolin, D., Wohlgenannt, R., Maier, T., Litzenberger, M., *[A Microbolometer Asynchronous Dynamic Vision Sensor for LWIR](https://doi.org/10.1109/JSEN.2009.2020658)*, IEEE Sensors Journal, 9(6):654-664, 2009.
    - Prototype, commercially n.a.
- **Smart DVS (GAEP)**: Posch, C., Hoffstaetter, M., Schoen, P., *[A SPARC-compatible general purpose Address-Event processor with 20-bit 10ns-resolution asynchronous sensor data interface in 0.18um CMOS](https://doi.org/10.1109/ISCAS.2010.5537575)*, IEEE Int. Symp. Circuits and Systems (ISCAS), 2010.
    - Prototype, commercially n.a.

<a name="companies_sftwr"></a>
# Companies working on Event-based Vision
- [iniVation AG](https://inivation.com/) invents, produces and sells neuromorphic technologies with a special focus on event-based vision into *business*.
- [iniLabs AG](https://inilabs.com/) invents neuromorphic technologies for *research*.
- [Samsung](http://www.samsung.com) develops Gen2 and Gen3 dynamic vision sensors and event-based vision solutions.
    - [IBM Research](http://www.research.ibm.com/articles/brain-chip.shtml) ([Synapse project](http://www.research.ibm.com/cognitive-computing/brainpower/)) and Samsung partenered to combine the [TrueNorth chip (brain) with a DVS (eye)](https://www.cnet.com/news/samsung-turns-ibms-brain-like-chip-into-a-digital-eye/).
- [Prophesee](http://www.prophesee.ai) (Formerly [Chronocam](http://www.chronocam.com/)) develops bio-inspired and self-adapting approach to the need for visual sensing and processing in autonomous vehicles, connected devices, security and surveillance systems.
- [Insightness AG](http://www.insightness.com/) builds visual systems to give mobile devices spatial awareness. [The Silicon Eye](http://www.insightness.com/?p=361) Technology.
- [SLAMcore](https://www.slamcore.com/) develops Localisation and mapping solutions for AR/VR, robotics & autonomous vehicles.
- [CelePixel](https://www.celepixel.com) (formerly [Hillhouse Technology](http://www.hillhouse-tech.com/)) offer integrated sensory platforms that incorporate various components and technologies, including a processing chipset and an image sensor (a dynamic vision sensor called CeleX).
- [AIT Austrian Institute of Technology](https://www.ait.ac.at/en/research-fields/new-sensor-technologies/optical-sensor-systems-for-industrial-processes/) sells neuromorphic sensor products.
    - [Inspection during production of carton packs](https://www.youtube.com/watch?v=8PZmb2z2bXw&index=39&list=PL659671AC92E70F19)
    - [UCOS Universal Counting Sensor](https://www.ait.ac.at/fileadmin/mc/digital_safety_security/downloads/Factsheet_-_People-Counting-Sensor_en.pdf)
    - [IVS Industrial Vision Sensor](https://www.ait.ac.at/fileadmin/mc/digital_safety_security/downloads/Factsheet_-_Industrial-Vision-Sensor_en.pdf)

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
- <a name="ZamarrenoRamos13tbcas"></a> Zamarreño-Ramos, C., Linares-Barranco, A., Serrano-Gotarredona, T., Linares-Barranco, B.,  
*[Multi-Casting Mesh AER: A Scalable Assembly Approach for Reconfigurable Neuromorphic Structured AER Systems. Application to ConvNets](https://doi.org/10.1109/TBCAS.2012.2195725)*,  
IEEE Trans. Biomed. Circuits Syst., 7(1):82-102, 2013.
- <a name="Liu14book"></a>Liu, S.-C., Delbruck, T., Indiveri, G., Whatley, A., Douglas, R.,  
*[Event-Based Neuromorphic Systems](http://eu.wiley.com/WileyCDA/WileyTitle/productCd-1118927621.html)*,  
Wiley. ISBN: 978-1-118-92762-5, 2014.
- <a name="Chicca14ieee"></a>Chicca, E., Stefanini, F., Bartolozzi, C., Indiveri, G.,  
*[Neuromorphic Electronic Circuits for Building Autonomous Cognitive Systems](http://dx.doi.org/10.1109/JPROC.2014.2313954)*,  
Proc. IEEE, 102(9):1367-1388, 2014.
- <a name="Vanarse16fnins"></a>Vanarse, A., Osseiran, A., Rassau, A,  
*[A Review of Current Neuromorphic Approaches for Vision, Auditory, and Olfactory Sensors](http://dx.doi.org/10.3389/fnins.2016.00115)*,  
Front. Neurosci. (2016), 10:115.
- <a name="Liu19msp"></a>Liu, S.-C., Rueckauer, B., Ceolini, E., Huber, A., Delbruck, T.,  
*[Event-Driven Sensing for Efficient Perception: Vision and audition algorithms](https://doi.org/10.1109/MSP.2019.2928127)*,  
IEEE Signal Processing Magazine, vol. 36, no. 6, pp. 29-37, 2019.

<a name="reviewpapers"></a>
# Review / Overview papers

<a name="reviewpapers-bio"></a>
## Sensor designs, Bio-inspiration
- <a name="Delbruck10iscas"></a>Delbruck, T.,  
*[Activity-driven, event-based vision sensors](https://doi.org/10.1109/ISCAS.2010.5537149)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2010. [PDF](https://e-lab.github.io/data/papers/ISCAS2010actsens.pdf).
- <a name="Posch12jinst"></a>Posch, C.,  
*[Bio-inspired vision](https://doi.org/10.1088/1748-0221/7/01/C01054)*,  
J. of Instrumentation, 7 C01054, 2012.  Bio-inspired explanation of the DVS and the ATIS. [PDF](https://www.neuromorphic-vision.com/public/publications/17/publication.pdf)
- Posch, C., Serrano-Gotarredona, T., Linares-Barranco, B., Delbruck, T.,  
*[Retinomorphic Event-Based Vision Sensors: Bioinspired Cameras With Spiking Output](https://doi.org/10.1109/JPROC.2014.2346153),*  
Proc. IEEE (2014), 102(10):1470-1484. [PDF](https://www.neuromorphic-vision.com/public/publications/21/publication.pdf)
- <a name="Posch15bicv"></a>Posch, C.,  
*[Bioinspired vision sensing](https://doi.org/10.1002/9783527680863.ch2)*,  
Biologically Inspired Computer Vision, Wiley-Blackwell, pp. 11-28, 2015. [book index](http://bicv.github.io/toc/index.html)
- <a name="Posch15ieee"></a>Posch, C., Benosman, R., Etienne-Cummings, R.,  
*[How Neuromorphic Image Sensors Steal Tricks From the Human Eye](https://spectrum.ieee.org/biomedical/devices/how-neuromorphic-image-sensors-steal-tricks-from-the-human-eye)*, also published as *[Giving Machines Humanlike Eyes](https://doi.org/10.1109/MSPEC.2015.7335800)*,  
IEEE Spectrum, 52(12):44-49, 2015. [PDF](https://www.neuromorphic-vision.com/public/publications/33/publication.pdf)
- <a name="Cho15sam"></a>Cho, D., Lee, T.-J.,  
*[A Review of Bioinspired Vision Sensors and Their Applications](https://doi.org/10.18494/SAM.2015.1133)*,  
Sensors and Materials, 27(6):447-463, 2015. [PDF](https://myukk.org/SM2017/sm_pdf/SM1083.pdf)


<a name="reviewpapers-algs"></a>
## Algorithms, Applications
- <a name="Delbruck12eccvw"></a>Delbruck, T.,  
*[Fun with asynchronous vision sensors and processing](https://www.ini.uzh.ch/~tobi/wiki/lib/exe/fetch.php?media=delbruck_funwithasynsensors_2012.pdf)*.  
Computer Vision - ECCV 2012. Workshops and Demonstrations. Springer Berlin/Heidelberg, 2012. A position paper and summary of recent accomplishments of the INI Sensors' group.
- <a name="Delbruck16essderc"></a>Delbruck, T.,  
*[Neuromorophic Vision Sensing and Processing (Invited paper)](https://doi.org/10.1109/ESSDERC.2016.7599576)*,  
46th Eur. Solid-State Device Research Conference (ESSDERC), Lausanne, 2016, pp. 7-14.
- Lakshmi, A., Chakraborty, A., Thakur, C.S.,  
*[Neuromorphic vision: From sensors to event-based algorithms](https://doi.org/10.1002/widm.1310)*,  
Wiley Interdiscip. Rev. Data Min. Knowl. Discov. 9(4), 2019.
- [Steffen, L. et al., Front. Neurorobot. 2019](#Steffen19fnbot),  
*Neuromorphic Stereo Vision: A Survey of Bio-Inspired Sensors and Algorithms*.
- [Gallego et al. arXiv 2019](#Gallego19arxiv),  
*[Event-based Vision: A Survey](http://rpg.ifi.uzh.ch/docs/EventVisionSurvey.pdf)*.


<a name="algorithms"></a>
# Algorithms

<a name="feature-detection"></a>
## Feature Detection and Tracking
- <a name="Litzenberger06dspws"></a>Litzenberger, M., Posch, C., Bauer, D., Belbachir, A. N., Schon. P., Kohn, B., Garn, H.,  
*[Embedded Vision System for Real-Time Object Tracking using an Asynchronous Transient Vision Sensor](https://doi.org/10.1109/DSPWS.2006.265448)*,  
IEEE 12th Digital Signal Proc. Workshop and 4th IEEE Signal Proc. Education Workshop, Teton National Park, WY, 2006, pp. 173-178. [PDF](http://www.belbachir.info/PDF/dsp2006.pdf)
    - <a name="Litzenberger06itsc"></a>Litzenberger, M., Kohn, B., Belbachir, A.N., Donath, N., Gritsch, G., Garn, H., Posch, C., Schraml, S.,  
*[Estimation of Vehicle Speed Based on Asynchronous Data from a Silicon Retina Optical Sensor](https://doi.org/10.1109/ITSC.2006.1706816)*,  
IEEE Intelligent Transportation Systems Conf., Toronto, Ont., 2006, pp. 653-658. [PDF](http://belbachir.info/PDF/itsc2006.pdf)
    - <a name="Bauer07ejes"></a>Bauer, D., Belbachir, A. N., Donath, N., Gritsch, G., Kohn, B., Litzenberger, M., Posch, C., Schön, P., Schraml, S.,  
*[Embedded Vehicle Speed Estimation System Using an Asynchronous Temporal Contrast Vision Sensor](https://link.springer.com/article/10.1155/2007/82174)*,  
EURASIP J. Embedded Systems, 2007:082174. [PDF](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.385.424&rep=rep1&type=pdf)
    - <a name="Litzenberger07icdsc"></a>Litzenberger, M., Belbachir, N., Schon, P., Posch, C.,  
*[Embedded Smart Camera for High Speed Vision](https://doi.org/10.1109/ICDSC.2007.4357509)*,  
ACM/IEEE Int. Conf. on Distributed Smart Cameras, 2007. [PDF](http://belbachir.info/PDF/icdsc2007.pdf)
- <a name="Ni12tro"></a>Ni, Z., Bolopion, A., Agnus, J., Benosman, R., Regnier, S.,  
*[Asynchronous event-based visual shape tracking for stable haptic feedback in microrobotics](https://doi.org/10.1109/TRO.2012.2198930)*,  
IEEE Trans. Robot., 28(5):1081-1089, 2012. [PDF](https://www.neuromorphic-vision.com/public/publications/15/publication.pdf)
    - [Ni, Ph.D. Thesis, 2013](#Ni13PhD),  
*Asynchronous Event Based Vision:  Algorithms and Applications to Microrobotics*.
    - <a name="Ni15neco"></a>Ni, Z., Ieng, S. H., Posch, C., Regnier, S., Benosman, R.,  
*[Visual Tracking Using Neuromorphic Asynchronous Event-Based Cameras](https://doi.org/10.1162/NECO_a_00720)*,  
Neural Computation (2015), 27(4):925-953. [PDF](https://www.neuromorphic-vision.com/public/publications/40/publication.pdf)
- <a name="Piatkowska12cvprw"></a>Piatkowska, E., Belbachir, A. N., Schraml, S., Gelautz, M.,  
*[Spatiotemporal multiple persons tracking using Dynamic Vision Sensor](https://doi.org/10.1109/CVPRW.2012.6238892)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2012, pp. 35-40. [PDF](https://publik.tuwien.ac.at/files/PubDat_209369.pdf)
- <a name="Lagorce15fnins"></a>Lagorce, X., Ieng, S.-H., Clady, X., Pfeiffer, M., Benosman, R.,  
*[Spatiotemporal features for asynchronous event-based data](http://dx.doi.org/10.3389/fnins.2015.00046)*,  
Front. Neurosci. (2015), 9:46.
    - <a name="Lagorce13iros"></a>Lagorce, X., Ieng, S. H., Benosman, R.,  
*[Event-based features for robotic vision](http://dx.doi.org/10.1109/IROS.2013.6696960)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2013, pp. 4214-4219.
- <a name="Saner14vmv"></a>Saner, D., Wang, O., Heinzle, S., Pritch, Y., Smolic, A., Sorkine-Hornung, A., Gross, M.,  
*[High-Speed Object Tracking Using an Asynchronous Temporal Contrast Sensor](http://dx.doi.org/10.2312/vmv.20141280)*,  
Int. Symp. Vision, Modeling and Visualization (VMV), 2014. [PDF](http://ahornung.net/files/pub/2014-vmv-siliconretina-saner.pdf)
- <a name="Lagorce15tnnls"></a>Lagorce, X., Meyer, C., Ieng, S. H., Filliat, D., Benosman, R.,  
*[Asynchronous Event-Based Multikernel Algorithm for High-Speed Visual Features Tracking](https://doi.org/10.1109/TNNLS.2014.2352401)*,  
IEEE Trans. Neural Netw. Learn. Syst. (TNNLS), 26(8):1710-1720, 2015. [PDF](https://www.neuromorphic-vision.com/public/publications/28/publication.pdf)
    - <a name="Lagorce14biocas"></a>Lagorce, X., Meyer, C., Ieng, S. H., Filliat, D., Benosman, R.,  
*[Live demonstration: Neuromorphic event-based multi-kernel algorithm for high speed visual features tracking](https://doi.org/10.1109/BioCAS.2014.6981681)*,  
IEEE Biomedical Circuits and Systems Conference (BioCAS), 2014, pp. 178.
- <a name="Reverter15tnnls"></a>D. Reverter Valeiras, D., Lagorce, X., Clady, X., Bartolozzi, C., Ieng, S., Benosman, R.,  
*[An Asynchronous Neuromorphic Event-Driven Visual Part-Based Shape Tracking](https://doi.org/10.1109/TNNLS.2015.2401834)*,  
IEEE Trans. Neural Netw. Learn. Syst. (TNNLS), 26(12):3045-3059, 2015. [PDF](https://www.neuromorphic-vision.com/public/publications/23/publication.pdf)
- <a name="LinaresBarranco15iscas"></a>Linares-Barranco, A., Gómez-Rodríguez, F., Villanueva, V., Longinotti, L., Delbrück, T.,    
*[A USB3.0 FPGA event-based filtering and tracking framework for dynamic vision sensors](https://doi.org/10.1109/ISCAS.2015.7169172)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2015.
- <a name="LinaresBarranco15iscas"></a>Leow, H. S., Nikolic, K.,  
*[Machine vision using combined frame-based and event-based vision sensor](https://doi.org/10.1109/ISCAS.2015.7168731)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2015.
- <a name="Liu16iscas"></a>Liu, H., Moeys, D. P., Das, G., Neil, D., Liu, S.-C., Delbruck, T.,  
*[Combined frame- and event-based detection and tracking](https://doi.org/10.1109/ISCAS.2016.7539103)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2016.
- <a name="Tedaldi16ebccsp"></a>Tedaldi, D., Gallego, G., Mueggler, E., Scaramuzza, D.,  
*[Feature detection and tracking with the dynamic and active-pixel vision sensor (DAVIS)](https://doi.org/10.1109/EBCCSP.2016.7605086)*,  
IEEE Int. Conf. Event-Based Control Comm. and Signal Proc. (EBCCSP), 2016. [PDF](http://rpg.ifi.uzh.ch/docs/EBCCSP16_Tedaldi.pdf), [YouTube](https://www.youtube.com/watch?v=nglfEkiK308)
    - [Kueng et al. IROS 2016](#Kueng16iros)
*Low-Latency Visual Odometry using Event-based Feature Tracks*.
- <a name="Brandli16ebccsp"></a>Braendli, C., Strubel, J., Keller, S., Scaramuzza, D., Delbruck, T.,  
*[ELiSeD - An Event-Based Line Segment Detector](https://doi.org/10.1109/EBCCSP.2016.7605244)*,  
Int. Conf. on Event-Based Control Comm. and Signal Proc. (EBCCSP), 2016. [PDF](http://rpg.ifi.uzh.ch/docs/EBCCSP16_Braendli.pdf)
- <a name="Glover16iros"></a>Glover, A. and Bartolozzi, C.,  
*[Event-driven ball detection and gaze fixation in clutter](https://doi.org/10.1109/IROS.2016.7759345)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2016, pp. 2203-2208. [YouTube](https://youtu.be/n6qTkw5U7YI), [Code](https://github.com/robotology/event-driven)
    - <a name="Glover17iros"></a>Glover, A. and Bartolozzi, C.,  
*[Robust Visual Tracking with a Freely-moving Event Camera](https://doi.org/10.1109/IROS.2017.8206226)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2017. [YouTube](https://youtu.be/xS-7xYRYSLc), [Code](https://github.com/robotology/event-driven)
    - <a name="Glover18irosw"></a>Glover, A., Stokes, A.B., Furber, S., Bartolozzi, C.,  
*[ATIS + SpiNNaker: a Fully Event-based Visual Tracking Demonstration](https://arxiv.org/pdf/1912.01320)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems Workshops (IROSW), 2018. Workshop on Unconventional Sensing and Processing for Robotic Visual Perception.
- <a name="Clady17fnins"></a>Clady, X., Maro, J.-M., Barré, S., Benosman, R. B.,  
*[A Motion-Based Feature for Event-Based Pattern Recognition](https://doi.org/10.3389/fnins.2016.00594)*.  
Front. Neurosci. (2017), 10:594. [PDF](https://www.neuromorphic-vision.com/public/publications/49/publication.pdf)
- <a name="Zhu17icra"></a>Zhu, A., Atanasov, N., Daniilidis, K.,  
*[Event-based Feature Tracking with Probabilistic Data Association](https://doi.org/10.1109/ICRA.2017.7989517)*,  
IEEE Int. Conf. Robotics and Automation (ICRA), 2017. [PDF](https://fling.seas.upenn.edu/~alexzhu/dynamic/wp-content/uploads/2017/07/EventBasedFeatureTrackingICRA2017.pdf), [YouTube](https://youtu.be/m93XCqAS6Fc), [Code](https://github.com/daniilidis-group/event_feature_tracking)
- <a name="BarriosAviles18electronics"></a>Barrios-Avilés, J., Iakymchuk, T., Samaniego, J., Medus, L.D., Rosado-Muñoz, A.,  
*[Movement Detection with Event-Based Cameras: Comparison with Frame-Based Cameras in Robot Object Tracking Using Powerlink Communication](https://doi.org/10.3390/electronics7110304)*,  
Electronics 2018, 7, 304. [PDF pre-print](https://arxiv.org/abs/1707.07188)
- <a name="Li17bmvc"></a>Li, J., Shi, F., Liu, W., Zou, D., Wang, Q., Park, P.K.J., Ryu, H.,  
*[Adaptive Temporal Pooling for Object Detection using Dynamic Vision Sensor](https://www.dropbox.com/s/m77i7cqqy7xbg51/0099.pdf?dl=1)*,  
British Machine Vision Conf. (BMVC), 2017.
- <a name="Peng17tnnls"></a>Peng, X., Zhao, B., Yan, R., Tang H., Yi, Z.,  
*[Bag of Events: An Efficient Probability-Based Feature Extraction Method for AER Image Sensors](http://dx.doi.org/10.1109/TNNLS.2016.2536741)*,  
IEEE Trans. Neural Netw. Learn. Syst. (TNNLS), 28(4):791-803, 2017.
- <a name="Ramesh19tpami"></a>Ramesh, B., Yang, H., Orchard, G., Le Thi, N.A., Xiang, C,  
*[DART: Distribution Aware Retinal Transform for Event-based Cameras](https://doi.org/10.1109/TPAMI.2019.2919301)*,  
IEEE Trans. Pattern Anal. Machine Intell. (TPAMI), 2019. [PDF](https://arxiv.org/pdf/1710.10800.pdf)
- <a name="Gehrig19ijcv"></a>Gehrig, D., Rebecq, H., Gallego, G., Scaramuzza, D.,  
*[EKLT: Asynchronous, Photometric Feature Tracking using Events and Frames](http://rpg.ifi.uzh.ch/docs/IJCV19_Gehrig.pdf)*,  
Int. J. Computer Vision (IJCV), 2019. [YouTube](https://youtu.be/ZyD1YPW1h4U), [Tracking code](https://github.com/uzh-rpg/rpg_eklt), [Evaluation code](https://github.com/uzh-rpg/rpg_feature_tracking_analysis)
    - <a name="Gehrig18eccv"></a>Gehrig, D., Rebecq, H., Gallego, G., Scaramuzza, D.,  
*[Asynchronous, Photometric Feature Tracking using Events and Frames](http://rpg.ifi.uzh.ch/docs/ECCV18_Gehrig.pdf)*,  
European Conf. Computer Vision (ECCV), 2018. [Poster](http://rpg.ifi.uzh.ch/docs/ECCV18_Gehrig_poster.pdf), [YouTube](https://youtu.be/A7UfeUnG6c4), [Oral presentation](https://youtu.be/7EvY8SxdLl8), [Tracking code](https://github.com/uzh-rpg/rpg_eklt), [Evaluation code](https://github.com/uzh-rpg/rpg_feature_tracking_analysis)
- <a name="LinaresBarrancoA18entropy"></a>Linares-Barranco, A., Liu, H., Rios-Navarro, A., Gomez-Rodriguez, F., Moeys, D., Delbruck, T.  
*[Approaching Retinal Ganglion Cell Modeling and FPGA Implementation for Robotics](https://doi.org/10.3390/e20060475)*,  
Entropy 2018, 20(6), 475.  
- <a name="Mitrokhin18iros"></a>Mitrokhin, A., Fermüller, C., Parameshwara, C., Aloimonos, Y.,  
*[Event-based Moving Object Detection and Tracking](https://doi.org/10.1109/IROS.2018.8593805)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2018. [PDF](https://arxiv.org/pdf/1803.04523.pdf), [YouTube](https://youtu.be/UCAJi0ZFaZ8), [Project page and Dataset](http://prg.cs.umd.edu/BetterFlow.html)
- <a name="Iacono18iros"></a>Iacono, M., Weber, S., Glover, A., Bartolozzi, C.,  
*[Towards Event-Driven Object Detection with Off-The-Shelf Deep Learning](https://doi.org/10.1109/IROS.2018.8594119)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2018.
- <a name="Ramesh18bmvc"></a>Ramesh, B., Zhang, S., Lee, Z.-W., Gao, Z., Orchard, G., Xiang, C.,  
*[Long-term object tracking with a moving event camera](http://bmvc2018.org/contents/papers/0814.pdf)*,  
British Machine Vision Conf. (BMVC), 2018.  [Video](http://bmvc2018.org/contents/supplementary/video/0814_video.mp4)
- <a name="Dardelet18arxiv"></a>Dardelet, L., Ieng, S.-H., Benosman, R.,  
*[Event-Based Features Selection and Tracking from Intertwined Estimation of Velocity and Generative Contours](https://arxiv.org/pdf/1811.07839)*,  
arXiv:1811.07839, 2018.
- <a name="Wu18chreoc"></a>Wu, J., Zhang, K., Zhang, Y., Xie, X., Shi, G.,  
*[High-Speed Object Tracking with Dynamic Vision Sensor](https://doi.org/10.1007/978-981-13-6553-9_18)*,  
China High Resolution Earth Observation Conference (CHREOC), 2018.
- <a name="Huang18tcsvt"></a>Huang, J., Wang, S., Guo, M., Chen, S.,  
*[Event-Guided Structured Output Tracking of Fast-Moving Objects Using a CeleX Sensor](https://doi.org/10.1109/TCSVT.2018.2841516)*,  
IEEE Trans. Circuits Syst. Video Technol. (TCSVT), vol. 28, no. 9, pp. 2413-2417, 2018.
- <a name="Renner19cvprw"></a>Renner, A., Evanusa, M., Sandamirskaya, Y.,  
*[Event-based attention and tracking on neuromorphic hardware](http://openaccess.thecvf.com/content_CVPRW_2019/papers/EventVision/Renner_Event-Based_Attention_and_Tracking_on_Neuromorphic_Hardware_CVPRW_2019_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2019. [Video pitch](https://youtu.be/eWBEJOr056E)
- <a name="Foster19elim"></a>Foster, B.J., Ye, D.H., Bouman, C.A.,  
*[Multi-target tracking with an event-based vision sensor and a partial-update GMPHD filter](https://www.ingentaconnect.com/contentone/ist/ei/2019/00002019/00000013/art00002?crawler=true&mimetype=application/pdf)*,  
IS&T International Symposium on Electronic Imaging 2019. Computational Imaging XVII.
- <a name="Alzugaray193dv"></a>Alzugaray, I., Chli, M.,  
*[Asynchronous Multi-Hypothesis Tracking of Features with Event Cameras](https://doi.org/10.3929/ethz-b-000360434)*,  
Int. Conf. 3D Vision (3DV), 2019. [PDF](https://doi.org/10.3929/ethz-b-000360434), [YouTube](https://youtu.be/eguV_AIbteU)
- <a name="LinaresBarranco19access"></a>Linares-Barranco, A., Perez-Pena, F., Moeys, D.P., Gomez-Rodriguez, F., Jimenez-Moreno, G., Delbruck, T.  
*[Low Latency Event-based Filtering and Feature Extraction for Dynamic Vision Sensors in Real-Time FPGA Applications](https://doi.org/10.1109/ACCESS.2019.2941282)*,  
IEEE Access, vol. 7, pp. 134926-134942, 2019. [Code](https://github.com/RTC-research-group/EDIP_library)
- <a name="Li19access"></a>Li, K., Shi, D., Zhang, Y., Li, R., Qin, W., Li, R.,  
*[Feature Tracking Based on Line Segments](https://doi.org/10.1109/ACCESS.2019.2933594)*,  
IEEE Access, vol. 7, pp. 110874-110883, 2019.
- <a name="Xu19arxiv"></a>Xu, L., Xu, W., Golyanik, V., Habermann, M., Fang, L., Theobalt, C.,  
*[EventCap: Monocular 3D Capture of High-Speed Human Motions using an Event Camera](https://arxiv.org/pdf/1908.11505)*,  
arXiv:1908.11505, 2019. [ZDNet news](https://www.zdnet.com/article/high-speed-motion-capture-using-a-single-event-camera/)
- <a name="Bolten19iccs"></a>Bolten T., Pohle-Fröhlich R., Tönnies K.D.,  
*[Application of Hierarchical Clustering for Object Tracking with a Dynamic Vision Sensor](https://doi.org/10.1007/978-3-030-22750-0_13)*,  
Int. Conf. Computational Science (ICCS) 2019. [PDF](https://www.hs-niederrhein.de/fileadmin/dateien/Institute_und_Kompetenzzentren/iPattern/selfarchived/bolten-iccs-2019.pdf)
- <a name="Chen19mm"></a>Chen, H., Wu, Q., Liang, Y., Gao, X., Wang, H.,  
*[Asynchronous Tracking-by-Detection on Adaptive Time Surfaces for Event-based Object Tracking](https://doi.org/10.1145/3343031.3350975)*,  
ACM Int. Conf. on Multimedia (MM), 2019.
- <a name="Reverter19tnnls"></a>Reverter Valeiras, D., Clady, X., Ieng, S.-H., Benosman, R.,  
*[Event-Based Line Fitting and Segment Detection Using a Neuromorphic Visual Sensor](https://doi.org/10.1109/TNNLS.2018.2807983)*,  
IEEE Trans. Neural Netw. Learn. Syst. (TNNLS), 30(4):1218-1230, 2019. [PDF](https://www.neuromorphic-vision.com/public/publications/51/publication.pdf)
- <a name="Li19fnbot"></a>Li, H., Shi, L.,  
*[Robust Event-Based Object Tracking Combining Correlation Filter and CNN Representation](https://doi.org/10.3389/fnbot.2019.00082)*,  
Front. Neurorobot. 13:82, 2019. [Dataset](https://figshare.com/s/70565903453eef7c3965)
- <a name="Chen2020arxiv"></a>Chen, H., Suter, D., Wu, Q., Wang, H.,  
*[End-to-end Learning of Object Motion Estimation from Retinal Events for Event-based Object Tracking](https://arxiv.org/pdf/2002.05911)*,  
arXiv, 2020.
- <a name="Monforte20aicas"></a>Monforte, M., Arriandiaga, A., Glover, A., Bartolozzi, C.,  
*[Exploiting Event Cameras for Spatio-Temporal Prediction of Fast-Changing Trajectories](https://arxiv.org/pdf/2001.01248)*,  
IEEE Int. Conf. Artificial Intelligence Circuits and Systems (AICAS), 2020.
- <a name="Seok20wacv"></a>Seok, H., Lim, J.,  
*[Robust Feature Tracking in DVS Event Stream using Bezier Mapping](http://openaccess.thecvf.com/content_WACV_2020/papers/Seok_Robust_Feature_Tracking_in_DVS_Event_Stream_using_Bezier_Mapping_WACV_2020_paper.pdf)*,  
IEEE Winter Conf. Applications of Computer Vision (WACV), 2020.  [YouTube](https://youtu.be/mskBdueW9Hc)


<a name="corner-detection"></a>
### Corner Detection and Tracking
- <a name="Clady15neunet"></a>Clady, X., Ieng, S.-H., Benosman, R.,  
*[Asynchronous event-based corner detection and matching](https://doi.org/10.1016/j.neunet.2015.02.013)*,  
Neural Networks (2015), 66:91-106. [PDF](https://www.neuromorphic-vision.com/public/publications/38/publication.pdf)
- <a name="Vasco16iros"></a>Vasco, V., Glover, A., Bartolozzi, C.,  
*[Fast event-based Harris corner detection exploiting the advantages of event-driven cameras](https://doi.org/10.1109/IROS.2016.7759610)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2016, pp. 4144-4149. [YouTube](https://youtu.be/YkI7AfBDBKE), [Code](https://github.com/robotology/event-driven)
- <a name="Mueggler17bmvc"></a>Mueggler, E., Bartolozzi, C., Scaramuzza, D.,  
*[Fast Event-based Corner Detection](http://rpg.ifi.uzh.ch/docs/BMVC17_Mueggler.pdf)*,  
British Machine Vision Conf. (BMVC), 2017. [YouTube](https://youtu.be/tgvM4ELesgI), [Code](https://github.com/uzh-rpg/rpg_corner_events)
    - <a name="Liu19cvprw"></a>Liu, H., Kao, W.-T., Delbruck, T.,  
*[Live Demonstration: A Real-time Event-based Fast Corner Detection Demo based on FPGA](http://openaccess.thecvf.com/content_CVPRW_2019/papers/EventVision/Liu_Live_Demonstration_A_Real-Time_Event-Based_Fast_Corner_Detection_Demo_Based_CVPRW_2019_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2019.
- <a name="Alzugaray18ral"></a>Alzugaray, I., Chli, M.,  
*[Asynchronous Corner Detection and Tracking for Event Cameras in Real Time](http://dx.doi.org/10.1109/LRA.2018.2849882)*,  
IEEE Robotics and Automation Letters (RA-L), 3(4):3177-3184, Oct. 2018.  [PDF](https://doi.org/10.3929/ethz-b-000277131), [YouTube](https://youtu.be/bKUAZ7IQcf0), [Code](https://github.com/ialzugaray/arc_star_ros).
- <a name="Alzugaray183dv"></a>Alzugaray, I., Chli, M.,  
*[ACE: An Efficient Asynchronous Corner Tracker for Event Cameras](https://doi.org/10.1109/3DV.2018.00080)*,  
Int. Conf. 3D Vision (3DV), 2018. [PDF](https://doi.org/10.3929/ethz-b-000291763), [YouTube](https://youtu.be/I31yQqmCsfs)
- <a name="Scheerlinck19ral"></a>Scheerlinck, C., Barnes, N., Mahony, R.,  
*[Asynchronous Spatial Image Convolutions for Event Cameras](https://doi.org/10.1109/LRA.2019.2893427)*,  
IEEE Robotics and Automation Letters (RA-L), 4(2):816-822, Apr. 2019.  [PDF](https://cedric-scheerlinck.github.io/files/2018_event_convolutions.pdf), [Website](https://cedric-scheerlinck.github.io/2018_event_convolutions)
- <a name="Manderscheid19cvpr"></a>Manderscheid, J., Sironi, A., Bourdis, N., Migliore, D., Lepetit, V.,  
*[Speed Invariant Time Surface for Learning to Detect Corner Points with Event-Based Cameras](http://openaccess.thecvf.com/content_CVPR_2019/html/Manderscheid_Speed_Invariant_Time_Surface_for_Learning_to_Detect_Corner_Points_CVPR_2019_paper.html)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2019.  [PDF](https://arxiv.org/pdf/1903.11332)
- <a name="Manderscheid19cvpr"></a>Li, R., Shi, D., Zhang, Y., Li, K., Li, R.,  
*[FA-Harris: A Fast and Asynchronous Corner Detector for Event Cameras](https://doi.org/10.1109/IROS40897.2019.8968491)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2019. [PDF](https://arxiv.org/pdf/1906.10925)

<a name="particle-detection"></a>
### Particle Detection and Tracking
- <a name="Drazen11eif"></a>Drazen, D., Lichtsteiner, P., Haefliger, P., Delbruck, T., Jensen, A.,  
*[Toward real-time particle tracking using an event-based dynamic vision sensor](https://doi.org/10.1007/s00348-011-1207-y)*,  
Experiments in Fluids (2011), 51(1):1465-1469. [PDF](http://www.zora.uzh.ch/60624/1/Drazen_EIF_2011.pdf)
- <a name="Ni11jmcro"></a>Ni, Z., Pacoret, C., Benosman, R., Ieng, S., Regnier, S.,  
*[Asynchronous event-based high speed vision for microparticle tracking](http://doi.org/10.1111/j.1365-2818.2011.03565.x)*,  
J. Microscopy (2011), 245(3):236-244. [PDF](https://www.neuromorphic-vision.com/public/publications/14/publication.pdf)
- <a name="Borer14isfv"></a>Borer, D.,  Rosgen, T.,  
*[Large-scale Particle Tracking with Dynamic Vision Sensors]()*,  
ISFV16 - 16th Int. Symp. Flow Visualization, Okinawa 2014. [Project page](http://www.ifd.mavt.ethz.ch/research/group-roesgen/dynamic-vision-sensors.html), [PDF](http://www.ifd.mavt.ethz.ch/content/dam/ethz/special-interest/mavt/fluid-dynamics/ifd-dam/research/documents/posters/experimental-methods/daniel_borer_dynamic_vision_sensor.pdf)


<a name="optical-flow-estimation"></a>
## Optical Flow Estimation
- <a name="Benosman12neunet"></a>Delbruck, T.,  
*[Frame-free dynamic digital vision](https://www.research-collection.ethz.ch/handle/20.500.11850/81769),*  
Int. Symp. on Secure-Life Electronics, Advanced Electronics for Quality Life and Society, pp. 21-26, 2008. [PDF](www.ini.uzh.ch/admin/extras/doc_get.php?id=42508)
- [Cook et. al. IJCNN 2011](#Cook11ijcnn),  
*Interacting maps for fast visual interpretation*.  (Joint estimation of optical flow, image intensity and angular velocity with a rotating event camera).
- <a name="Benosman12neunet"></a>Benosman, R., Ieng, S.-H., Clercq, C., Bartolozzi, C., Srinivasan, M.,  
*[Asynchronous Frameless Event-Based Optical Flow](https://doi.org/10.1016/j.neunet.2011.11.001),*  
Neural Networks (2012), 27:32-37. [PDF](https://www.neuromorphic-vision.com/public/publications/12/publication.pdf), [Suppl. Mat.](https://www.neuromorphic-vision.com/public/publications/12/supplementaryMaterial.zip)
- <a name="Orchard13biocas"></a>Orchard, G., Benosman, R., Etienne-Cummings, R., Thakor, N,  
*[A Spiking Neural Network Architecture for Visual Motion Estimation](https://doi.org/10.1109/BioCAS.2013.6679698)*,  
IEEE Biomedical Circuits and Systems Conf. (BioCAS), 2013. [PDF](https://www.researchgate.net/publication/261075772_A_spiking_neural_network_architecture_for_visual_motion_estimation), [Code](https://github.com/gorchard/Spiking_Motion)
- <a name="Benosman14tnnls"></a>Benosman, R., Clercq, C., Lagorce, X., Ieng, S.-H., Bartolozzi, C.,  
*[Event-Based Visual Flow](https://doi.org/10.1109/TNNLS.2013.2273537),*  
IEEE Trans. Neural Netw. Learn. Syst. (TNNLS), 25(2):407-417, 2014. [PDF](https://www.neuromorphic-vision.com/public/publications/3/publication.pdf), [Code (jAER): LocalPlanesFlow](https://sourceforge.net/p/jaer/code/HEAD/tree/jAER/trunk/src/ch/unizh/ini/jaer/projects/rbodo/opticalflow/LocalPlanesFlow.java)
    - <a name="Clady14fnins"></a>Clady, X., Clercq, C., Ieng, S.H., Houseini, F., Randazzo, M., Natale, L., Bartolozzi, C., Benosman, R.,  
*[Asynchronous visual event-based time-to-contact](https://dx.doi.org/10.3389%2Ffnins.2014.00009)*,  
Front. Neurosci. (2014), 8:9. [PDF](https://www.neuromorphic-vision.com/public/publications/30/publication.pdf)
    - <a name="Mueggler15icra"></a>E. Mueggler, C. Forster, N. Baumli, G. Gallego, D. Scaramuzza,  
*[Lifetime Estimation of Events from Dynamic Vision Sensors](http://dx.doi.org/10.1109/ICRA.2015.7139876)*,  
IEEE Int. Conf. Robotics and Automation (ICRA), 2015, pp. 4874-4881. [PDF](http://rpg.ifi.uzh.ch/docs/ICRA15_Mueggler.pdf), [PPT](http://rpg.ifi.uzh.ch/docs/ICRA15_Mueggler.pptm), [Code](https://www.github.com/uzh-rpg/rpg_event_lifetime)
    - <a name="Lee17iccas"></a>Lee, A. J., Kim, A.,  
*[Event-based Real-time Optical Flow Estimation](https://doi.org/10.23919/ICCAS.2017.8204333)*,  
IEEE Int. Conf. on Control, Automation and Systems (ICCAS), 2017.
    - <a name="Aung18iscas"></a>Aung, M.T., Teo, R., Orchard, G.,  
*[Event-based Plane-fitting Optical Flow for Dynamic Vision Sensors in FPGA](https://doi.org/10.1109/ISCAS.2018.8351588)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2018. [Code](https://github.com/gorchard/FPGA_event_based_optical_flow)
- <a name="Barranco14ieee"></a>Barranco, F., Fermüller, C., Aloimonos, Y.,  
*[Contour motion estimation for asynchronous event-driven cameras](https://doi.org/10.1109/JPROC.2014.2347207)*,  
Proc. IEEE (2014), 102(10):1537-1556. [PDF](http://www.cfar.umd.edu/~fer/postscript/contourmotion-dvs-final.pdf)
- <a name="Lee14icip"></a>Lee, J.H., Lee, K., Ryu, H., Park, P.K.J., Shin, C.W., Woo, J., Kim, J.-S.,  
*[Real-time motion estimation based on event-based vision sensor](https://doi.org/10.1109/ICIP.2014.7025040)*,  
IEEE Int. Conf. Image Processing (ICIP), 2014.
- <a name="Richter14bc"></a>Richter, C., Röhrbein, F., Conradt, J.,  
[Bio inspired optic flow detection using neuromorphic hardware](https://doi.org/10.12751/NNCN.BC2014.0032),  
Bernstein Conf. 2014. [PDF](https://mediatum.ub.tum.de/doc/1281617/789727.pdf)
- <a name="Barranco15iwann"></a>Barranco, F., Fermûller, C., Aloimonos, Y.,  
*[Bio-inspired Motion Estimation with Event-Driven Sensors](https://doi.org/10.1007/978-3-319-19258-1_27)*,  
Int. Work-Conf. Artificial Neural Networks (IWANN) 2015, Advances in Computational Intell., pp. 309-321.
- <a name="Conradt15robio"></a>Conradt, J.,  
*[On-Board Real-Time Optic-Flow for Miniature Event-Based Vision Sensors](https://doi.org/10.1109/ROBIO.2015.7419043)*,  
IEEE Int. Conf. Robotics and Biomimetics (ROBIO), 2015.
- <a name="Brosch15fnins"></a>Brosch, T., Tschechne, S., Neumann, H.,  
*[On event-based optical flow detection](https://doi.org/10.3389/fnins.2015.00137)*,  
Front. Neurosci. (2015), 9:137.
    - <a name="Tschechne14bict"></a>Tschechne, S., Brosch, T., Sailer, R., von Egloffstein, N., Abdul-Kreem L.I., Neumann, H.,  
*[On event-based motion detection and integration](http://dx.doi.org/10.4108/icst.bict.2014.257904)*,  
Int. Conf. Bio-inspired Information and Comm. Technol. (BICT), 2014. [PDF](https://dl.acm.org/citation.cfm?id=2744588)
    - <a name="Tschechne14annpr"></a>Tschechne, S., Sailer R., Neumann, H.,  
*[Bio-Inspired Optic Flow from Event-Based Neuromorphic Sensor Input](https://doi.org/10.1007/978-3-319-11656-3_16)*,  
IAPR Workshop on Artificial Neural Networks in Pattern Recognition (ANNPR) 2014, pp. 171-182.
    - <a name="Brosch15bict"></a>Brosch, T., Neumann, H.,  
*[Event-based optical flow on neuromorphic hardware](https://doi.org/10.4108/eai.3-12-2015.2262447)*,  
Int. Conf. Bio-inspired Information and Comm. Technol. (BICT), 2015. [PDF](https://dl.acm.org/citation.cfm?id=2954727)
    - <a name="Kosiorek15techrep"></a>Kosiorek, A., Adrian, D., Rausch, J., Conradt, J.,  
*[An Efficient Event-Based Optical Flow Implementation in C/C++ and CUDA](http://tum.neurocomputing.systems/fileadmin/w00bqs/www/publications/pp/2015SS-PP-RealTimeDVSOpticFlow.pdf),*  
Tech. Rep. TU Munich, 2015.
- <a name="Milde15ebccsp"></a>Milde, M. B., Bertrand, O.J.N., Benosman, R., Egelhaaf, M., Chicca, E.,  
*[Bioinspired event-driven collision avoidance algorithm based on optic flow](https://doi.org/10.1109/EBCCSP.2015.7300673)*,  
IEEE Int. Conf. Event-Based Control Comm. and Signal Proc. (EBCCSP), 2015.
- <a name="Giulioni16fnins"></a>Giulioni, M., Lagorce, X., Galluppi, F., Benosman, R.,  
*[Event-Based Computation of Motion Flow on a Neuromorphic Analog Neural Platform](https://doi.org/10.3389/fnins.2016.00035)*,  
Front. Neurosci. (2016), 10:35. [PDF](https://www.neuromorphic-vision.com/public/publications/46/publication.pdf)
    - <a name="Haessig19aicas"></a>Haessig, G., Galluppi, F., Lagorce, X., Benosman, R.,  
*[Neuromorphic networks on the SpiNNaker platform](https://doi.org/10.1109/AICAS.2019.8771512)*,  
IEEE Int. Conf. Artificial Intelligence Circuits and Systems (AICAS), 2019.
- <a name="Rueckauer16fnins"></a>Rueckauer, B. and Delbruck, T.,  
*[Evaluation of Event-Based Algorithms for Optical Flow with Ground-Truth from Inertial Measurement Sensor](https://doi.org/10.3389/fnins.2016.00176),*  
Front. Neurosci. (2016), 10:176.
    - [Code (jAER)](https://sourceforge.net/p/jaer/code/HEAD/tree/jAER/trunk/src/ch/unizh/ini/jaer/projects/rbodo/opticalflow/)
- <a name="Bardow16cvpr"></a>Bardow, P. A., Davison, A. J., Leutenegger, S.,  
*[Simultaneous Optical Flow and Intensity Estimation from an Event Camera](http://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Bardow_Simultaneous_Optical_Flow_CVPR_2016_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2016. [YouTube](https://youtu.be/1zqJpiheaaI), [Dataset: 4 sequences](http://wp.doc.ic.ac.uk/pb2114/datasets/)
- <a name="Stoffregen17acra"></a>Stoffregen, T., Kleeman, L.,  
*[Simultaneous Optical Flow and Segmentation (SOFAS) using Dynamic Vision Sensor](http://www.araa.asn.au/acra/acra2017/papers/pap127s1-file1.pdf)*,  
Australasian Conf. Robotics and Automation (ACRA), 2017. [PDF](https://arxiv.org/pdf/1805.12326.pdf), [YouTube](https://youtu.be/JVkQOW_iUqs)
- <a name="Haessig17tbcas"></a>Haessig, G., Cassidy, A. Alvarez, R., Benosman, R., Orchard, G.,  
*[Spiking Optical Flow for Event-based Sensors Using IBM's TrueNorth Neurosynaptic System](https://doi.org/10.1109/TBCAS.2018.2834558)*,  
IEEE Trans. Biomed. Circuits Syst., 12(4):860-870, 2018. [PDF](https://arxiv.org/pdf/1710.09820.pdf)
- [Gallego et. al. CVPR 2018](#Gallego18cvpr),  
*A Unifying Contrast Maximization Framework for Event Cameras, with Applications to Motion, Depth and Optical Flow Estimation*.
    - <a name="Stoffregen19cvpr"></a>Stoffregen, T., Kleeman, L.,  
*[Event Cameras, Contrast Maximization and Reward Functions: An Analysis](http://openaccess.thecvf.com/content_CVPR_2019/html/Stoffregen_Event_Cameras_Contrast_Maximization_and_Reward_Functions_An_Analysis_CVPR_2019_paper.html)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2019.
    - [Gallego et. al. CVPR 2019](#Gallego19cvpr),  
*Focus Is All You Need: Loss Functions For Event-based Vision*.
    - [Stoffregen et. al. ICCV 2019](#Stoffregen19iccv),  
*Event-Based Motion Segmentation by Motion Compensation*.
- <a name="Zhu18rss"></a>Zhu, A., Yuan, L., Chaney, K., Daniilidis, K.,  
*[EV-FlowNet: Self-Supervised Optical Flow Estimation for Event-based Cameras](http://www.roboticsproceedings.org/rss14/p62.pdf)*,  
Robotics: Science and Systems (RSS), 2018. [PDF](https://arxiv.org/abs/1802.06898), [YouTube](https://youtu.be/eMHZBSoq0sE), [Code](https://github.com/daniilidis-group/EV-FlowNet)
    - [Gehrig et. al. ICCV 2019](#Gehrig19iccv),  
*End-to-End Learning of Representations for Asynchronous Event-Based Data*.
- <a name="Liu18bmvc"></a>Liu, M., Delbruck, T.,  
*[Adaptive Time-Slice Block-Matching Optical Flow Algorithm for Dynamic Vision Sensors](http://bmvc2018.org/contents/papers/0280.pdf)*,  
British Machine Vision Conf. (BMVC), 2018. [Supplementary material](https://docs.google.com/document/d/10X0z4zznuV9j1OOjWpJGv-YCWujkF7FiYjG6efwUrP0/edit), [Video](https://youtu.be/fGJ8jyqziBI)
    - <a name="Liu17iscas"></a>Liu, M., Delbruck, T.,  
*[Block-Matching Optical Flow for Dynamic Vision Sensors: Algorithm and FPGA Implementation](https://arxiv.org/pdf/1706.05415.pdf)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2017.
- <a name="Ye18arxiv"></a>Ye, C., Mitrokhin, A., Parameshwara, C., Fermüller, C., Yorke, J. A., Aloimonos,Y,  
*[Unsupervised Learning of Dense Optical Flow and Depth from Sparse Event Data](https://arxiv.org/pdf/1809.08625.pdf)*,  
arXiv:1809.08625, 2018.
- <a name="Akolkar18arxiv"></a>Akolkar, H., Ieng, S.-H., Benosman, R.,  
*[See before you see: Real-time high speed motion prediction using fast aperture-robust event-driven visual flow](https://arxiv.org/pdf/1811.11135)*,  
arXiv:1811.11135, 2018.
- <a name="Nagata19iwait"></a>Nagata, J., Sekikawa, Y., Hara, K., Aoki, Y.,  
[FOE-based regularization for optical flow estimation from an in-vehicle event camera](https://doi.org/10.1117/12.2521520),  
Proc. SPIE 11049, Int. Workshop on Advanced Image Technology (IWAIT), 2019.
- <a name="ParedesValles19tpami"></a>Paredes-Valles, F., Scheper, K. Y. W., de Croon, G. C. H. E.,  
*[Unsupervised Learning of a Hierarchical Spiking Neural Network for Optical Flow Estimation: From Events to Global Motion Perception](https://ieeexplore.ieee.org/document/8660483)*,  
IEEE Trans. Pattern Anal. Mach. Intell (TPAMI), 2019. [PDF](https://arxiv.org/abs/1807.10936), [YouTube](https://www.youtube.com/watch?v=FJrba02kZII&list=PL_KSX9GOn2P80tm3IsgbmPAUi2KDE53zI&index=2&t=0s), [Code](https://github.com/tudelft/cuSNN).
- <a name="Zhu19cvpr"></a>Zhu, A. Z., Yuan, L., Chaney, K., Daniilidis, K.,  
*[Unsupervised Event-Based Learning of Optical Flow, Depth, and Egomotion](http://openaccess.thecvf.com/content_CVPR_2019/papers/Zhu_Unsupervised_Event-Based_Learning_of_Optical_Flow_Depth_and_Egomotion_CVPR_2019_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2019. [PDF](https://arxiv.org/pdf/1812.08156), [YouTube](https://youtu.be/aDzFSG4yV0M)
    - <a name="Zhu18eccvw"></a>Zhu, A. Z., Yuan, L., Chaney, K., Daniilidis, K.,  
*[Unsupervised Event-Based Optical Flow Using Motion Compensation](https://doi.org/10.1007/978-3-030-11024-6_54)*,  
European Conf. Computer Vision Workshops (ECCVW), 2018. [PDF](http://openaccess.thecvf.com/content_ECCVW_2018/papers/11134/Zhu_Unsupervised_Event-based_Optical_Flow_using_Motion_Compensation_ECCVW_2018_paper.pdf)
- <a name="Khoei19neco"></a>Khoei, M.A., Benosman, R.,  
*[Asynchronous Event-Based Motion Processing: From Visual Events to Probabilistic Sensory Representation](https://doi.org/10.1162/neco_a_01191)*,  
Neural Computation (2019), 31(6):1114-1138. [PDF](https://www.neuromorphic-vision.com/public/publications/56/publication.pdf)
- <a name="Almatrafi19davis"></a>Almatrafi, M. M.,  Hirakawa, K.,  
*[DAViS Camera Optical Flow](http://doi.org/10.1109/TCI.2019.2948787)*,  
IEEE Trans. Comput. Imag. (TCI), 6:396-407, 2019.


<a name="scene-flow-estimation"></a>
### Scene Flow Estimation
- <a name="Ieng17fnins"></a>Ieng, S.-H., Carneiro, J., Benosman, R.,  
*[Event-Based 3D Motion Flow Estimation Using 4D Spatio Temporal Subspaces Properties](https://doi.org/10.3389/fnins.2016.00596)*,  
Front. Neurosci. (2017), 10:596.
    - [Carneiro, Ph.D. Thesis, 2014](#Carneiro14PhD),  
*Asynchronous Event-Based 3D Vision - Chapter 3*.


<a name="visualization"></a>
## Reconstruction of Visual Information


<a name="image-reconstruction"></a>
### Intensity-Image Reconstruction from events
- <a name="Cook11ijcnn"></a>Cook, M., Gugelmann, L., Jug, F., Krautz, C., Steger, A.,  
*[Interacting maps for fast visual interpretation](https://doi.org/10.1109/IJCNN.2011.6033299)*,  
Int. Joint Conf. on Neural Networks (IJCNN), San Jose, CA, 2011, pp. 770-776. [PDF](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.690.7666&rep=rep1&type=pdf), [YouTube](https://youtu.be/irX3Nd5U0hY)
    - <a name="Martel15irosw"></a>Martel, J. N. P., Cook, M.,  
    *[A Framework of Relational Networks to Build Systems with Sensors able to Perform the Joint Approximate Inference of Quantities](https://doi.org/10.5167/uzh-121743)*,  
    IEEE/RSJ Int. Conf. Intelligent Robots and Systems Workshop (IROSW), 2015. Workshop on Unconventional Computing for Bayesian Inference. [PDF](http://www.zora.uzh.ch/121743/1/RelationalNetSensor.pdf)
    - <a name="Martel15iscas"></a>Martel, J. N. P., Chau, M., Dudek, P., Cook, M.,  
    *[Toward joint approximate inference of visual quantities on cellular processor arrays](https://doi.org/10.1109/ISCAS.2015.7169083)*,  
    IEEE Int. Symp. Circuits and Systems (ISCAS), 2015.
- [Belbachir et al. CVPRW 2014](#Belbachir14cvprw),  
*A Novel HDR Depth Camera for Real-time 3D 360-degree Panoramic Vision*.
- <a name="Kim14bmvc"></a>Kim, H., Handa, A., Benosman, R., Ieng, S.-H., Davison, A. J.,  
*[Simultaneous Mosaicing and Tracking with an Event Camera](http://www.bmva.org/bmvc/2014/papers/paper066/)*,  
British Machine Vision Conf. (BMVC), 2014. [PDF](http://www.bmva.org/bmvc/2014/files/paper066.pdf), [YouTube](https://youtu.be/l6qxeM1DbXU).
    - [Code for intensity reconstruction](https://github.com/uzh-rpg/rpg_image_reconstruction_from_events).
- <a name="Barua16wacv"></a>Barua, S., Miyatani, Y., Veeraraghavan, A.,  
*[Direct face detection and video reconstruction from event cameras](http://doi.org/10.1109/WACV.2016.7477561)*,  
IEEE Winter Conf. Applications of Computer Vision (WACV), 2016. [YouTube](https://youtu.be/yGDVlN-L1TU)
- [Bardow et. al. CVPR 2016](#Bardow16cvpr),  
*Simultaneous Optical Flow and Intensity Estimation from an Event Camera*.
- <a name="Moeys17iscas"></a>Moeys, D. P., Li, C., Martel, J. N. P., Bamford, S., Longinotti, L., Motsnyi, V., Bello, D. S. S., Delbruck, T.,  
*[Color Temporal Contrast Sensitivity in Dynamic Vision Sensors](http://dx.doi.org/10.1109/ISCAS.2017.8050412)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2017. [PDF](http://www.ini.uzh.ch/admin/extras/doc_get.php?id=65634).
- <a name="Munda18ijcv"></a>Munda, G., Reinbacher, C., Pock, T.,  
*[Real-Time Intensity-Image Reconstruction for Event Cameras Using Manifold Regularisation](https://doi.org/10.1007/s11263-018-1106-2)*,  
Int. J. of Computer Vision (IJCV), 2018.
    - <a name="Reinbacher16bmvc"></a>Reinbacher, C., Graber, G., Pock, T.,  
*[Real-Time Intensity-Image Reconstruction for Event Cameras Using Manifold Regularisation](http://www.bmva.org/bmvc/2016/papers/paper009/)*,  
British Machine Vision Conf. (BMVC), 2016. [PDF](http://www.bmva.org/bmvc/2016/papers/paper009/paper009.pdf), [YouTube](https://youtu.be/rvB2URrGT94), [Code](https://github.com/VLOGroup/dvs-reconstruction)
- <a name="Watkins18icons"></a>Watkins, Y., Thresher, A., Mascarenas, D., Kenyon,  G.T.,  
*[Sparse Coding Enables the Reconstruction of High-Fidelity Images and Video from Retinal Spike Trains](https://doi.org/10.1145/3229884.3229892)*,  
Int. Conf. Neuromorphic Systems (ICONS), 2018. Article No. 8. [PDF](https://dl.acm.org/ft_gateway.cfm?id=3229892&ftid=1990359&dwn=1&CFID=41965358&CFTOKEN=fe90e12f8b0b321e-23C508A3-0508-BCD6-37A17F6C8E171DAB)
- <a name="Scheerlinck18accv"></a>Scheerlinck, C., Barnes, N., Mahony, R.,  
*[Continuous-time Intensity Estimation Using Event Cameras](https://cedric-scheerlinck.github.io/files/2018_scheerlinck_continuous-time_intensity_estimation.pdf)*,  
Asian Conf. Computer Vision (ACCV), 2018. [PDF](https://cedric-scheerlinck.github.io/files/2018_scheerlinck_continuous-time_intensity_estimation.pdf), [YouTube](https://youtu.be/bZ0ZKido0Ag), [Website](https://cedric-scheerlinck.github.io/continuous-time-intensity-estimation)
- <a name="Mostafavi19cvpr"></a>Mostafavi I., S.M., Wang, L., Ho, Y.S., Yoon, K.J.,  
*[Event-based High Dynamic Range Image and Very High Frame Rate Video Generation using Conditional Generative Adversarial Networks](http://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Event-Based_High_Dynamic_Range_Image_and_Very_High_Frame_Rate_CVPR_2019_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2019. [PDF](https://arxiv.org/abs/1811.08230)
- <a name="Rebecq20tpami"></a>Rebecq, H., Ranftl, R., Koltun, V., Scaramuzza, D.,  
*[High Speed and High Dynamic Range Video with an Event Camera](https://doi.org/10.1109/TPAMI.2019.2963386)*,  
IEEE Trans. Pattern Anal. Machine Intell. (TPAMI), 2020. [PDF](http://rpg.ifi.uzh.ch/docs/TPAMI19_Rebecq.pdf),  [YouTube](https://youtu.be/eomALySSGVU), [Code](https://github.com/uzh-rpg/rpg_e2vid), [Project page](http://rpg.ifi.uzh.ch/E2VID/)
    - <a name="Rebecq19cvpr"></a>Rebecq, H., Ranftl, R., Koltun, V., Scaramuzza, D.,  
*[Events-to-Video: Bringing Modern Computer Vision to Event Cameras](http://rpg.ifi.uzh.ch/docs/CVPR19_Rebecq.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2019. [PDF](http://rpg.ifi.uzh.ch/docs/CVPR19_Rebecq.pdf),  [YouTube](https://youtu.be/IdYrC4cUO0I), [Slides](http://rpg.ifi.uzh.ch/docs/CVPR19workshop/CVPRW19_Henri_Rebecq.pdf), [Video pitch](https://youtu.be/1LZKtnQ-6lA).
    - <a name="Scheerlinck20wacv"></a>Scheerlinck, C., Rebecq, H., Gehrig, D., Barnes, N., Mahony, R., Scaramuzza, D.,  
*[Fast Image Reconstruction with an Event Camera](https://cedric-scheerlinck.github.io/firenet)*,  
IEEE Winter Conf. Applications of Computer Vision (WACV), 2020. [PDF](https://cedric-scheerlinck.github.io/files/2019_firenet.pdf),  [YouTube](https://youtu.be/QaGYFtR2-X8), [Website](https://cedric-scheerlinck.github.io/firenet)
- [Scheerlinck et al., CVPRW 2019](#Scheerlinck19cvprw),  
*CED: Color Event Camera Dataset*.
- <a name="Nagata20wacv"></a>Nagata, J., Sekikawa, Y., Hara, K., Suzuki, T., Aoki, Y.,  
*[QR-code Reconstruction from Event Data via Optimization in Code Subspace](http://openaccess.thecvf.com/content_WACV_2020/papers/Nagata_QR-code_Reconstruction_from_Event_Data_via_Optimization_in_Code_Subspace_WACV_2020_paper.pdf)*,  
IEEE Winter Conf. Applications of Computer Vision (WACV), 2020.


<a name="video-synthesis"></a>
### Video Synthesis
- <a name="Brandli14iscas"></a>Brandli, C., Muller, L., Delbruck, T.,  
*[Real-time, high-speed video decompression using a frame- and event-based DAVIS sensor](https://doi.org/10.1109/ISCAS.2014.6865228)*,  
IEEE Int. Symp. on Circuits and Systems (ISCAS), 2014.
    - [Brandli, Ph.D. Thesis, 2014](#Brandli15PhD),  
*Event-Based Machine Vision - Section 4.11*.
- <a name="Liu17tvc"></a>Liu HC., Zhang FL., Marshall D., Shi L., Hu SM.,  
*[High-speed Video Generation with an Event Camera](https://link.springer.com/article/10.1007/s00371-017-1372-y)*,  
The Visual Computer, 2017. [PDF](https://cg.cs.tsinghua.edu.cn/papers/TVC-2017-HS-Video.pdf).
- <a name="Shedligeri19jei"></a>Shedligeri, P.A., Mitra, K.,  
*[Photorealistic Image Reconstruction from Hybrid Intensity and Event based Sensor](https://doi.org/10.1117/1.JEI.28.6.063012)*,  
J. Electronic Imaging, 28(6), 063012 (2019). [PDF](https://arxiv.org/pdf/1805.06140.pdf)
- <a name="Wang19iccvw"></a>Wang, Z., Jiang, W., Katsaggelos, A., Cossairt, O.,  
*[Event-driven Video Frame Synthesis](http://openaccess.thecvf.com/content_ICCVW_2019/papers/PBDL/Wang_Event-Driven_Video_Frame_Synthesis_ICCVW_2019_paper.pdf)*,  
IEEE Int. Conf. Computer Vision Workshops (ICCVW), 2019. [PDF](https://arxiv.org/abs/1902.09680)
- <a name="Pan19cvpr"></a>Pan, L., Scheerlinck, C., Yu, X., Hartley, R., Liu, M., Dai, Y.,  
*[Bringing a Blurry Frame Alive at High Frame-Rate with an Event Camera](http://openaccess.thecvf.com/content_CVPR_2019/papers/Pan_Bringing_a_Blurry_Frame_Alive_at_High_Frame-Rate_With_an_CVPR_2019_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2019. [PDF](https://arxiv.org/pdf/1811.10180). [Slides](http://rpg.ifi.uzh.ch/docs/CVPR19workshop/CVPRW19_Yuchao_Dai.pdf), [Video CVPR](https://drive.google.com/file/d/1NscnUF2QxK0of4ZW7T8kneJTH1X76l2u/view), [Video CVPRW](https://youtu.be/JcgboJ_7JAE), [Code](https://github.com/panpanfei/Bringing-a-Blurry-Frame-Alive-at-High-Frame-Rate-with-an-Event-Camera)
    - <a name="Pan19arxiv"></a>Pan, L., Hartley, R., Scheerlinck, C., Liu, M., Yu, X., Dai, Y.,  
*[High Frame Rate Video Reconstruction based on an Event Camera](https://arxiv.org/pdf/1903.06531)*,  
arXiv, 2019.
- <a name="Pini19iciap"></a>Pini, S., Borghi, G., Vezzani, R., Cucchiara, R.,  
*[Video synthesis from Intensity and Event Frames](https://doi.org/10.1007/978-3-030-30642-7_28)*,  
Int. Conf. Image Analysis and Processing (ICIAP), 2019. LNCS, vol 11751. [PDF](https://iris.unimore.it/retrieve/handle/11380/1178955/224434/ICIAP19_Event_Cameras.pdf)
- <a name="Pini20visapp"></a>Pini S., Borghi G., Vezzani R.,  
*[Learn to See by Events: Color Frame Synthesis from Event and RGB Cameras](http://hdl.handle.net/11380/1185831)*,  
Int. Joint Conf. on Computer Vision, Imaging and Computer Graphics Theory and Applications (VISAPP) 2020. [PDF](https://arxiv.org/pdf/1812.02041)

<a name="super-resolution"></a>
### Super-resolution
- <a name="Li19neucom"></a>Li, H., Li, G., Shi, L.,  
*[Super-resolution of spatiotemporal event-stream image](https://doi.org/10.1016/j.neucom.2018.12.048)*,  
Neurocomputing, vol. 335, pp. 206-214, 2019. [PDF pre-print](https://arxiv.org/abs/1802.02398)
- <a name="Mostafavi19arxiv"></a>Mostafavi I., S.M.,  Choi, J., Yoon, K.J,  
*[Learning to Super Resolve Intensity Images from Events](https://arxiv.org/abs/1912.01196)*,  
arXiv, 2019.

<a name="tone-mapping"></a>
### Tone Mapping
- <a name="SimonChane16fnins"></a>Simon Chane, C., Ieng, S.-H., Posch, C., Benosman, R.,  
*[Event-Based Tone Mapping for Asynchronous Time-Based Image Sensor](https://doi.org/10.3389/fnins.2016.00391)*,  
Front. Neurosci. (2016), 10:391. [PDF](https://www.neuromorphic-vision.com/public/publications/43/publication.pdf)

<a name="visual-stabilization"></a>
### Visual Stabilization
- <a name="Delbruck14iscas"></a>Delbruck, T., Villanueva, V., Longinotti, L.,  
*[Integration of dynamic vision sensor with inertial measurement unit for electronically stabilized event-based vision](http://doi.org/10.1109/ISCAS.2014.6865714)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2014. [YouTube](https://youtu.be/Tzy4WF6Qp-Y)


<a name="depth-estimation"></a>
## Depth Estimation (3D Reconstruction)

<a name="depth-mono"></a>
### Monocular Depth Estimation
- <a name="Rebecq17ijcv"></a>Rebecq, H., Gallego, G., Mueggler, E., Scaramuzza, D.,  
*[EMVS: Event-Based Multi-View Stereo—3D Reconstruction with an Event Camera in Real-Time](https://doi.org/10.1007/s11263-017-1050-6)*,  
Int. J. of Computer Vision (IJCV), 126(12):1394-1414, 2018. [PDF](http://rpg.ifi.uzh.ch/docs/IJCV17_Rebecq.pdf), [YouTube](https://youtu.be/EFpZcpd9XJ0), [Code](https://github.com/uzh-rpg/rpg_emvs).
    - <a name="Rebecq16bmvc"></a>Rebecq, H., Gallego, G., Scaramuzza, D.,  
*[EMVS: Event-based Multi-View Stereo](http://www.bmva.org/bmvc/2016/papers/paper063/)*,  
British Machine Vision Conf. (BMVC), 2016. [PDF](http://rpg.ifi.uzh.ch/docs/BMVC16_Rebecq.pdf), [YouTube](https://www.youtube.com/watch?v=EUX3Tfx0KKE), [3D Reconstruction Experiments from a Train using an Event Camera](https://www.youtube.com/watch?v=fA4MiSzYHWA), [Code](https://github.com/uzh-rpg/rpg_emvs).
- [Kim et. al. ECCV 2016](#Kim16eccv),  
*Real-Time 3D Reconstruction and 6-DoF Tracking with an Event Camera*.
- <a name="Gallego18cvpr"></a>Gallego, G., Rebecq, H., Scaramuzza, D.,  
*[A Unifying Contrast Maximization Framework for Event Cameras, with Applications to Motion, Depth and Optical Flow Estimation](https://arxiv.org/pdf/1804.01306)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2018. [PDF](http://rpg.ifi.uzh.ch/docs/CVPR18_Gallego.pdf),  [Poster](http://rpg.ifi.uzh.ch/docs/CVPR18_Gallego_poster.pdf),  [YouTube](https://youtu.be/KFMZFhi-9Aw),  [Spotlight presentation](https://youtu.be/IOntXI5iRzA).
- <a name="Haessig19srep"></a>Haessig, G., Berthelon, X., Ieng, S.-H., Benosman, R.,  
[A Spiking Neural Network Model of Depth from Defocus for Event-based Neuromorphic Vision](https://doi.org/10.1038/s41598-019-40064-0),  
Scientific Reports 9, Article number: 3744 (2019). [PDF](https://www.neuromorphic-vision.com/public/publications/55/publication.pdf)
- <a name="Gallego19cvpr"></a>Gallego, G., Gehrig, M., Scaramuzza, D.,  
*[Focus Is All You Need: Loss Functions For Event-based Vision](http://rpg.ifi.uzh.ch/docs/CVPR19_Gallego.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2019. [PDF arXiv](https://arxiv.org/pdf/1904.07235), [Poster](http://rpg.ifi.uzh.ch/docs/CVPR19_Gallego_poster.pdf), [YouTube](https://youtu.be/SU_Fp4xS_g4?t=1059)
- <a name="Chaney19cvprw"></a>Chaney, K., Zhu, A., Daniilidis, K.,  
*[Learning Event-based Height from Plane and Parallax](https://doi.org/10.1109/IROS40897.2019.8968223)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2019. [PDF](http://openaccess.thecvf.com/content_CVPRW_2019/papers/EventVision/Chaney_Learning_Event-Based_Height_From_Plane_and_Parallax_CVPRW_2019_paper.pdf), [Video pitch](https://youtu.be/S1OLnbnB_qo),  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2019.
- [Zhu et. al. CVPR 2019](#Zhu19cvpr),  
*Unsupervised Event-Based Learning of Optical Flow, Depth, and Egomotion.*

<a name="depth-mono-active"></a>
### Monocular Depth Estimation using Structured Light
- <a name="Brandli14fnins"></a>Brandli, C., Mantel, T.A., Hutter, M., Hoepflinger, M.A., Berner, R., Siegwart, R., Delbruck, T.,  
*[Adaptive Pulsed Laser Line Extraction for Terrain Reconstruction using a Dynamic Vision Sensor](https://doi.org/10.3389/fnins.2013.00275)*,  
Front. Neurosci. (2014), 7:275. [PDF](http://www.zora.uzh.ch/107736/1/fnins-07-00275.pdf), [YouTube](https://youtu.be/20OGD5Wwe9Q)
- <a name="Matsuda15iccp"></a>Matsuda, N., Cossairt, O., Gupta, M.,  
*[MC3D: Motion Contrast 3D Scanning](https://doi.org/10.1109/ICCPHOT.2015.7168370)*,  
IEEE Conf. Computational Photography (ICCP), 2015. [PDF](http://compphotolab.northwestern.edu/wordpress/wp-content/uploads/2015/04/dvs_031.pdf), [YouTube](https://youtu.be/m7qOEsTyVwU), [Project page](http://compphotolab.northwestern.edu/project/mc3d-motion-contrast-3d-laser-scanner/)
- <a name="Leroux18arxiv"></a>Leroux, T., Ieng, S.-H., Benosman, R.,  
*[Event-Based Structured Light for Depth Reconstruction using Frequency Tagged Light Patterns](https://arxiv.org/pdf/1811.10771)*,  
arXiv:1811.10771, 2018.

<a name="depth-stereo"></a>
### Stereo Depth Estimation
- <a name="Schraml07visapp"></a>Schraml, C., Schon, P., Milosevic, N.,  
*[Smartcam for real-time stereo vision - address-event based embedded system](http://doi.org/10.5220/0002057604660471)*,  
Int. Conf. Computer Vision Theory and Applications (VISAPP), 2007, pp. 466-471.
    - <a name="Schraml10iscas"></a>Schraml, S., Belbachir, A. N., Milosevic, N., Schon, P.,  
*[Dynamic stereo vision system for real-time tracking](https://doi.org/10.1109/ISCAS.2010.5537289)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2010.
    - <a name="Schraml10cvprw"></a>Schraml, S., Belbachir, A. N.,  
*[A spatio-temporal clustering method using real-time motion analysis on event-based 3D vision](https://doi.org/10.1109/CVPRW.2010.5543810)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2010. [PDF](http://www.belbachir.info/PDF/cvpr1_2010.pdf)
    - <a name="Schraml10cvprw2"></a>Schraml, S., Belbachir, A. N., Braendle, N.,  
*[A Real-time Pedestrian Classification Method for Event-based Dynamic Stereo Vision](https://doi.org/10.1109/CVPRW.2010.5543775)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2010. [PDF](http://www.belbachir.info/PDF/cvpr2_2010.pdf)
    - <a name="Schraml10cvprw3"></a>Schraml, S., Belbachir, A. N., Braendle, N.,  
*[Real-time classification of pedestrians and cyclists for intelligent counting of non-motorized traffic](https://doi.org/10.1109/CVPRW.2010.5543170)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2010. [PDF](http://www.belbachir.info/PDF/cvpr3_2010.pdf)
- <a name="Kogler09icvs"></a>Kogler, J., Sulzbachner, C., Kubinger, W.,  
*[Bio-inspired stereo vision system with silicon retina imagers](https://doi.org/10.1007/978-3-642-04667-4_18)*,  
Int. Conf. Computer Vision Systems (ICVS), 2009.
    - <a name="Kogler11icvs"></a>Kogler, J., Humenberger, M., Sulzbachner, C.,  
*[Event-Based Stereo Matching Approaches for Frameless Address Event Stereo Data](http://doi.org/10.1007/978-3-642-24028-7_62)*,  
Int. Symp. Visual Computing (ISVC) 2011, Advances in Visual Computing, pp. 674-685.
    - <a name="Kogler11atasc"></a>Kogler, J., Sulzbachner, C., Humenberger, M., Eibensteiner, F.,  
*[Address-Event Based Stereo Vision with Bio-Inspired Silicon Retina Imagers](http://doi.org/10.5772/12941)*,  
Advances in Theory and Applications of Stereo Vision (2011), pp. 165-188.
    - [Kogler, J., Ph.D. Thesis 2016](#Kogler16PhD),  
*Design and evaluation of stereo matching techniques for silicon retina cameras*.
- <a name="Kogler10scce"></a>Kogler, J., Sulzbachner, C., Eibensteiner, F., Humenberger, M.,  
*[Address-Event Matching for a Silicon Retina based Stereoo Vision System](https://pdfs.semanticscholar.org/2a76/ebed789fdca9dc9e40dc412f6bba3cfa3ef2.pdf)*,  
Int. Conf. from Scientific Computing to Computational Engineering (IC-SCCE), 2010.
    - <a name="Sulzbachner10elmar"></a>Sulzbachner, C., Kogler, J., Eibensteiner, F.,  
*[A novel verification approach for silicon retina stereo matching](https://ieeexplore.ieee.org/abstract/document/5606120)*,  
IEEE Int. Symp. Electronics in Marine (ELMAR), 2010.
    - <a name="Sulzbachner11cvprw"></a>Sulzbachner, C., Zinner, C., Kogler, J.,  
*[An optimized silicon retina stereo matching algorithm using time-space correlation](https://doi.org/10.1109/CVPRW.2011.5981722)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2011. [PDF](http://encevis.de/documents/Paper/2011_06_20-25.pdf)
    - <a name="Eibensteiner11eurocast"></a>Eibensteiner, F., Kogler, J., Sulzbachner, C., Scharinger, J.,  
*[Stereo-Vision Algorithm Based on Bio-Inspired Silicon Retinas for Implementation in Hardware](https://doi.org/10.1007/978-3-642-27549-4_80)*,  
Int. Conf. Computer Aided Systems Theory EUROCAST, LNCS, pp. 624–631, 2011.
    - <a name="Eibensteiner14cvprw"></a>Eibensteiner, F., Kogler, J., Scharinger, J.,  
*[A High-Performance Hardware Architecture for a Frameless Stereo Vision Algorithm Implemented on a FPGA Platform](https://doi.org/10.1109/CVPRW.2014.97)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2014. [PDF](http://openaccess.thecvf.com/content_cvpr_workshops_2014/W17/papers/Eibensteiner_A_High-Performance_Hardware_2014_CVPR_paper.pdf)
    - <a name="Eibensteiner17radio"></a>Eibensteiner, F., Brachtendorf, H. G., Scharinger, J.,  
*[Event-driven stereo vision algorithm based on silicon retina sensors](http://doi.org/10.1109/RADIOELEK.2017.7937602)*,  
27th Int. Conf. Radioelektronika, 2017.
- <a name="Belbachir11cvprw"></a>Belbachir, A.N., Schraml, S., Nowakoska, A.,  
*[Event-Driven Stereo Vision for Fall Detection](https://doi.org/10.1109/CVPRW.2011.5981819)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2011.
    - <a name="Belbachir11iccvw"></a>Belbachir, A.N., Nowakoska, A., Schraml, S., Wiesmann, G., Sablatnig, R.,  
*[Event-Driven Feature Analysis in a 4D Spatiotemporal Representation](https://doi.org/10.1109/ICCVW.2011.6130437)*,  
IEEE Int. Conf. Computer Vision Workshops (ICCVW), 2011.
    - <a name="Belbachir12iscas"></a>Belbachir, A.N., Litzenberger, M., Schraml, S., Hofstätter, M., Bauer, D., Schön, P., Humenberger, M., Sulzbachner, C., Lunden, T., Merne, M.,  
*[CARE: A dynamic stereo vision sensor system for fall detection](https://doi.org/10.1109/ISCAS.2012.6272141)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2012.
    - <a name="Humenberger12cvprw"></a>Humenberger, M., Schraml, S., Sulzbachner, C., Belbachir, A.N., Srp A., Vajda, F.,  
*[Embedded Fall Detection with a Neural Network and Bio-inspired Stereo Vision](https://doi.org/10.1109/CVPRW.2012.6238896)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2012.
- <a name="Benosman11tnn"></a>Benosman, R., Ieng, S. H., Rogister, P., Posch, C.,  
*[Asynchronous Event-Based Hebbian Epipolar Geometry](https://doi.org/10.1109/TNN.2011.2167239)*,  
IEEE Trans. Neural Netw., 22(11):1723-1734, 2011. [PDF](https://www.neuromorphic-vision.com/public/publications/10/publication.pdf)
- <a name="Rogister12tnnls"></a>Rogister, P. , Benosman, R., Ieng, S.-H., Lichtsteiner, P., Delbruck, T.,  
*[Asynchronous Event-Based Binocular Stereo Matching](https://doi.org/10.1109/TNNLS.2011.2180025)*,  
IEEE Trans. Neural Netw. Learn. Syst. (TNNLS), 23(2):347-353, 2012. [PDF](https://www.neuromorphic-vision.com/public/publications/16/publication.pdf)
- <a name="Carneiro13neunet"></a>Carneiro, J., Ieng, S.-H., Posch, C., Benosman, R.,  
*[Event-based 3D reconstruction from neuromorphic retinas](https://doi.org/10.1016/j.neunet.2013.03.006)*,  
Neural Networks (2013), 45:27-38. [PDF](https://www.neuromorphic-vision.com/public/publications/5/publication.pdf)
    - [Carneiro, Ph.D. Thesis, 2014](#Carneiro14PhD),  
*Asynchronous Event-Based 3D Vision*.
- [Lee et. al., TNNLS 2014](#Lee14tnnls)
- <a name="Piatkowska14mst"></a>Piatkowska, E., Belbachir, A. N., Gelautz, M.,  
*[Cooperative and asynchronous stereo vision for dynamic vision sensors](http://dx.doi.org/10.1088/0957-0233/25/5/055108)*,  
Meas. Sci. Technol. (2014), 25(5).
    - <a name="Piatkowska13iccvw"></a>Piatkowska, E., Belbachir, A. N., Gelautz, M.,  
*[Asynchronous Stereo Vision for Event-Driven Dynamic Stereo Sensor Using an Adaptive Cooperative Approach](https://doi.org/10.1109/ICCVW.2013.13)*,  
IEEE Int. Conf. Computer Vision Workshops (ICCVW), 2013.
    - <a name="Piatkowska17cvprw"></a>Piatkowska, E., Kogler, J., Belbachir, A. N., Gelautz, M.,  
*[Improved Cooperative Stereo Matching for Dynamic Vision Sensors with Ground Truth Evaluation](http://doi.org/10.1109/CVPRW.2017.51)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2017, pp. 370-377. [PDF](http://openaccess.thecvf.com/content_cvpr_2017_workshops/w4/papers/Piatkowska_Improved_Cooperative_Stereo_CVPR_2017_paper.pdf).
- <a name="Camunas14fnins"></a>Camuñas-Mesa, L. A., Serrano-Gotarredona, T., Ieng, S. H., Benosman, R. B., Linares-Barranco, B.,  
*[On the use of orientation filters for 3D reconstruction in event–driven stereo vision](https://doi.org/10.3389/fnins.2014.00048)*,  
Front. Neurosci. (2014), 8:48. [PDF](https://www.neuromorphic-vision.com/public/publications/29/publication.pdf)
    - <a name="Camunas14iscas"></a>Camuñas-Mesa, L. A., Serrano-Gotarredona, T., Linares-Barranco, B., Ieng, S., Benosman, R.,  
*[Event-Driven Stereo Vision with Orientation Filters](https://doi.org/10.1109/ISCAS.2014.6865114)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2014.
- <a name="Kogler14jei"></a>Kogler, J., Eibensteiner, F., Humenberger, M., Sulzbachner, C., Gelautz, M., Scharinger, J.,  
*[Enhancement of sparse silicon retina-based stereo matching using belief propagation and two-stage postfiltering](https://doi.org/10.1117/1.JEI.23.4.043011)*,  
J. Electronic Imaging, 23(4), 043011 (2014).
    - [Kogler, J., Ph.D. Thesis 2016](#Kogler16PhD),  
*Design and evaluation of stereo matching techniques for silicon retina cameras*.
- <a name="Firouzi16npl"></a>Firouzi, M. and Conradt, J.,  
*[Asynchronous Event-based Cooperative Stereo Matching Using Neuromorphic Silicon Retinas](http://doi.org/10.1007/s11063-015-9434-5),*  
Neural Processing Letters, 43(2):311-326, Apr. 2016. [PDF](https://mediatum.ub.tum.de/doc/1254531/131347.pdf)
    - <a name="Dikov17lmlncs"></a>Dikov, G., Firouzi, M., Röhrbein, F., Conradt, J., Richter, C.,  
*[Spiking Cooperative Stereo-Matching at 2 ms Latency with Neuromorphic Hardware](https://doi.org/10.1007/978-3-319-63537-8_11)*,  
Conf. Biomimetic and Biohybrid Systems. Living Machines 2017: Biomimetic and Biohybrid Systems, pp. 119-137. LNCS, vol 10384. Springer, Cham.  [PDF](https://www.researchgate.net/publication/318449954_Spiking_Cooperative_Stereo-Matching_at_2_ms_Latency_with_Neuromorphic_Hardware),  [Videos](https://figshare.com/s/0d9fb146149b832ed8ec)
    - <a name="Kaiser18icann"></a>Kaiser, J., Weinland, J., Keller, P., Steffen, L., Vasquez Tieck, J.C., Reichard, D., Roennau, A., Conradt, J., Dillmann, R.,  
*[Microsaccades for Neuromorphic Stereo Vision](https://doi.org/10.1007/978-3-030-01418-6_24)*,  
Int. Conf. Artificial Neural Networks (ICANN), 2018.
- <a name="Zou16icip"></a>Zou, D., Guo, P., Wang, Q., Wang, X., Shao, G., Shi, F., Li, J., Park, P.K.J.,  
*[Context-Aware Event-driven Stereo Matching](https://doi.org/10.1109/ICIP.2016.7532523)*,  
IEEE Int. Conf. Image Processing (ICIP), 2016.
- [Kaelber, F., Bachelor Thesis 2016](#Kaelber16BS),  
*A probabilistic method for event stream registration*.
- [Galanis, M., Bachelor Thesis 2016](#Galanis16BS),  
*DVS event stream registration*.
- <a name="Osswald17srep"></a>Osswald, M., Ieng, S.-H., Benosman, R., Indiveri, G.,  
*[A spiking neural network model of 3D perception for event-based neuromorphic stereo vision systems](http://doi.org/10.1038/srep40703)*,  
Scientific Reports 7, Article number: 40703 (2017). [PDF](https://www.neuromorphic-vision.com/public/publications/44/publication.pdf)
    - [Haessig et al., AICAS 2019](#Haessig19aicas),  
*Neuromorphic networks on the SpiNNaker platform*.
- <a name="Zou17bmvc"></a>Zou, D., Shi, F., Liu, W., Li, J., Wang, Q., Park, P.K.J., Shi, C.-W., Roh, Y.J., Ryu, H.,  
*[Robust Dense Depth Map Estimation from Sparse DVS Stereos](https://www.dropbox.com/s/ee6dn8zy4odpfwl/0096.pdf?dl=1)*,  
British Machine Vision Conf. (BMVC), 2017. [Supp. Material](https://www.dropbox.com/s/eztqo109iue6ned/Active%20Papers%20Paper%2096%20%20Supplementary%20File.zip?dl=1).
- Camuñas-Mesa, L. A., Serrano-Gotarredona, T., Ieng, S., Benosman, R., Linares-Barranco, B.,  
*[Event-driven Stereo Visual Tracking Algorithm to Solve Object Occlusion](https://doi.org/10.1109/TNNLS.2017.2759326)*,  
IEEE Trans. Neural Netw. Learn. Syst. (TNNLS), 2017.
- <a name="Xie17fnins"></a>Xie, Z., Chen, S., Orchard, G.  
*[Event-Based Stereo Depth Estimation Using Belief Propagation](https://doi.org/10.3389/fnins.2017.00535)*,  
Front. Neurosci. (2017), 11:535.  [YouTube](https://youtu.be/ngJpY1lcbdw)
- <a name="Andreopoulos18cvpr"></a>Andreopoulos, A., Kashyap, H.J., Nayak, T.K., Amir, A., Flickner, M.D.,  
*[A Low Power, High Throughput, Fully Event-Based Stereo System](http://openaccess.thecvf.com/content_cvpr_2018/papers/Andreopoulos_A_Low_Power_CVPR_2018_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2018.
    - [Stereo Dataset](https://ibm.ent.box.com/s/3hiq58ww1pbbjrinh367ykfdf60xsfm8).
- <a name="Ieng18fnins"></a>Ieng, S.-H., Carneiro, J., Osswald, M., Benosman, R.,  
*[Neuromorphic Event-Based Generalized Time-Based Stereovision](https://doi.org/10.3389/fnins.2018.00442)*,  
Front. Neurosci. (2018), 12:442.
    - [Carneiro, Ph.D. Thesis, 2014](#Carneiro14PhD),  
*Asynchronous Event-Based 3D Vision - Chapter 4*.
- <a name="Zhu18eccv"></a>Zhu, A., Chen, Y., Daniilidis, K.,  
*[Realtime Time Synchronized Event-based Stereo](https://arxiv.org/abs/1803.09025)*,  
European Conf. Computer Vision (ECCV), 2018. [YouTube](https://youtu.be/4oa7e4hsrYo)
- <a name="Zhou18eccv"></a>Zhou, Y., Gallego, G., Rebecq, H., Kneip, L., Li, H., Scaramuzza, D.,  
*[Semi-Dense 3D Reconstruction with a Stereo Event Camera](http://rpg.ifi.uzh.ch/docs/ECCV18_Zhou.pdf)*,  
European Conf. Computer Vision (ECCV), 2018. [Poster](http://rpg.ifi.uzh.ch/docs/ECCV18_Zhou_poster.pdf),  [YouTube](https://youtu.be/Qrnpj2FD1e4).
- <a name="DominguezMorales19electr"></a>Dominguez-Morales, M., Dominguez-Morales, J. P., Jimenez-Fernandez, A., Linares-Barranco, A., Jimenez-Moreno, G.,  
*[Stereo Matching in Address-Event-Representation (AER) Bio-Inspired Binocular Systems in a Field-Programmable Gate Array (FPGA)](https://doi.org/10.3390/electronics8040410)*,  
Electronics 2019, 8(4), 410.
- <a name="Steffen19fnbot"></a>Steffen, L., Reichard, D., Weinland, J., Kaiser, J., Roennau, A., Dillmann, R.,  
*[Neuromorphic Stereo Vision: A Survey of Bio-Inspired Sensors and Algorithms](https://doi.org/10.3389/fnbot.2019.00028)*,  
Front. Neurorobot. (2019) 13:28.
- <a name="Steffen19case"></a>Steffen, L., Hauck, B., Kaiser, J., Weinland, J., Ulbrich, S., Reichard, D., Roennau, A., Dillmann, R.,  
*[Creating an Obstacle Memory Through Event-Based Stereo Vision and Robotic Proprioception](https://doi.org/10.1109/COASE.2019.8843238)*,  
IEEE Int. Conf. Automation Science and Engineering (CASE), 2019.
- <a name="Hadviger19ecmr"></a>Hadviger, A., Markovic, I., Petrovic, I.,  
*[Stereo Event Lifetime and Disparity Estimation for Dynamic Vision Sensors](https://arxiv.org/pdf/1907.07518)*,  
European Conf. Mobile Robots (ECMR), 2019. [PDF arXiv](https://arxiv.org/pdf/1907.07518).
- <a name="Tulyakov19iccv"></a>Tulyakov, S., Fleuret, F., Kiefel, M., Gehler, P., Hirsch., M.,  
*[Learning an event sequence embedding for dense event-based deep stereo](https://www.idiap.ch/~fleuret/papers/tulyakov-et-al-iccv2019.pdf)*,  
IEEE Int. Conf. Computer Vision (ICCV), 2019.
- <a name="Steffen19icar"></a>Steffen, L., Ulbrich, S., Roennau, A., Dillmann, R.,  
*[Multi-View 3D Reconstruction With Self-Organizing Maps on Event-Based Data](https://doi.org/10.1109/ICAR46387.2019.8981569)*,  
IEEE Int. Conf. Advanced Robotics (ICAR), 2019.

<a name="depth-stereo-active"></a>
### Stereo Depth Estimation using Structured Light
- <a name="Martel18iscas"></a>Martel, J.N.P., Mueller, J., Conradt, J., Sandamirskaya, Y.,  
*[An Active Approach to Solving the Stereo Matching Problem using Event-Based Sensors](http://dx.doi.org/10.1109/ISCAS.2018.8351411)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2018.
    - <a name="Martel18iscas"></a>Martel, J.N.P., Müller, J., Conradt, J., Sandamirskaya, Y.,  
*[Live Demonstration: An Active System for Depth Reconstruction using Event-Based Sensors](https://doi.org/10.1109/ISCAS.2018.8351861)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2018.

<a name="depth-stereo-pano"></a>
### Stereoscopic Panoramic Imaging
- <a name="TUCO14ait"></a>[smart eye TUCO-3D camera](https://www.ait.ac.at/fileadmin/mc/digital_safety_security/downloads/Factsheet_-_Panoramic-Imaging-Sensor_en.pdf),  
Stereoscopic panoramic imaging camera based on dynamic vision sensors. [PDF](https://www.ait.ac.at/fileadmin/mc/digital_safety_security/downloads/TUCO-3D_Vision2014.pdf)
- <a name="Belbachir10icdsc"></a>Belbachir, A. N., Pflugfelder, R., Gmeiner, P.,  
*[A Neuromorphic Smart Camera for Real-time 360deg distortion-free Panoramas](https://doi.org/10.1145/1865987.1866022)*,  
IEEE Conference on Distributed Smart Cameras (ICDSC), 2010. [PDF](http://www.belbachir.info/PDF/icdsc2010.pdf)
- <a name="Belbachir12iscas2"></a>Belbachir, A.N., Mayerhofer, M., Matolin, D., Colineau, J.,  
*[Real-time 360 degrees Panoramic Views using BiCa360, the Fast Rotating Dynamic Vision Sensor to up to 10 Rotations per Sec](https://doi.org/10.1109/ISCAS.2012.6272139)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2012.
- <a name="Belbachir12icdsc"></a>Belbachir, A.N., Mayerhofer, M., Matolin, D., Colineau, J.,  
*[360SCAN: High-speed rotating line sensor for real-time 360 degrees panoramic vision](https://ieeexplore.ieee.org/document/6470127)*,  
IEEE Int. Conf. Distributed Smart Cameras (ICDSC), 2012.
- <a name="Belbachir14cvprw"></a>Belbachir, A. N., Schraml, S., Mayerhofer, M., Hofstatter, M.,  
*[A Novel HDR Depth Camera for Real-time 3D 360-degree Panoramic Vision](https://doi.org/10.1109/CVPRW.2014.69)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2014, pp. 419-426. [PDF](http://www.cv-foundation.org/openaccess/content_cvpr_workshops_2014/W13/papers/Belbachir_A_Novel_HDR_2014_CVPR_paper.pdf)
- <a name="Schraml15cvpr"></a>Schraml, S., Belbachir, A. N., Bischof, H.,  
*[Event-Driven Stereo Matching for Real-Time 3D Panoramic Vision](https://doi.org/10.1109/CVPR.2015.7298644)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2015, pp. 466-474. [PDF](http://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Schraml_Event-Driven_Stereo_Matching_2015_CVPR_paper.pdf). [Slides](https://www.anyline.io/wp-content/uploads/2016/03/event-driven-stereo-for-3d-360deg-panoramic-vision.pdf).
- <a name="Schraml16tie"></a>Schraml, S., Belbachir, A. N., Bischof, H.,  
*[An Event-Driven Stereo System for Real-Time 3-D 360° Panoramic Vision](https://doi.org/10.1109/TIE.2015.2477265)*,  
IEEE Trans. Ind. Electron., 63(1):418-428, 2016.


<a name="slam"></a>
## SLAM (Simultaneous Localization And Mapping)

<a name="slam-localization"></a>
### Localization, Ego-Motion Estimation
- <a name="Weikersdorfer12robio"></a>Weikersdorfer, D. and Conradt, J.,  
*[Event-based particle filtering for robot self-localization](http://doi.org/10.1109/ROBIO.2012.6491077)*,  
IEEE Int. Conf. Robotics and Biomimetics (ROBIO), 2012. [PDF](https://mediatum.ub.tum.de/doc/1215541/835468.pdf)
- <a name="Censi13iros"></a>Censi, A., Strubel, J., Brandli, C., Delbruck, T., Scaramuzza, D.,  
*[Low-latency localization by Active LED Markers tracking using a Dynamic Vision Sensor](https://doi.org/10.1109/IROS.2013.6696456)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2013. [PDF](http://rpg.ifi.uzh.ch/docs/IROS13_Censi.pdf), [Slides](http://rpg.ifi.uzh.ch/docs/IROS13_Censi.ppt)
- <a name="Mueggler14iros"></a>Mueggler, E., Huber, B., Scaramuzza, D.,  
*[Event-based, 6-DOF Pose Tracking for High-Speed Maneuvers](https://doi.org/10.1109/IROS.2014.6942940)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Chicago, IL, 2014, pp. 2761-2768. [PDF](http://rpg.ifi.uzh.ch/docs/IROS14_Mueggler.pdf), [YouTube](https://youtu.be/LauQ6LWTkxM)
- <a name="Gallego15arxiv"></a>Gallego, G., Forster, C., Mueggler, E., Scaramuzza, D.,  
*[Event-based Camera Pose Tracking using a Generative Event Model](https://arxiv.org/pdf/1510.01972)*,  
arXiv:1510.01972, 2015.
- <a name="Mueggler15rss"></a>Mueggler, E., Gallego G., Scaramuzza, D.,   
*[Continuous-Time Trajectory Estimation for Event-based Vision Sensors](http://dx.doi.org/10.15607/RSS.2015.XI.036)*,  
Robotics: Science and Systems (RSS), 2015. [PDF](http://rpg.ifi.uzh.ch/docs/RSS15_Mueggler.pdf), [PPT](http://rpg.ifi.uzh.ch/docs/RSS15_Mueggler.pptm),  [Poster](http://rpg.ifi.uzh.ch/docs/RSS15_Mueggler_poster.pdf)
- <a name="Reverter16fnins"></a>Reverter Valeiras, D., Orchard, G., Ieng, S.-H., Benosman, R.,  
*[Neuromorphic Event-Based 3D Pose Estimation](https://doi.org/10.3389/fnins.2015.00522)*.  
Front. Neurosci. (2016), 9:522. [PDF](https://www.neuromorphic-vision.com/public/publications/24/publication.pdf), [Suppl. Mat.](https://www.neuromorphic-vision.com/public/publications/24/supplementaryMaterial.zip)
- <a name="Reverter16fninsb"></a>Reverter Valeiras, D., Kime, S., Ieng, S.-H., Benosman, R.,  
*[An Event-Based Solution to the Perspective-n-Point Problem](https://doi.org/10.3389/fnins.2016.00208)*.  
Front. Neurosci. (2016), 10:208. [PDF](https://www.neuromorphic-vision.com/public/publications/25/publication.pdf), [Suppl. Mat.](https://www.neuromorphic-vision.com/public/publications/25/supplementaryMaterial.zip)
- [Mueggler et. al. IJRR 2017](#Mueggler17ijrr).  
*The Event-Camera Dataset and Simulator: Event-based Data for Pose Estimation, Visual Odometry, and SLAM.*
- <a name="Gallego18tpami"></a>Gallego, G., Lund, J.E.A., Mueggler, E., Rebecq, H., Delbruck, T., Scaramuzza, D.,  
*[Event-based, 6-DOF Camera Tracking from Photometric Depth Maps](http://dx.doi.org/10.1109/TPAMI.2017.2769655)*,  
IEEE Trans. Pattern Anal. Machine Intell. (TPAMI), 2018. [PDF](http://rpg.ifi.uzh.ch/docs/PAMI17_Gallego.pdf),  [YouTube](https://youtu.be/iZZ77F-hwzs?t=5), [Datasets](http://rpg.ifi.uzh.ch/direct_event_camera_tracking/index.html)
- <a name="Nguyen19cvprw"></a>Nguyen, A., Do, T.-T., Caldwell, D. G., Tsagarakis, N. G.,  
*[Real-Time 6DOF Pose Relocalization for Event Cameras with Stacked Spatial LSTM Networks](http://openaccess.thecvf.com/content_CVPRW_2019/papers/EventVision/Nguyen_Real-Time_6DOF_Pose_Relocalization_for_Event_Cameras_With_Stacked_Spatial_CVPRW_2019_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2019. [PDF](https://arxiv.org/abs/1708.09011). [Project page](https://github.com/nqanh/pose_relocalization). [Video pitch](https://youtu.be/Bwmmt7dqTIw)
- [Maqueda et. al. CVPR 2018](#Maqueda18cvpr).  
*Event-based Vision meets Deep Learning on Steering Prediction for Self-driving Cars.*
- [Gallego et. al. CVPR 2018](#Gallego18cvpr),  
*A Unifying Contrast Maximization Framework for Event Cameras, with Applications to Motion, Depth and Optical Flow Estimation*.
- <a name="Bryner19icra"></a>Bryner, S., Gallego, G., Rebecq, H., Scaramuzza, D.,  
*[Event-based, Direct Camera Tracking from a Photometric 3D Map using Nonlinear Optimization](http://rpg.ifi.uzh.ch/docs/ICRA19_Bryner.pdf)*,  
IEEE Int. Conf. Robotics and Automation (ICRA), 2019. [PDF](http://rpg.ifi.uzh.ch/docs/ICRA19_Bryner.pdf), [YouTube](https://youtu.be/ISgXVgCR-lE), [Project page and Datasets](http://rpg.ifi.uzh.ch/direct_event_camera_tracking/index.html)
- [Gallego et. al. CVPR 2019](#Gallego19cvpr),  
*Focus Is All You Need: Loss Functions For Event-based Vision*.
- [Zhu et. al. CVPR 2019](#Zhu19cvpr),  
*Unsupervised Event-Based Learning of Optical Flow, Depth, and Egomotion.*
- <a name="Xu20tci"></a>Xu, J., Jiang, M., Yu, L., Yang, W., Wang, W.,  
*[Robust Motion Compensation for Event Cameras With Smooth Constraint](http://dx.doi.org/10.1109/TCI.2020.2964255)*,  
IEEE Trans. Comput. Imag. (TCI), 6:604-614, 2020.


<a name="slam-mapping"></a>
### Mapping
- See [Depth Estimation (3D Reconstruction)](#depth-estimation)

<a name="visual-odometry"></a>
### Visual Odometry / SLAM
- [Cook et. al. IJCNN 2011](#Cook11ijcnn),  
*Interacting maps for fast visual interpretation*. (Joint estimation of optical flow, image intensity and angular velocity with a rotating event camera).
- <a name="Weikersdorfer13icvs"></a>Weikersdorfer, D., Hoffmann, R., Conradt. J.,  
*[Simultaneous localization and mapping for event-based vision systems](http://doi.org/10.1007/978-3-642-39402-7_14)*.  
Int. Conf. Computer Vision Systems (ICVS), 2013, pp. 133-142. [PDF](https://mediatum.ub.tum.de/doc/1191908/271955.pdf), [Slides](http://workshops.acin.tuwien.ac.at/ICVS/downloads/ICVS2013-ebslam_weikersdorfer.pdf)
- [Kim et al., BMVC 2014](#Kim14bmvc),  
*Simultaneous Mosaicing and Tracking with an Event Camera*.
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
- <a name="Gallego17ral"></a>Gallego, G. and Scaramuzza, D.,  
*[Accurate Angular Velocity Estimation with an Event Camera](https://doi.org/10.1109/LRA.2016.2647639)*,  
IEEE Robotics and Automation Letters (RA-L), 2(2):632-639, 2017.
[PDF](http://rpg.ifi.uzh.ch/docs/RAL16_Gallego.pdf),  [PPT](http://rpg.ifi.uzh.ch/docs/RAL16_Gallego.pptx),  [Youtube](https://youtu.be/v1sXWoOAs_0).
- <a name="Rebecq17ral"></a>Rebecq, H., Horstschaefer, T., Gallego, G., Scaramuzza, D.,  
*[EVO: A Geometric Approach to Event-based 6-DOF Parallel Tracking and Mapping in Real-time](https://doi.org/10.1109/LRA.2016.2645143)*,  
IEEE Robotics and Automation Letters (RA-L), 2(2):593-600, 2017. [PDF](http://rpg.ifi.uzh.ch/docs/RAL16_EVO.pdf),  [PPT](http://rpg.ifi.uzh.ch/docs/ICRA17_EVO.pptx),  [Poster](http://rpg.ifi.uzh.ch/docs/RAL16_EVO_poster.pdf),  [Youtube](https://youtu.be/bYqD2qZJlxE).
- <a name="Reinbacher17iccp"></a>Reinbacher, C., Munda, G., Pock, T.,  
*[Real-Time Panoramic Tracking for Event Cameras](https://doi.org/10.1109/ICCPHOT.2017.7951488)*,  
IEEE Int. Conf. Computational Photography (ICCP), 2017. [PDF](https://arxiv.org/abs/1703.05161), [YouTube](https://youtu.be/Qy0brSlirmk), [Code](https://github.com/VLOGroup/dvs-panotracking)
- [Mueggler et. al. IJRR 2017](#Mueggler17ijrr).  
*The Event-Camera Dataset and Simulator: Event-based Data for Pose Estimation, Visual Odometry, and SLAM.*
- <a name="ZhuD19robio"></a>Zhu, D., Dong, J., Xu, Z., Ye, C., Hu, Y., Su, H., Liu, Z., Chen, G.,  
*[Neuromorphic Visual Odometry System for Intelligent Vehicle Application with Bio-inspired Vision Sensor](https://doi.org/10.1109/ROBIO49542.2019.8961878)*,  
IEEE Int. Conf. Robotics and Biomimetics (ROBIO), 2019. [PDF](https://arxiv.org/pdf/1909.02490)
- <a name="Park19iedm"></a>Park, P.K.J., Kim, J.-S., Shin, C.-W, Lee, H., Liu, W., Wang, Q., Roh, Y., Kim, J., Ater, Y., Soloveichik, E., Ryu, H. E.,  
*[Low-Latency Interactive Sensing for Machine Vision](https://doi.org/10.1109/IEDM19573.2019.8993468)*,  
IEEE Int. Electron Devices Meeting (IEDM), 2019.
- <a name="Liu20arxiv"></a>Liu. D., Parra, A., Chin, T.-J.,  
*[Globally Optimal Contrast Maximisation for Event-based Motion Estimation](https://arxiv.org/pdf/2002.10686)*,  
arXiv, 2020.


<a name="visual-inertial"></a>
### Visual-Inertial Odometry
- <a name="Mueggler18tro"></a>Mueggler, E., Gallego, G., Rebecq, H., Scaramuzza, D.,  
*[Continuous-Time Visual-Inertial Odometry for Event Cameras](http://rpg.ifi.uzh.ch/docs/TRO18_Mueggler.pdf)*,  
IEEE Trans. Robot., 2018.
- [Mueggler et. al. IJRR 2017](#Mueggler17ijrr).  
*The Event-Camera Dataset and Simulator: Event-based Data for Pose Estimation, Visual Odometry, and SLAM.*
- <a name="Zhu17cvpr"></a>Zhu, A., Atanasov, N., Daniilidis, K.,  
*[Event-based Visual Inertial Odometry](https://doi.org/10.1109/CVPR.2017.616)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2017. [PDF](http://openaccess.thecvf.com/content_cvpr_2017/papers/Zhu_Event-Based_Visual_Inertial_CVPR_2017_paper.pdf), [Supplementary material](http://openaccess.thecvf.com/content_cvpr_2017/supplemental/Zhu_Event-Based_Visual_Inertial_2017_CVPR_supplemental.zip), [YouTube](https://youtu.be/9zGoR67l9Wc).
- <a name="Rebecq17bmvc"></a>Rebecq, H., Horstschaefer, T., Scaramuzza, D.,  
*[Real-time Visual-Inertial Odometry for Event Cameras using Keyframe-based Nonlinear Optimization](http://rpg.ifi.uzh.ch/docs/BMVC17_Rebecq.pdf)*,  
British Machine Vision Conf. (BMVC), 2017. [PDF](http://rpg.ifi.uzh.ch/docs/BMVC17_Rebecq.pdf), [Appendix](http://rpg.ifi.uzh.ch/docs/BMVC17_Rebecq_appendix.pdf), [YouTube](https://youtu.be/F3OFzsaPtvI), [Project page](http://rpg.ifi.uzh.ch/ultimateslam.html), [PPT](http://rpg.ifi.uzh.ch/docs/BMVC17_Rebecq.pptx), [Oral presentation](https://youtu.be/iYptNMqK0tQ).
- <a name="Rosinol18ral"></a>Rosinol Vidal, A., Rebecq, H., Horstschaefer, T., Scaramuzza, D.,  
*[Ultimate SLAM? Combining Events, Images, and IMU for Robust Visual SLAM in HDR and High Speed Scenarios](https://doi.org/10.1109/LRA.2018.2793357)*,  
IEEE Robotics and Automation Letters (RA-L), 3(2):994-1001, Apr. 2018. [PDF](http://rpg.ifi.uzh.ch/docs/RAL18_VidalRebecq.pdf), [YouTube](https://youtu.be/jIvJuWdmemE), [Poster](http://rpg.ifi.uzh.ch/docs/RAL18_VidalRebecq_poster.pdf), [Project page](http://rpg.ifi.uzh.ch/ultimateslam.html), [ICRA18 video pitch](https://youtu.be/0hDGFFJQfmA).
- [Nelson, K. J., MSc Thesis 2019](#Nelson19MSc),  
*Event-Based Visual-Inertial Odometry on a Fixed-Wing Unmanned Aerial Vehicle*.
- [Rebecq et. al. TPAMI 2020](#Rebecq20tpami),  
*High Speed and High Dynamic Range Video with an Event Camera*.
    - [Rebecq et. al. CVPR 2019](#Rebecq19cvpr),  
*Events-to-Video: Bringing Modern Computer Vision to Event Cameras*.


<a name="segmentation"></a>
## Segmentation

<a name="object-segmentation"></a>
### Object Segmentation
- <a name="Barranco15iccv"></a>Barranco, F., Teo, C. L., Fermüller, C., Aloimonos, Y.,  
*[Contour Detection and Characterization for Asynchronous Event Sensors](https://doi.org/10.1109/ICCV.2015.63)*,  
IEEE Int. Conf. Computer Vision (ICCV), 2015, pp. 486-494. [PDF](http://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Barranco_Contour_Detection_and_ICCV_2015_paper.pdf), [Project page](http://www.umiacs.umd.edu/research/POETICON/DVSContours/)
- <a name="Marcireau18fnins"></a>Marcireau, A., Ieng, S.-H., Simon-Chane, C., Benosman, R.,  
*[Event-Based Color Segmentation With a High Dynamic Range Sensor](https://doi.org/10.3389/fnins.2018.00135)*.  
Front. Neurosci. (2018), 12:135. [PDF](https://www.neuromorphic-vision.com/public/publications/53/publication.pdf)
- <a name="Barranco18iros"></a>Barranco, F., Fermüller, C., Ros, E.,  
*[Real-Time Clustering and Multi-Target Tracking Using Event-Based Sensors](https://doi.org/10.1109/IROS.2018.8593380)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2018. [PDF](https://arxiv.org/pdf/1807.02851.pdf)
- <a name="Alonso19cvprw"></a>Alonso I., Murillo A.,  
*[EV-SegNet: Semantic Segmentation for Event-based Cameras](http://openaccess.thecvf.com/content_CVPRW_2019/papers/EventVision/Alonso_EV-SegNet_Semantic_Segmentation_for_Event-Based_Cameras_CVPRW_2019_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2019. [PDF](https://arxiv.org/pdf/1811.12039.pdf). [Project page](https://github.com/Shathe/Ev-SegNet). [Video pitch](https://youtu.be/AuXN7y3bMqo)


<a name="motion-segmentation"></a>
### Motion Segmentation
- [Glover et al., IROS 2016](#Glover16iros),  
*Event-driven ball detection and gaze fixation in clutter*.
    - [Glover et al., IROS 2017](#Glover17iros),  
*Robust Visual Tracking with a Freely-moving Event Camera*.
- <a name="Mishra17fnins"></a>Mishra, A., Ghosh, R., Principe, J.C., Thakor, N.V., Kukreja, S.L.,  
*[A Saccade Based Framework for Real-Time Motion Segmentation Using Event Based Vision Sensors](https://doi.org/10.3389/fnins.2017.00083)*,  
Front. Neurosci. (2017), 11:83.
- <a name="Vasco17icar"></a>Vasco, V., Glover, A., Mueggler, E., Scaramuzza, D., Natale, L., Bartolozzi, C.  
*[Independent Motion Detection with Event-driven Cameras](http://doi.org/10.1109/ICAR.2017.8023661)*,  
Int. Conf. Advanced Robotics (ICAR), 2017, pp. 530-536. [PDF](https://arxiv.org/pdf/1706.08713v2.pdf)
- [Stoffregen et. al. ACRA 2017](#Stoffregen17acra),  
*Simultaneous Optical Flow and Segmentation (SOFAS) using Dynamic Vision Sensor*.
- [Mitrokhin et al. IROS 2018](#Mitrokhin18iros),  
*Event-based Moving Object Detection and Tracking*.
- <a name="Stoffregen19iccv"></a>Stoffregen, T., Gallego, G., Drummond, T., Kleeman, L., Scaramuzza, D.,  
*[Event-Based Motion Segmentation by Motion Compensation](http://rpg.ifi.uzh.ch/docs/ICCV19_Stoffregen.pdf)*,  
IEEE Int. Conf. Computer Vision (ICCV), 2019. [PDF (animations best viewed with Acrobat Reader)](http://rpg.ifi.uzh.ch/docs/ICCV19_Stoffregen.pdf), [YouTube](https://youtu.be/0q6ap_OSBAk)
- [Mitrokhin et al., IROS 2019](#Mitrokhin19iros),  
*EV-IMO: Motion Segmentation Dataset and Learning Pipeline for Event Cameras*.  


<a name="pattern-recognition"></a>
## Pattern Recognition

<a name="object-recognition"></a>
### Object Recognition
- <a name="SerranoGotarredona09tnn"></a>Serrano-Gotarredona, R., Oster, M., Lichtsteiner, P., Linares-Barranco, A., Paz-Vicente, R., Gómez-Rodríguez, F., Camuñas-Mesa, L., Berner, R., Rivas, M., Delbrück, T., Liu, S. C., Douglas, R., Häfliger, P., Jiménez-Moreno, G., Civit, A., Serrano-Gotarredona, T., Acosta-Jiménez, A., Linares-Barranco, B.,  
*[CAVIAR: A 45k-Neuron, 5M-Synapse, 12G-connects/sec AER Hardware Sensory-Processing-Learning-Actuating System for High Speed Visual Object Recognition and Tracking](https://doi.org/10.1109/TNN.2009.2023653)*,  
IEEE Trans. on Neural Netw., 20(9):1417-1438, 2009. [PDF](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.192.1326&rep=rep1&type=pdf)
- <a name="Belbachir11tie"></a>Belbachir, A. N., Hofstaetter, M., Litzenberger, M., Schoen, P.,  
*[High Speed Embedded Object Analysis Using a Dual-Line Timed-Address-Event Temporal Contrast Vision Sensor](https://doi.org/10.1109/TIE.2010.2095390)*,  
IEEE Trans. Ind. Electron., 58(3):770-783, 2011.
- <a name="Ghosh14biocas"></a>Ghosh, R., Mishra, A., Orchard, G., Thakor, N.,  
*[Real-time object recognition and orientation estimation using an event-based camera and CNN](https://doi.org/10.1109/BioCAS.2014.6981783)*,  
IEEE Biomedical Circuits and Systems Conf. (BioCAS), 2014.
- <a name="SerranoGotarredona15iscas"></a>Serrano-Gotarredona, T., Linares-Barranco, B., Galluppi, F., Plana, L., Furber, S.,  
*[ConvNets experiments on SpiNNaker](https://doi.org/10.1109/ISCAS.2015.7169169)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2015.
- <a name="Cohen16fnins"></a>Cohen, G., Orchard, G., Ieng, S.-H., Tapson, J., Benosman, R., van Schaik, A.,  
*[Skimming Digits: Neuromorphic Classification of Spike-Encoded Images](https://doi.org/10.3389/fnins.2016.00184)*,  
Front. Neurosci. (2016), 10:184. [PDF](https://www.neuromorphic-vision.com/public/publications/45/publication.pdf)
- [Barua et. al. WACV 2016](#Barua16wacv). Face recognition.
- <a name="Moeys16ebccsp"></a>Moeys, D., Corradi F., Kerr, E., Vance, P., Das, G., Neil, D., Kerr, D., Delbruck, T.,  
*[Steering a Predator Robot using a Mixed Frame/Event-Driven Convolutional Neural Network](https://doi.org/10.1109/EBCCSP.2016.7605233)*,  
IEEE Int. Conf. Event-Based Control Comm. and Signal Proc. (EBCCSP), 2016. [PDF](https://arxiv.org/pdf/1606.09433.pdf), [YouTube 1](https://youtu.be/fL3YCIPxuhM), [YouTube 2](https://youtu.be/lPF3Youpmqk)
- <a name="Li16bics"></a>Li, H., Li, G., Shi, L.,  
*[Classification of Spatiotemporal Events Based on Random Forest](https://doi.org/10.1007/978-3-319-49685-6_13)*,  
Int. Conf. Brain Inspired Cognitive Systems (BICS), 2016.
- <a name="Ghosh16icann"></a>Ghosh, R., Siyi, T., Rasouli, M., Thakor, N. V., Kukreja, S. L.,    
*[Pose-Invariant Object Recognition for Event-Based Vision with Slow-ELM](https://doi.org/10.1007/978-3-319-44781-0_54)*,  
Int. Conf. Artificial Neural Networks (ICANN), 2016. [PDF](https://arxiv.org/pdf/1903.07873)
- <a name="Cohen18tnnls"></a>Cohen, G., Afshar, S., Orchard, G., Tapson, J., Benosman, R., van Schaik, A.,  
*[Spatial and Temporal Downsampling in Event-Based Visual Classification](https://doi.org/10.1109/TNNLS.2017.2785272)*,  
IEEE Trans. Neural Netw. Learn. Syst. (TNNLS), 29(10):5030-5044, Oct. 2018.
- <a name="Lenz18arxiv"></a>Lenz, G., Ieng, S.-H., Benosman, R.,  
*[Event-based Face Detection and Tracking in the Blink of an Eye](http://arxiv.org/abs/1803.10106)*,  
arXiv:1803.10106, 2018. [YouTube](https://www.youtube.com/watch?v=F5UzXQsr5Es)
- <a name="Ramesh18accvw"></a>Ramesh, B., Ussa, A., Della Vedova, L., Yang, H., Orchard, G.,  
*[PCA-RECT: An Energy-Efficient Object Detection Approach for Event Cameras](https://doi.org/10.1007/978-3-030-21074-8_35)*,  
Assian Conf. Computer Vision Workshops (ACCVW), 2018. [Code](https://github.com/nusneuromorphic/PCA-RECT)
    - <a name="Ramesh20fnins"></a>Ramesh, B., Ussa, A., Della Vedova, L., Yang, H., Orchard, G.,  
*[Low-Power Dynamic Object Detection and Classification With Freely Moving Event Cameras](https://doi.org/10.3389/fnins.2020.00135)*,  
Front. Neurosci. (2020), 14:135. [N-SOD Dataset](https://drive.google.com/drive/folders/10_bnZ_TOcq7xCtCiDcaDiIO3_Txgr19S)
- <a name="Negri18icecs"></a>Negri, P., Soto, M., Linares-Barranco, B., Serrano-Gotarredona, T.,  
*[Scene Context Classification with Event-Driven Spiking Deep Neural Networks](https://dx.doi.org/10.1109/ICECS.2018.8617982)*,  
IEEE Int. Conf. Electronics, Circuits and Systems (ICECS), 2018.
- <a name="Cannici19wacv"></a>Cannici, M., Ciccone, M., Romanoni, A., Matteucci, M.,  
*[Attention Mechanisms for Object Recognition With Event-Based Cameras](https://arxiv.org/abs/1807.09480)*,  
IEEE Winter Conf. Applications of Computer Vision (WACV), 2019.
- <a name="Jiang19icra"></a> Jiang, Z., Xia, P., Huang, K., Stechele, W., Chen, G., Bing, Z., Knoll, A.,  
*[Mixed Frame-/Event-Driven Fast Pedestrian Detection](https://doi.org/10.1109/ICRA.2019.8793924)*,  
IEEE Int. Conf. Robotics and Automation (ICRA), 2019.
- <a name="Rueckauer19arxiv"></a>Rueckauer, B., Kanzig, N., Liu, S.-C., Delbruck, T., Sandamirskaya, Y.,  
*[Closing the Accuracy Gap in an Event-Based Visual Recognition Task](https://arxiv.org/pdf/1906.08859.pdf)*,  
arXiv, 2019.
- <a name="Bi19iccv"></a>Bi, Y., Chadha, A., Abbas, A.,  Bourtsoulatze, E., Andreopoulos, Y.,  
*[Graph-Based Object Classification for Neuromorphic Vision Sensing](http://openaccess.thecvf.com/content_ICCV_2019/html/Bi_Graph-Based_Object_Classification_for_Neuromorphic_Vision_Sensing_ICCV_2019_paper.html),*  
IEEE Int. Conf. Computer Vision (ICCV), 2019.
[PDF](http://openaccess.thecvf.com/content_ICCV_2019/papers/Bi_Graph-Based_Object_Classification_for_Neuromorphic_Vision_Sensing_ICCV_2019_paper.pdf), [Suppl. Mat.](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Bi_Graph-Based_Object_Classification_ICCV_2019_supplemental.pdf), [PDF arXiv](https://arxiv.org/pdf/1908.06648.pdf), [Github Page](https://github.com/PIX2NVS/NVS2Graph), [ASL-DVS Dataset](https://www.dropbox.com/sh/ibq0jsicatn7l6r/AACNrNELV56rs1YInMWUs9CAa?dl=0).
    - [Bi et al arXiv 2019](#Bi19arxiv),  
*Graph-based Spatial-temporal Feature Learning for Neuromorphic Vision Sensing*.
- <a name="Li19icme"></a>Li, J., Dong, S., Yu, Z., Tian, Y., Huang, T.,  
*[Event-Based Vision Enhanced: A Joint Detection Framework in Autonomous Driving](https://doi.org/10.1109/ICME.2019.00242),*  
IEEE Int. Conf. Multimedia and Expo (ICME), 2019.
- <a name="Iacono19iros"></a>Iacono, M., D'Angelo, G., Glover, A., Tikhanoff, V., Niebur, E., Bartolozzi, C.,  
*[Proto-Object Based Saliency for Event-Driven Cameras](https://doi.org/10.1109/IROS40897.2019.8967943)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2019.
- <a name="Gao19iccvw"></a>Gao, S., Guo, G., Chen, C.L.P.,  
*[Event-Based Incremental Broad Learning System for Object Classification](http://openaccess.thecvf.com/content_ICCVW_2019/papers/CEFRL/Gao_Event-Based_Incremental_Broad_Learning_System_for_Object_Classification_ICCVW_2019_paper.pdf),*  
IEEE Int. Conf. Computer Vision Workshop (ICCVW), 2019.
- <a name="Nan19ssci"></a>Nan, Y., Xiao, R., Gao, S., Yan, R.,  
*[An Event-based Hierarchy Model for Object Recognition](https://www.researchgate.net/publication/336318915_An_Event-based_Hierarchy_Model_for_Object_Recognition)*,  
IEEE Symp. Series in Computational Intell. (SSCI), 2019.
- <a name="Damien19visigrapp"></a>Damien, J., Hubert, K., Frederic, C.,  
*[Convolutional Neural Network for Detection and Classification with Event-based Data](https://www.scitepress.org/PublicationsDetail.aspx?ID=gn69gKYUbaM%3d&t=1)*,  
Int. Joint Conf. Computer Vision, Imaging and Computer Graphics Theory and Applications (VISIGRAPP), 2019. [PDF](https://pdfs.semanticscholar.org/0453/c19ced72b649e0609f04cd861a75140ed734.pdf).
- <a name="Xiao19tnnls"></a>Xiao, R., Tang, H., Ma, Y., Yan, R., Orchard, G.,  
*[An Event-Driven Categorization Model for AER Image Sensors Using Multispike Encoding and Learning](https://doi.org/10.1109/TNNLS.2019.2945630)*,  
IEEE Trans. Neural Netw. Learn. Syst. (TNNLS), 2019.
- [Li and Shi, Front. Neurorobot. 2019](#Li19fnbot),  
*Robust Event-Based Object Tracking Combining Correlation Filter and CNN Representation*.
- <a name="CamunasMesa19icecs"></a>Camuñas-Mesa, L.A., Linares-Barranco, B., Serrano-Gotarredona, T.,  
*[Low-power hardware implementation of SNN with decision block for recognition tasks](https://doi.org/10.1109/ICECS46596.2019.8964964)*,  
IEEE Int. Conf. Electronics, Circuits and Systems (ICECS), 2019.
- [Park et al. IEDM 2019](#Park19iedm),  
*Low-Latency Interactive Sensing for Machine Vision*.
- <a name="Liu20aaai"></a>Liu, Q., Ruan, H., Xing, D., Tang, H., Pan, G.,  
*[Effective AER Object Classification Using Segmented Probability-Maximization Learning in Spiking Neural Networks](https://arxiv.org/pdf/2002.06199)*,  
AAAI Conf. Artificial Intelligence, 2020.


<a name="gesture-recognition"></a>
### Gesture Recognition
- <a name="Lee14tnnls"></a>Lee, J. H., Delbruck, T., Pfeiffer, M., Park, P.K.J., Shin, C.-W., Ryu, H., Kang, B. C.,  
*[Real-Time Gesture Interface Based on Event-Driven Processing From Stereo Silicon Retinas](https://doi.org/10.1109/TNNLS.2014.2308551)*,  
IEEE Trans. Neural Netw. Learn. Syst. (TNNLS), 25(12):2250-2263, 2014.
    - <a name="Lee12iscas"></a>Lee, J., Delbruck, T., Park, P.K.J., Pfeiffer, M., Shin, C. W., Ryu, H., Kang, B. C.,  
*[Live demonstration: Gesture-Based remote control using stereo pair of dynamic vision sensors](https://doi.org/10.1109/ISCAS.2012.6272144)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2012. [PDF](http://www.zora.uzh.ch/75315/1/Lee_et_al_Live_demonstration.pdf), [YouTube](https://youtu.be/IlKimfJN21A)
- <a name="Kohn12iscas"></a>Kohn, B., Belbachir, A.N., Hahn, T., Kaufmann, H.,  
*[Event-driven Body Motion Analysis For Real-time Gesture Recognition](https://doi.org/10.1109/ISCAS.2012.6272132)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2012. [PDF](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.839.4932&rep=rep1&type=pdf)
    - <a name="Kohn12cvprw"></a>Kohn, B., Belbachir, A.N., Nowakowska, A.,  
*[Real-time Gesture Recognition using a Bio-inspired 3D Vision Sensor](https://doi.org/10.1109/CVPRW.2012.6239184)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2012.
    - <a name="Kohn12cvprw2"></a>Kohn, B., Nowakowska, A., Belbachir, A.N.,  
*[Real-time Body Motion Analysis for Dance Pattern Recognition](https://doi.org/10.1109/CVPRW.2012.6238894)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2012.
- <a name="Orchard15tpami"></a>Orchard, G., Meyer, C., Etienne-Cummings, R., Posch, C., Thakor, N., Benosman, R.,  
*[HFIRST: A Temporal Approach to Object Recognition](https://doi.org/10.1109/TPAMI.2015.2392947)*,  
IEEE Trans. Pattern Anal. Machine Intell. (TPAMI), 37(10):2028-2040, 2015. [PDF](https://arxiv.org/pdf/1508.01176.pdf), [PDF](https://www.neuromorphic-vision.com/public/publications/36/publication.pdf)
    - [Code](https://github.com/gorchard/HFIRST): HFIRST: A simple spiking neural network for recognition based on the canonical frame-based HMAX model.
- <a name="Park15icip"></a>Park, P.K.J., Lee, K., Lee, J.H., Kang, B., Shin, C.-W., Woo, J., Kim, J.-S., Suh, Y., Kim, S., Moradi, S., Gurel, O., Ryu, H.,  
*[Computationally efficient, real-time motion recognition based on bio-inspired visual and cognitive processing](http://dx.doi.org/10.1109/ICIP.2015.7350936)*,  
IEEE Int. Conf. Image Processing (ICIP), 2015.
- <a name="Park16icip"></a>Park, P.K.J., Cho, B.H., Park, J.M., Lee, K., Kim, H.Y., Kang, H.A., Lee, H.G., Woo, J., Roh, Y., Lee, W.J., Shin, C.-W., Wang, Q., Ryu, H.,  
*[Performance improvement of deep learning based gesture recognition using spatiotemporal demosaicing technique](http://dx.doi.org/10.1109/ICIP.2016.7532633)*,  
IEEE Int. Conf. Image Processing (ICIP), 2016.
- <a name="Lungu17iscas"></a>Lungu, I.-A., Corradi, F., Delbruck, T.,  
*[Live Demonstration: Convolutional Neural Network Driven by Dynamic Vision Sensor Playing RoShamBo](https://doi.org/10.1109/ISCAS.2017.8050403)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2017. [YouTube](https://youtu.be/q5ua91n13TA), [Slides 36-39](http://rpg.ifi.uzh.ch/docs/ICRA17workshop/Delbruck.pdf)
- <a name="Amir17cvpr"></a>Amir, A., Taba, B., Berg, D., Melano, T., McKinstry, J., Di Nolfo, C., Nayak, T., Andreopoulos, A., Garreau, G., Mendoza, M., Kusnitz, J., Debole, M., Esser, S., Delbruck, T., Flickner, M., Modha, D.,  
*[A Low Power, Fully Event-Based Gesture Recognition System](https://doi.org/10.1109/CVPR.2017.781)*,  
 IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2017. [PDF](http://openaccess.thecvf.com/content_cvpr_2017/papers/Amir_A_Low_Power_CVPR_2017_paper.pdf), [Dataset](#dvsgesture_dataset)
    - [YouTube: IBM Research demonstrates event-based gesture recognition using a brain-inspired chip](https://youtu.be/g08IW-qRomM)
- <a name="Maro18arxiv"></a>Maro, J.-M., Benosman, R.,  
*[Event-based Gesture Recognition with Dynamic Background Suppression using Smartphone Computational Capabilities](https://arxiv.org/pdf/1811.07802)*,  
arXiv: 1811.07802, 2018.
- <a name="Wang19wacv"></a>Wang, Q., Zhang, Y., Yuan, J., Lu, Y.,  
*[Space-time Event Clouds for Gesture Recognition: from RGB Cameras to Event Cameras](https://cse.buffalo.edu/~jsyuan/papers/2019/WACV_2019_Qinyi.pdf)*,  
IEEE Winter Conf. Applications of Computer Vision (WACV), 2019.
- <a name="Ghosh19arxivb"></a>Ghosh, R., Gupta, A., Nakagawa, A., Soares, A. B., Thakor, N. V.,  
*[Spatiotemporal Filtering for Event-Based Action Recognition](https://arxiv.org/pdf/1903.07067)*,  
arXiv:1903.07067, 2019.
- <a name="Wang19cvpr"></a>Wang, Y., Du, B., Shen, Y., Wu, K., Zhao, G., Sun, J., Wen, H.,  
*[EV-Gait: Event-Based Robust Gait Recognition Using Dynamic Vision Sensors](http://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_EV-Gait_Event-Based_Robust_Gait_Recognition_Using_Dynamic_Vision_Sensors_CVPR_2019_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2019.
- <a name="Calabrese19cvprw"></a>Calabrese, E., Taverni, G., Easthope, C., Skriabine, S., Corradi, F., Longinotti, L., Eng, K., Delbruck, T.,  
*[DHP19: Dynamic Vision Sensor 3D Human Pose Dataset](http://openaccess.thecvf.com/content_CVPRW_2019/papers/EventVision/Calabrese_DHP19_Dynamic_Vision_Sensor_3D_Human_Pose_Dataset_CVPRW_2019_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2019. [Project page](https://sites.google.com/view/dhp19), [Video pitch](https://youtu.be/nFUAQYk3tYA).
- <a name="Pradhan19iscas"></a>Pradhan, B. R., Bethi, Y., Narayanan, S., Chakraborty, A., Thakur, C. S.,  
*[N-HAR: A Neuromorphic Event-Based Human Activity Recognition System Using Memory Surfaces](https://doi.org/10.1109/ISCAS.2019.8702581)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2019.
- <a name="Sokolova19mva"></a>Sokolova, A., Konushin, A.,  
*[Human identification by gait from event-based camera](https://doi.org/10.23919/MVA.2019.8758019)*,  
Int. Conf. Machine Vision Applications (MVA), 2019.
- <a name="Chadha19icassp"></a>Chadha, A., Bi, Y., A., Abbas, A., Andreopoulos, Y.,  
*[Neuromorphic Vision Sensing for CNN-based Action Recognition](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8683606),*  
IEEE Int. Conf. Acoust., Speech, Signal Proc. (ICASSP), 2019, [Github Page](https://github.com/PIX2NVS/NVS_ActionRecognition).
- <a name="Chen19tci"></a>Chen, H., Liu, W., Goel, R., Lua, R., Siddharth, M., Huang, Y., Veeraraghavan, A., Patel, A.,  
*[Fast Retinomorphic Event-Driven Representations for Video Gameplay and Action Recognition](https://doi.org/10.1109/TCI.2019.2948755)*,  
IEEE Trans. Comput. Imag. (TCI), 6:276-290, 2019.
- <a name="Lungu19jetcas"></a>Lungu, I.-A., Liu, S.-C., Delbruck, T.,  
*[Incremental learning of hand symbols using event-based cameras](https://doi.org/10.1109/JETCAS.2019.2951062)*,  
IEEE J. Emerging Sel. Topics Circuits Syst. (JETCAS), 2019.
    - <a name="Lungu19aicas"></a>Lungu, I. A., Liu, S.-C., Delbruck, T.,  
*[Fast event-driven incremental learning of hand symbols](https://doi.org/10.1109/AICAS.2019.8771472)*,  
IEEE Int. Conf. AI Circuits Syst. (AICAS), 2019.
- [Park et al. IEDM 2019](#Park19iedm),  
*Low-Latency Interactive Sensing for Machine Vision*.


<a name="learning-representation-features"></a>
### Representation / Feature Extraction
- Camuñas-Mesa, L., Zamarreño-Ramos, C., Linares-Barranco, A., Acosta-Jiménez, A., Serrano-Gotarredona, T., Linares-Barranco, B.  
*[An Event-Driven Multi-Kernel Convolution Processor Module for Event-Driven Vision Sensors](https://doi.org/10.1109/JSSC.2011.2167409)*,  
IEEE J. of Solid-State Circuits, 47(2):504-517, 2012.
- <a name="Zhao15tnnls"></a>Zhao, B., Ding, R., Chen, S., Linares-Barranco, B., Tang, H.,  
*[Feedforward Categorization on AER Motion Events using Cortex-like Features in a Spiking Neural Network](https://doi.org/10.1109/TNNLS.2014.2362542)*,  
IEEE Trans. Neural Netw. Learn. Syst. (TNNLS), 26(9):1963-1978, 2015.
- <a name="Lagorce17tpami"></a>Lagorce, X., Orchard, G., Gallupi, F., Shi, B., Benosman, R.,  
*[HOTS: A Hierarchy Of event-based Time-Surfaces for pattern recognition](https://doi.org/10.1109/TPAMI.2016.2574707)*,  
IEEE Trans. Pattern Anal. Machine Intell. (TPAMI), 39(7):1346-1359, 2017. [PDF](https://www.neuromorphic-vision.com/public/publications/1/publication.pdf)
- [Clady et. al. FNINS](#Clady17fnins),  
*A Motion-Based Feature for Event-Based Pattern Recognition*.
- <a name="Yousefzadeh17iscas"></a>Yousefzadeh, A., Masquelier, T., Serrano-Gotarredona, T., Linares-Barranco, B.,  
*[Live demonstration: Hardware implementation of convolutional STDP for on-line visual feature learning](https://doi.org/10.1109/ISCAS.2017.8050395)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2017.
- <a name="Sullivan17roman"></a>Sullivan, K., Lawson, W.,  
*[Representing motion information from event-based cameras](https://doi.org/10.1109/ROMAN.2017.8172497)*,  
IEEE Int. Symp. Robot and Human Interactive Comm. (RO-MAN), 2017.
- <a name="Li16neucom"></a>Li, H., Li, G., Ji, X., Shi, L.P.,  
*[Deep representation via convolutional neural network for classification of spatiotemporal event streams](https://doi.org/10.1016/j.neucom.2018.02.019)*,  
Neurocomputing 299, 2018.
- <a name="Sironi18cvpr"></a>Sironi, A., Brambilla, M., Bourdis, N., Lagorce, X., Benosman, R.,    
*[HATS: Histograms of Averaged Time Surfaces for Robust Event-based Object Classification](http://openaccess.thecvf.com/content_cvpr_2018/papers/Sironi_HATS_Histograms_of_CVPR_2018_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2018. [PDF](https://arxiv.org/abs/1803.07913).
    - [N-CARS Dataset](#ncars_dataset): A large real-world event-based dataset for car classification.
- <a name="LiuW18arxiv"></a>Liu, W., Chen, H., Goel, R., Huang, Y., Veeraraghavan, A., Patel, A.,  
*[Fast Retinomorphic Event-Driven Representations for Video Recognition and Reinforcement Learning](https://arxiv.org/pdf/1805.06374.pdf)*,  
arXiv: 1805.06374, 2018.
- <a name="Cannici19cvprw"></a>Cannici, M., Ciccone, M., Romanoni, A., Matteucci, M.,  
*[Asynchronous Convolutional Networks for Object Detection in Neuromorphic Cameras](http://openaccess.thecvf.com/content_CVPRW_2019/papers/EventVision/Cannici_Asynchronous_Convolutional_Networks_for_Object_Detection_in_Neuromorphic_Cameras_CVPRW_2019_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2019. [PDF](https://arxiv.org/pdf/1805.07931). [Video pitch](https://youtu.be/JKRSeg3WrGw)
- <a name="Afshar18fnins"></a>Afshar, S., Hamilton, T. J., Tapson, J., van Schaik, A., Cohen, G.,  
*[Investigation of Event-Based Surfaces for High-Speed Detection, Unsupervised Feature Extraction, and Object Recognition](https://doi.org/10.3389/fnins.2018.01047)*,  
Front. Neurosci. (2018), 12:1047.
- <a name="Sekikawa183dv"></a>Sekikawa, Y., Ishikawa, K., Hara, K., Yoshida, Y., Suzuki, K., Sato, I., Saito, H.,  
*[Constant Velocity 3D Convolution](https://doi.org/10.1109/3DV.2018.00047)*,  
Int. Conf. 3D Vision (3DV), 2018.
    - <a name="Sekikawa18access"></a>Sekikawa, Y., Ishikawa, K., Saito, H.,  
*[Constant Velocity 3D Convolution](https://doi.org/10.1109/ACCESS.2018.2883340)*,  
IEEE Access, vol. 6, pp. 76490-76501, 2018.
- <a name="Chen19fnins"></a>Chen, G., Chen, J., Lienen, M., Conradt, J., Roehrbein, F., Knoll, A.C.,  
*[FLGR: Fixed Length Gists Representation Learning for RNN-HMM Hybrid-Based Neuromorphic Continuous Gesture Recognition](https://dx.doi.org/10.3389%2Ffnins.2019.00073)*,  
Front. Neurosci. (2019), 13:73.
- <a name="Tapiador18tbiocas"></a>Tapiador-Morales, R., Linares-Barranco, A., Jimenez-Fernandez, A., Jimenez-Moreno, G.  
*[Neuromorphic LIF Row-by-Row Multiconvolution Processor for FPGA](https://doi.org/10.1109/TBCAS.2018.2880012)*,  
IEEE Trans. Biomed. Circuits Syst, 2019, vol. 13, issue 1.
- <a name="Ghosh19arxiv"></a>Ghosh, R., Gupta, A., Tang, S., Soares, A. B., Thakor, N. V.,  
*[Spatiotemporal Feature Learning for Event-Based Vision](https://arxiv.org/pdf/1903.06923)*,  
arXiv:1903.06923, 2019.
- <a name="Sekikawa19cvpr"></a>Sekikawa, Y., Hara, K., Saito, H.,  
*[EventNet: Asynchronous Recursive Event Processing](http://openaccess.thecvf.com/content_CVPR_2019/papers/Sekikawa_EventNet_Asynchronous_Recursive_Event_Processing_CVPR_2019_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2019. [PDF](https://arxiv.org/abs/1812.07045), [Slides](http://rpg.ifi.uzh.ch/docs/CVPR19workshop/CVPRW19_Yusuke_Sekikawa.pdf), [YouTube](https://youtu.be/jHcxQRC-7iQ)
- <a name="Gehrig19iccv"></a>Gehrig, D., Loquercio, A., Derpanis, K. G., Scaramuzza, D.,  
*[End-to-End Learning of Representations for Asynchronous Event-Based Data](http://openaccess.thecvf.com/content_ICCV_2019/papers/Gehrig_End-to-End_Learning_of_Representations_for_Asynchronous_Event-Based_Data_ICCV_2019_paper.pdf)*,  
IEEE Int. Conf. Computer Vision (ICCV), 2019. [PDF](http://rpg.ifi.uzh.ch/docs/ICCV19_Gehrig.pdf), [Suppl. Mat](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Gehrig_End-to-End_Learning_of_ICCV_2019_supplemental.pdf),  [YouTube](https://youtu.be/bQtSx59GXRY),  [Project Page](https://github.com/uzh-rpg/rpg_event_representation_learning).
- <a name="LinaresBarranco19arxiv"></a>Linares-Barranco, A., Rios-Navarro, A., Tapiador-Morales, R., Delbruck, T.,  
*[Dynamic Vision Sensor integration on FPGA-based CNN accelerators for high-speed visual classification](https://arxiv.org/abs/1905.07419)*,  
arXiv:1905.07419, 2019.
- <a name="Afshar19arxiv"></a>Afshar, S., Xu, Y., Tapson, J., van Schaik, A., Cohen, G.,  
*[Event-based Feature Extraction using Adaptive Selection Thresholds](https://arxiv.org/pdf/1907.07853)*,  
arXiv:1907.07853, 2019
- <a name="Zhu19arxiv"></a>Zhu, A.Z., Wang, Z., Daniilidis, K.,  
*[Motion Equivariant Networks for Event Cameras with the Temporal Normalization Transform](https://arxiv.org/abs/1902.06820)*,  
arXiv:1902.06820, 2019.
- <a name="Baldwin19iciar"></a>Baldwin R.W., Almatrafi M., Kaufman J.R., Asari V., Hirakawa K.,  
*[Inceptive Event Time-Surfaces for Object Classification Using Neuromorphic Cameras](https://link.springer.com/chapter/10.1007/978-3-030-27272-2_35)*,  
Int. Conf. on Image Analysis and Recognition (ICIAR), 2019. [PDF](https://rdcu.be/bQcGk), [Code](https://github.com/bald6354/iets).
- <a name="Bi19arxiv"></a>Bi, Y., Chadha, A., Abbas, A.,  Bourtsoulatze, E., Andreopoulos, Y.,  
*[Graph-based Spatial-temporal Feature Learning for Neuromorphic Vision Sensing](https://arxiv.org/pdf/1910.03579),*  
arXiv:1910.03579, 2019.
- <a name="Zhu19arxivGAN"></a>Zhu, A., Wang, Z., Khant, K., Daniilidis, K.,  
*[EventGAN: Leveraging Large Scale Image Datasets for Event Cameras](https://arxiv.org/pdf/1912.01584)*,  
arXiv:1912.01584, 2019.
- <a name="Cannici20arxiv"></a>Cannici, M., Ciccone, M., Romanoni, A., Matteucci, M.,  
*[Matrix-LSTM: a Differentiable Recurrent Surface for Asynchronous Event-Based Data](https://arxiv.org/pdf/2001.03455)*,  
arXiv:2001.03455, 2020. [Videos](https://drive.google.com/drive/folders/1KzhKKwJGXvMnhbg1l6gEArgYote7WW8V)


<a name="learning-regression"></a>
### Regression Tasks
- <a name="Maqueda18cvpr"></a>Maqueda, A.I., Loquercio, A., Gallego, G., Garcia, N., Scaramuzza, D.,  
*[Event-based Vision meets Deep Learning on Steering Prediction for Self-driving Cars](http://openaccess.thecvf.com/content_cvpr_2018/papers/Maqueda_Event-Based_Vision_Meets_CVPR_2018_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition (CVPR), 2018. [PDF](http://rpg.ifi.uzh.ch/docs/CVPR18_Maqueda.pdf), [Poster](http://rpg.ifi.uzh.ch/docs/CVPR18_Maqueda_poster.pdf),  [YouTube](https://youtu.be/_r_bsjkJTHA).
- [Zhu et. al. RSS 2018](#Zhu18rss),  
*EV-FlowNet: Self-Supervised Optical Flow Estimation for Event-based Cameras.*
- [Paredes-Valles et. al. TPAMI 2019](#ParedesValles19tpami),  
*Unsupervised Learning of a Hierarchical Spiking Neural Network for Optical Flow Estimation: From Events to Global Motion Perception.*
- [Gallego et. al. CVPR 2019](#Gallego19cvpr),  
*Focus Is All You Need: Loss Functions For Event-based Vision*.
- [Rebecq et. al. TPAMI 2020](#Rebecq20tpami),  
*High Speed and High Dynamic Range Video with an Event Camera*.
    - [Rebecq et. al. CVPR 2019](#Rebecq19cvpr),  
*Events-to-Video: Bringing Modern Computer Vision to Event Cameras*.
- [Zhu et. al. CVPR 2019](#Zhu19cvpr),  
*Unsupervised Event-Based Learning of Optical Flow, Depth, and Egomotion.*
- <a name="Hu19aicas"></a>Hu, Y., Chen, H. M., Delbruck, T.,  
*[Slasher: Stadium racer car for event camera end-to-end learning autonomous driving experiments](https://doi.org/10.1109/AICAS.2019.8771520)*,  
IEEE Int. Conf. AI Circuits Syst. (AICAS), 2019.


<a name="learning-methods-frameworks"></a>
### Learning Methods / Frameworks
- <a name="PerezCarrasco13tpami"></a>Perez-Carrasco, J. A., Zhao, B., Serrano, C., Acha, B., Serrano-Gotarredona, T., Chen, S., Linares-Barranco, B.,  
*[Mapping from Frame-Driven to Frame-Free Event-Driven Vision Systems by Low-Rate Rate-Coding and Coincidence Processing. Application to Feed-Forward ConvNets](https://doi.org/10.1109/TPAMI.2013.71)*,  
IEEE Trans. Pattern Anal. Machine Intell. (TPAMI), 35(11):2706-2719, 2013.
- <a name="Stromatias17fnins"></a>Stromatias, E., Soto, M., Serrano-Gotarredona, T., Linares-Barranco, B.,  
*[An Event-Based Classifier for Dynamic Vision Sensor and Synthetic Data](https://doi.org/10.3389/fnins.2017.00350)*,  
Front. Neurosci. (2017), 11:350.
- <a name="Haessig18spie"></a>Haessig, G. and Benosman, R.,  
*[A Sparse Coding Multi-Scale Precise-Timing Machine Learning Algorithm for Neuromorphic Event-Based Sensors](https://doi.org/10.1117/12.2305933)*,  
Proc. SPIE 10639, Micro- and Nanotechnology Sensors, Systems, and Applications X, 106391U, 2018. [PDF](https://arxiv.org/pdf/1804.09236.pdf)
- <a name="Shrestha18nips"></a>Shrestha, S., Orchard, G.,  
*[SLAYER: Spike Layer Error Reassignment in time](https://arxiv.org/abs/1810.08646)*,  
Advances in Neural Information Processing Systems (NeurIPS) 2018. [PDF](https://arxiv.org/pdf/1810.08646.pdf), [YouTube](https://youtu.be/JGdatqqci5o).
- <a name="Macanovic18arxiv"></a>Macanovic, M., Chersi, F., Rutard, F., Ieng, S.-H., Benosman, R.,  
*[When Conventional machine learning meets neuromorphic engineering: Deep Temporal Networks (DTNets) a machine learning framework allowing to operate on Events and Frames and implantable on Tensor Flow Like Hardware](https://arxiv.org/pdf/1811.07672)*,  
arXiv: 1811.07672, 2018.
- <a name="Zanardi19rss"></a>Zanardi, A., Aumiller, A.J., Zilly, J., Censi, A., Frazzoli, E.,  
*[Cross-Modal Learning Filters for RGB-Neuromorphic Wormhole Learning](http://www.roboticsproceedings.org/rss15/p45.html)*,  
Robotics: Science and Systems (RSS), 2019. [PDF](https://www.research-collection.ethz.ch/bitstream/handle/20.500.11850/349414/1/rsswebsite.pdf)
- <a name="Kaiser19arxiv"></a>Kaiser, J., Friedrich, A., Vasquez Tieck, J.C., Reichard, D., Roennau, A., Neftci, E., Dillmann, R.,  
*[Embodied Neuromorphic Vision with Event-Driven Random Backpropagation](https://arxiv.org/abs/1904.04805)*,  
arXiv, 2019. [PDF](https://arxiv.org/pdf/1904.04805), [Video](https://neurorobotics-files.net/index.php/s/sBQzWFrBPoH9Dx7)


<br><br>
<a name="control"></a>
## Control
- <a name="Delbruck13fnins"></a>Delbruck, T. and Lang, M.,  
*[Robotic Goalie with 3ms Reaction Time at 4% CPU Load Using Event-Based Dynamic Vision Sensor](https://doi.org/10.3389/fnins.2013.00223)*,  
Front. Neurosci. (2013), 7:223. [PDF](http://www.zora.uzh.ch/107801/1/fnins-07-00223.pdf), [YouTube](https://youtu.be/IC5x7ftJ96w)
    - <a name="Delbruck07iscas"></a>Delbruck, T. and Lichtsteiner, P.,  
*[Fast sensory motor control based on event-based hybrid neuromorphic-procedural system](https://doi.org/10.1109/ISCAS.2007.378038)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2007.
- <a name="Conradt09iscas"></a>Conradt, J., Cook, M., Berner, R., Lichtsteiner, P., Douglas, R. J., Delbruck, T.,  
*[A Pencil Balancing Robot Using a Pair of AER Dynamic Vision Sensors](https://doi.org/10.1109/ISCAS.2009.5117867)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2009. [PDF](https://www.ini.uzh.ch/~conradt/publications/ISCAS2009-JConradt.pdf), [Poster](https://www.ini.uzh.ch/~conradt/publications/NIPS2008-JConradt.pdf), [Project page](https://www.ini.uzh.ch/~conradt/projects/PencilBalancer/), [YouTube 1](https://youtu.be/XVR5wEYkEGk), [YouTube 2](https://youtu.be/f9UngTdngY4), [YouTube 3](https://youtu.be/yCOnDc5r7p8)
    - <a name="Conradt09iccvw"></a>Conradt, J., Berner, R., Cook, M., Delbruck, T.,  
*[An embedded AER dynamic vision sensor for low-latency pole balancing](https://doi.org/10.1109/ICCVW.2009.5457625)*,  
IEEE Int. Conf. Computer Vision Workshops (ICCVW), 2009. [PDF](http://www.ini.uzh.ch/admin/extras/doc_get.php?id=42580)
- <a name="Mueller15ebccsp"></a>Mueller, E., Censi, A., Frazzoli, E.,  
*[Efficient high speed signal estimation with neuromorphic vision sensors](https://doi.org/10.1109/EBCCSP.2015.7300672)*,  
IEEE Int. Conf. Event-Based Control Comm. and Signal Proc. (EBCCSP), 2015.
- <a name="Censi15acc"></a>Censi, A.,  
*[Efficient Neuromorphic Optomotor Heading Regulation](https://doi.org/10.1109/ACC.2015.7171931)*,  
American Control Conference (ACC), 2015.
- <a name="Mueggler15ecmr"></a>Mueggler, E., Baumli, N., Fontana, F., Scaramuzza, D.,  
*[Towards Evasive Maneuvers with Quadrotors using Dynamic Vision Sensors](https://doi.org/10.1109/ECMR.2015.7324048)*,  
Eur. Conf. Mobile Robots (ECMR), Lincoln, 2015. [PDF](http://rpg.ifi.uzh.ch/docs/ECMR15_Mueggler.pdf)
- <a name="Delbruck15iscas"></a>Delbruck, T., Pfeiffer, M., Juston, R., Orchard, G., Mueggler, E., Linares-Barranco, A., Tilden, M. W.,  
*[Human vs. computer slot car racing using an event and frame-based DAVIS vision sensor](https://doi.org/10.1109/ISCAS.2015.7169170)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2015. [YouTube 1](https://youtu.be/CnGPGiZuFRI), [YouTube 2](https://youtu.be/ALneVn-Ls2Q)
- <a name="Mueller15cdc"></a>Mueller, E., Censi, A., Frazzoli, E.,  
*[Low-latency heading feedback control with neuromorphic vision sensors using efficient approximated incremental inference](https://doi.org/10.1109/CDC.2015.7402002)*,  
IEEE Conf. Decision and Control (CDC), 2015.
- [Moeys et. al. EBCCSP 2016](#Moeys16ebccsp).  *VISUALISE Predator/Prey Dataset*.
- <a name="Vasco16humanoids"></a>Vasco, V., Glover, A., Tirupachuri, Y., Solari, F., Chessa M., Bartolozzi C.,  
*[Vergence control with a neuromorphic iCub](https://doi.org/10.1109/HUMANOIDS.2016.7803355)*,  
IEEE Int. Conf. Humanoid Robotics (Humanoids), 2016.
- <a name="Singh16cdc"></a>Singh, P., Yong, S. Z., Gregoire, J., Censi, A., Frazzoli, E.,  
*[Stabilization of linear continuous-time systems using neuromorphic vision sensors](https://doi.org/10.1109/CDC.2016.7798722)*,  
IEEE Conf. Decision and Control (CDC), 2016.
    - <a name="Singh17cdc"></a>Singh, P., Yong, S. Z., Frazzoli, E.,  
*[Stabilization of stochastic linear continuous-time systems using noisy neuromorphic vision sensors](https://doi.org/10.23919/ACC.2017.7963008)*,  
American Control Conference (ACC), 2017.
    - <a name="Singh19tac"></a>Singh, P., Yong, S. Z., Frazzoli, E.,  
*[Regulation of Linear Systems Using Event-Based Detection Sensors](https://doi.org/10.1109/TAC.2018.2876997)*,  
IEEE Trans. Automatic Control, 2019.
- <a name="Blum17rss"></a>Blum, H., Dietmüller, A., Milde, M., Conradt, J., Indiveri, G., Sandamirskaya, Y.,  
*[A neuromorphic controller for a robotic vehicle equipped with a Dynamic Vision Sensor](http://www.roboticsproceedings.org/rss13/p35.pdf)*,  
Robotics: Science and Systems (RSS), 2017.
- <a name="Glover18icra"></a>Glover, A., Vasco, V., Bartolozzi, C.,  
*[A Controlled-Delay Event Camera Framework for On-Line Robotics](https://doi.org/10.1109/ICRA.2018.8460541)*,  
IEEE Int. Conf. Robotics and Automation (ICRA), 2018.
- <a name="Falanga19ral"></a>Falanga, D., Kim, S., Scaramuzza, D.,  
*[How Fast is Too Fast? The Role of Perception Latency in High-Speed Sense and Avoid](http://rpg.ifi.uzh.ch/docs/RAL19_Falanga.pdf)*,  
IEEE Robotics and Automation Letters (RA-L), 2019. [YouTube](https://youtu.be/sbJAi6SXOQw)
- <a name="Sanket19arxiv"></a>Sanket, N.J., Parameshwara, C.M., Singh, C.D., Kuruttukulam, A.V., Fermüller, C., Scaramuzza, D., Aloimonos, Y.,  
*[EVDodge: Embodied AI For High-Speed Dodging On A Quadrotor Using Event Cameras](https://arxiv.org/pdf/1906.02919)*,  
arXiv:1906.02919, 2019. [PDF](https://prg.cs.umd.edu/research/EVDodge_files/EVDodge.pdf), [YouTube](https://youtu.be/k1uzsiDI4hM), [Project page](http://prg.cs.umd.edu/EVDodgeNet), [Code](https://github.com/prgumd/EVDodge).


<a name="space"></a>
## Space Applications
- <a name="Cohen17amos"></a>Cohen, G., Afshar, S., van Schaik, A., Wabnitz, A., Bessell, T., Rutten, M., Morreale, B.,  
*[Event-based Sensing for Space Situational Awareness](https://amostech.com/TechnicalPapers/2017/Optical-Systems/Cohen.pdf)*,  
Proc. Advanced Maui Optical and Space Surveillance Technologies Conf. (AMOS), 2017.
- <a name="Cheung18fusion"></a>Cheung, B., Rutten, M., Davey, S., Cohen, G.,  
*[Probabilistic Multi Hypothesis Tracker for an Event Based Sensor](http://dx.doi.org/10.23919/ICIF.2018.8455718)*,  
Int. Conf. Information Fusion (FUSION) 2018, pp. 1-8.
- <a name="Cohen18amos"></a>Cohen, G., Afshar, S., van Schaik, A.,  
*[Approaches for Astrometry using Event-Based Sensors](https://amostech.com/TechnicalPapers/2018/Poster/Cohen.pdf)*,  
Proc. Advanced Maui Optical and Space Surveillance Technologies Conf. (AMOS), 2018.
- <a name="Chin19cvprw"></a>Chin, T.-J., Bagchi, S., Eriksson, A., van Schaik, A.,  
*[Star Tracking using an Event Camera](http://openaccess.thecvf.com/content_CVPRW_2019/papers/EventVision/Chin_Star_Tracking_Using_an_Event_Camera_CVPRW_2019_paper.pdf)*,  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2019. [PDF](https://arxiv.org/pdf/1812.02895). [Project page](https://cs.adelaide.edu.au/~tjchin/startracking/). [Video pitch](https://youtu.be/XuYYhyS8IwM)
- Western Sydney University ICNS
    - [Astrosite](https://www.westernsydney.edu.au/icns/astrosite): [University News](https://www.westernsydney.edu.au/newscentre/news_centre/more_news_stories/world-first_technology_to_revolutionise_space_imaging), [ABC News](https://www.abc.net.au/news/2019-02-24/space-camera-astrosite-created-in-sydney-a-game-change-raaf-says/10842220).
    - [Simultaneous Sky Mapping and Satellite Tracking](https://www.westernsydney.edu.au/icns/research/research_streams/perception/sky_mapping_satellite_tracking)
- <a name="Zolnowski19neosst"></a>Zolnowski, M., Reszelewski, R., Moeys, D.P., Delbruck, T., Kaminski, K.,  
*[Observational Evaluation of Event Cameras Performance in Optical Space Surveillance](https://conference.sdo.esoc.esa.int/proceedings/neosst1/paper/475/NEOSST1-paper475.pdf)*,  
Proc. NEO and Debris Detection Conference, Darmstadt, Germany, Jan. 2019.
- <a name="Bagchi20wacv"></a>Bagchi, S., Chin, T.-J.,  
*[Event-based Star Tracking via Multiresolution Progressive Hough Transforms](http://openaccess.thecvf.com/content_WACV_2020/papers/Bagchi_Event-based_Star_Tracking_via_Multiresolution_Progressive_Hough_Transforms_WACV_2020_paper.pdf)*,  
IEEE Winter Conf. Applications of Computer Vision (WACV), 2020. [PDF](https://arxiv.org/pdf/1906.07866.pdf)
- <a name="Afshar19arxiv"></a>Afshar, S., Nicholson, A. P., van Schaik, A., Cohen, G.,  
*[Event-based Object Detection and Tracking for Space Situational Awareness](https://arxiv.org/pdf/1911.08730)*,  
arXiv:1911.08730, 2019.


<a name="tactile_sensing"></a>
## Tactile Sensing Applications
- <a name="Rigi18sensors"></a>Rigi, A., Baghaei Naeini, F., Makris, D., Zweiri, Y.,  
*[A Novel Event-Based Incipient Slip Detection Using Dynamic Active-Pixel Vision Sensor (DAVIS)](https://doi.org/10.3390/s18020333)*,  
Sensors 2018, 18, 333.
- <a name="Naeini19tim"></a>Naeini, F. B., Alali, A., Al-Husari, R., Rigi, A., AlSharman, M. K., Makris, D., Zweiri, Y.,  
*[A Novel Dynamic-Vision-Based Approach for Tactile Sensing Applications](https://doi.org/10.1109/TIM.2019.2919354)*,  
IEEE Trans. Instrum. Meas., 2019.

<a name="signal_processing"></a>
# Signal Processing
- <a name="Ieng14ieee"></a>Ieng, S.-H., Posch, C., Benosman, R.,  
*[Asynchronous Neuromorphic Event-Driven Image Filtering](https://doi.org/10.1109/JPROC.2014.2347355)*,  
Proc. IEEE, 102(10):1485-1499, 2014. [PDF](http://neuromorphic-vision.com/public/publications/20/publication.pdf)
- <a name="Fillatre15eusipco"></a>Fillatre, L., Antonini, M.,   
*[Uniformly minimum variance unbiased estimation for asynchronous event-based cameras](https://doi.org/10.1109/ICIP.2014.7025834)*,  
IEEE Int. Conf. Image Processing (ICIP), 2014.
- [Mueggler et al. ICRA 2015](#Mueggler15icra),  
*Lifetime Estimation of Events from Dynamic Vision Sensors*.
- <a name="Liu15iscas"></a>Klein, P., Conradt, J., Liu, S.-C.,  
*[Scene stitching with event-driven sensors on a robot head platform](https://doi.org/10.1109/ISCAS.2015.7169173)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2015.
- <a name="Fillatre15eusipco"></a>Fillatre, L.,  
*[Bayes classification for asynchronous event-based cameras](https://doi.org/10.1109/EUSIPCO.2015.7362498)*,  
European Signal Process. Conf. (EUSIPCO), 2015.
- <a name="Sabatier17tip"></a>Sabatier, Q., Ieng, S.-H., Benosman, R.,  
*[Asynchronous Event-Based Fourier Analysis](https://doi.org/10.1109/TIP.2017.2661702)*,  
IEEE Trans. Image Process., 2017, pp. 2192-2202. [PDF](https://www.neuromorphic-vision.com/public/publications/7/publication.pdf), [Suppl. Mat.](https://www.neuromorphic-vision.com/public/publications/7/supplementaryMaterial.zip)
- <a name="Khodamoradi19tetc"></a>Khodamoradi, A., Kastner, R.,  
*[O(N)-Space Spatiotemporal Filter for Reducing Noise in Neuromorphic Vision Sensors](https://doi.org/10.1109/TETC.2017.2788865)*,  
IEEE Trans. Emerging Topics in Computing, 2018.
- [Scheerlinck et. al. RAL 2019](#Scheerlinck19ral),  
*Asynchronous Spatial Image Convolutions for Event Cameras*.
- <a name="Lee19arxiv"></a>Lee, S., Kim, H., Kim, H.J.,  
*[Edge Detection for Event Cameras using Intra-pixel-area Events](https://bmvc2019.org/wp-content/uploads/papers/1140-paper.pdf)*,  
British Machine Vision Conf. (BMVC), 2019. [PDF](https://arxiv.org/pdf/1907.07469)


<br><br>
<a name="datasets"></a>
# Datasets and Simulators (sorted by topic)

## Emulators and Simulators
- <a name="Katz12iscas"></a>Katz, M. L., Nikolic, K., Delbruck, T. (2012),  
*[Live demonstration: Behavioural emulation of event-based vision sensors](https://doi.org/10.1109/ISCAS.2012.6272143)*,  
IEEE Int. Symp. Circuits and Systems (ISCAS), 2012. [PDF](https://drive.google.com/open?id=1asyMIQIAtsl3_KqgfPuZagr_gjKZhbYm)
- <a name="Kaiser16simpar"></a>Kaiser, J., Tieck, J. C. V., Hubschneider, C., Wolf, P., Weber, M., Hoff, M., Friedrich., A., Wojtasik, K., Roennau, A., Kohlhaas, R., Dillmann, R., Zoellner, M. (2016),  
*[Towards a framework for end-to-end control of a simulated vehicle with spiking neural networks](https://doi.org/10.1109/SIMPAR.2016.7862386)*,  
IEEE Int. Conf. on Simulation, Modeling, and Programming for Autonomous Robots (SIMPAR), 2016. [PDF](https://www.researchgate.net/profile/Jacques_Kaiser/publication/309558315_Towards_a_framework_for_end-to-end_control_of_a_simulated_vehicle_with_spiking_neural_networks/links/5bb568b192851ca9ed379dc3/Towards-a-framework-for-end-to-end-control-of-a-simulated-vehicle-with-spiking-neural-networks.pdf), [Gazebo DVS plugin](https://github.com/HBPNeurorobotics/gazebo_dvs_plugin)
- <a name="Pineda16ssci"></a>Pineda García, G., Camilleri, P., Liu, Q., Furber, S.,  
*[pyDVS: An extensible, real-time Dynamic Vision Sensor emulator using off-the-shelf hardware](https://doi.org/10.1109/SSCI.2016.7850249)*,  
IEEE Int. Symp. Series on Computational Intelligence (SSCI), 2016. [Code](https://github.com/chanokin/pyDVS)
- E. Mueggler, H. Rebecq, G. Gallego, T. Delbruck, D. Scaramuzza,  
*[The Event-Camera Dataset and Simulator: Event-based Data for Pose Estimation, Visual Odometry, and SLAM](http://rpg.ifi.uzh.ch/davis_data.html),*  
Int. J. Robotics Research, 36:2, pp. 142-149, 2017. [PDF](https://arxiv.org/pdf/1610.08336.pdf), [PDF IJRR](http://dx.doi.org/10.1177/0278364917691115), [YouTube](https://youtu.be/bVVBTQ7l36I), [Dataset](http://rpg.ifi.uzh.ch/davis_data.html).
- <a name="Bi17icip"></a>Bi, Y. and Andreopoulos, Y.,  
*[PIX2NVS: Parameterized conversion of pixel-domain video frames to neuromorphic vision streams](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8296630),*  
IEEE Int. Conf. Image Processing (ICIP), 2017, [GitHub Page](https://github.com/PIX2NVS/PIX2NVS).
- <a name="Li18bmvc"></a>W. Li, S. Saeedi, J. McCormac, R. Clark, D. Tzoumanikas, Q. Ye, Y. Huang, R. Tang, S. Leutenegger,  
[Interiornet: Mega-scale multi-sensor photo-realistic indoor scenes dataset](https://arxiv.org/pdf/1809.00716.pdf),  
British Machine Vis. Conf. (BMVC), 2018. [YouTube](https://youtu.be/z8uJh_xUq7A), [Project Page](https://interiornet.org/).
- <a name="Rebecq18corl"></a>H. Rebecq, D. Gehrig, D. Scaramuzza,  
*[ESIM: an Open Event Camera Simulator](http://rpg.ifi.uzh.ch/docs/CORL18_Rebecq.pdf),*  
Conf. on Robot Learning (CoRL), 2018. [PDF](http://rpg.ifi.uzh.ch/docs/CORL18_Rebecq.pdf), [YouTube](https://youtu.be/ytKOIX_2clo), [Project Page](http://rpg.ifi.uzh.ch/esim/index.html).



## Datasets (sorted by topic)
- [Datasets from the Sensors group at INI](http://sensors.ini.uzh.ch/databases.html) (Institute of Neuroinformatics), Zurich:
    - DVS09 - 	DVS128 Dynamic Vision Sensor Silicon Retina
    - DVSFLOW16 - 	DVS/DAVIS Optical Flow Dataset
    - DVSACT16 -	DVS Datasets for Object Tracking, Action Recognition and Object Recognition
    - PRED18 - 	VISUALISE Predator/Prey Dataset
    - DDD17 - 	DAVIS Driving Dataset 2017
    - ROSHAMBO17 - 	RoShamBo Rock Scissors Paper game DVS dataset
    - DHP19 - 	DAVIS Human Pose Estimation and Action Recognition

### Optical Flow
- [DVS/DAVIS Optical Flow Dataset](https://docs.google.com/document/d/1r9sRYANGuDTUcfSSq-sL4sd79SfjHGNRul_10uztDaI/pub) associated to the paper [Rueckauer and Delbruck, FNINS 2016](#Rueckauer16fnins).
- [Bardow et al. CVPR2016](#Bardow16cvpr), [Four sequences](http://wp.doc.ic.ac.uk/pb2114/datasets/)
- [Zhu et al. RAL2018](#Zhu18mvsec): *MVSEC The Multi Vehicle Stereo Event Camera Dataset*.

### Intensity-Image Reconstruction from events
- [Bardow et al. CVPR2016](#Bardow16cvpr), [Four sequences](http://wp.doc.ic.ac.uk/pb2114/datasets/)
- [Scheerlinck et al. ACCV2018](#Scheerlinck18accv), *Continuous-time Intensity Estimation Using Event Cameras*. [Website](https://cedric-scheerlinck.github.io/continuous-time-intensity-estimation)
- <a name="Scheerlinck19cvprw"></a>Scheerlinck, C., Rebecq, H., Stoffregen, T., Barnes, N., Mahony, R., Scaramuzza, D.,  
[CED: Color Event Camera Dataset](http://rpg.ifi.uzh.ch/CED.html),  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2019. [Slides](http://rpg.ifi.uzh.ch/docs/CVPR19workshop/CVPRW19_CED_pitch.pdf), [Video pitch](https://youtu.be/BfMjtUQwWnQ).
- [Rebecq et. al. TPAMI 2020](#Rebecq20tpami),  
*High Speed and High Dynamic Range Video with an Event Camera*. [Project page](http://rpg.ifi.uzh.ch/E2VID/)

### Visual Odometry and SLAM
- [Combined Dynamic Vision / RGB-D Dataset](http://ebvds.neurocomputing.systems/EBSLAM3D/index.html) associated to the paper [Weikersdorfer et. al. ICRA 2014](#Weikersdorfer14icra).
- Barranco, F., Fermüller, C., Aloimonos, Y.,  
*[A Dataset for Visual Navigation with Neuromorphic Methods](https://dx.doi.org/10.3389%2Ffnins.2016.00049),*  
Front. Neurosci. (2016), 10:49.
- <a name="Mueggler17ijrr"></a>E. Mueggler, H. Rebecq, G. Gallego, T. Delbruck, D. Scaramuzza,  
*[The Event-Camera Dataset and Simulator: Event-based Data for Pose Estimation, Visual Odometry, and SLAM](http://rpg.ifi.uzh.ch/davis_data.html),*  
Int. J. Robotics Research, 36:2, pp. 142-149, 2017. [PDF](https://arxiv.org/pdf/1610.08336.pdf), [PDF IJRR](http://dx.doi.org/10.1177/0278364917691115), [YouTube](https://youtu.be/bVVBTQ7l36I), [Dataset](http://rpg.ifi.uzh.ch/davis_data.html).
- <a name="Binas17icmlw"></a>Binas, J., Neil, D., Liu, S.-C., Delbruck, T.,  
*[DDD17: End-To-End DAVIS Driving Dataset](https://www.openreview.net/pdf?id=HkehpKVG-),*  
Int. Conf. Machine Learning, Workshop on Machine Learning for Autonomous Vehicles, 2017. [Dataset](http://sensors.ini.uzh.ch/databases.html)
- <a name="Zhu18mvsec"></a>Zhu, A., Thakur, D., Ozaslan, T., Pfrommer, B., Kumar, V., Daniilidis, K.,  
*[The Multi Vehicle Stereo Event Camera Dataset: An Event Camera Dataset for 3D Perception](https://doi.org/10.1109/LRA.2018.2800793),*  
IEEE Robotics and Automation Letters (RA-L), 3(3):2032-2039, Feb. 2018. [PDF](https://arxiv.org/abs/1801.10202), [Dataset](https://daniilidis-group.github.io/mvsec/), [YouTube](https://youtu.be/9FaUvvzaHW8).
- [Event-based, 6-DOF Camera Tracking from Photometric Depth Maps](http://rpg.ifi.uzh.ch/direct_event_camera_tracking/index.html) associated to the paper [Gallego et. al. PAMI 2018](#Gallego18tpami)
- <a name="Leung18spie"></a>Leung, S., Shamwell, J., Maxey, C., Nothwang, W. D.,  
[Toward a large-scale multimodal event-based dataset for neuromorphic deep learning applications](https://doi.org/10.1117/12.2305504),  
Proc. SPIE 10639, Micro- and Nanotechnology Sensors, Systems, and Applications X, 106391T. [PDF](https://www.researchgate.net/publication/325939343)
- [Event-based, Direct Camera Tracking from a Photometric 3D Map using Nonlinear Optimization](http://rpg.ifi.uzh.ch/direct_event_camera_tracking/index.html) associated to the paper [Bryner et. al. ICRA 2019](#Bryner19icra).
- <a name="Delmerico19icra"></a>Delmerico, J., Cieslewski, T., Rebecq, H., Faessler, M., Scaramuzza, D.,  
[Are We Ready for Autonomous Drone Racing? The UZH-FPV Drone Racing Dataset](http://rpg.ifi.uzh.ch/uzh-fpv.html),  
IEEE Int. Conf. Robotics and Automation (ICRA), 2019. [PDF](http://rpg.ifi.uzh.ch/docs/ICRA19_Delmerico.pdf), [YouTube](https://youtu.be/G5w4ZcEzvoo), [Project page](http://rpg.ifi.uzh.ch/uzh-fpv.html).
- <a name="Lee19icraw"></a>Lee, A. J., Cho, Y., Yoon, S., Shin, Y., Kim, A.,  
[ViViD: Vision for Visibility Dataset](https://sites.google.com/view/dgbicra2019-vivid/),  
IEEE Int. Conf. Robotics and Automation (ICRA) Workshop: Dataset Generation and Benchmarking of SLAM Algorithms for Robotics and VR/AR, 2019.
- [Mitrokhin et. al. IROS 2019](#Mitrokhin19iros).  
*EV-IMO: Motion Segmentation Dataset and Learning Pipeline for Event Cameras*

### Segmentation
- [Mitrokhin et. al. IROS 2018](#Mitrokhin18iros), Extreme Event Dataset (EED). [Project page and Dataset](http://prg.cs.umd.edu/BetterFlow.html)
- <a name="Mitrokhin19iros"></a>Mitrokhin, A., Ye, C., Fermüller, C., Aloimonos, Y., Delbrück, T.,  
*[EV-IMO: Motion Segmentation Dataset and Learning Pipeline for Event Cameras](https://doi.org/10.1109/IROS40897.2019.8968520)*,  
IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), 2019. [PDF](https://arxiv.org/pdf/1903.07520.pdf), [Dataset](https://better-flow.github.io/evimo), [Project page](http://prg.cs.umd.edu/EV-IMO.html)

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
- <a name="Liu16fnins"></a>Liu, Q., Pineda-García, G., Stromatias, E., Serrano-Gotarredona, T., Furber, SB.,  
*[Benchmarking Spike-Based Visual Recognition: A Dataset and Evaluation](https://doi.org/10.3389/fnins.2016.00496)*,  
Front. Neurosci. (2016), 10:496. [Dataset](https://github.com/qian-liu/benchmarking), [Dataset](https://github.com/NEvision/NE15)
- <a name="dvsgesture_dataset"></a>[DVS128 Gesture Dataset](http://research.ibm.com/dvsgesture/): The dataset that was used to build the real-time gesture recognition system described in [Amir et al. CVPR 2017](#Amir17cvpr).
- <a name="ncars_dataset"></a>[N-CARS Dataset](http://www.prophesee.ai/dataset-n-cars/): A large real-world event-based dataset for car classification.     [Sironi et al. CVPR 2018](#Sironi18cvpr).
- [Mitrokhin et. al. IROS 2018](#Mitrokhin18iros) *Event-based Moving Object Detection and Tracking*. [Project page and Dataset](http://prg.cs.umd.edu/BetterFlow.html)
- <a name="atisplanesdataset"></a>[ATIS Plane Dataset](https://www.westernsydney.edu.au/bens/home/reproducible_research/atis_planes), assocated to the paper [Afshar et al., Front. Neurosci. 2018](#Afshar18fnins).    
- <a name="Cheng19cvprw"></a>Cheng, W., Luo, H., Yang, W., Yu, L., Chen, S., Li, W.,  
*[DET: A High-resolution DVS Dataset for Lane Extraction](http://openaccess.thecvf.com/content_CVPRW_2019/papers/EventVision/Cheng_DET_A_High-Resolution_DVS_Dataset_for_Lane_Extraction_CVPRW_2019_paper.pdf),*  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2019. [Project page](https://spritea.github.io/DET/).
- <a name="Miao19fnbot"></a>Miao, S., Chen, G., Ning, X., Zi, Y., Ren, K., Bing, Z., Knoll, A.,  
*[Neuromorphic Vision Datasets for Pedestrian Detection, Action Recognition, and Fall Detection](https://doi.org/10.3389/fnbot.2019.00038),*  
Front. Neurorobot. (2019). [Dataset](https://github.com/MSZTY/PAFBenchmark)
- <a name="deTournemire20arxiv"></a>de Tournemire, P., Nitti, D., Perot, E., Migliore, D., Sironi, A.,  
*[A Large Scale Event-based Detection Dataset for Automotive](https://arxiv.org/abs/2001.08499)*,  
arXiv, 2020. [Code](https://github.com/prophesee-ai/prophesee-automotive-dataset-toolbox), [News](https://www.prophesee.ai/2020/01/24/prophesee-gen1-automotive-detection-dataset/)
- [N-SOD Dataset](https://drive.google.com/drive/folders/10_bnZ_TOcq7xCtCiDcaDiIO3_Txgr19S) associated to the paper [Ramesh et al. FNINS 2020](#Ramesh20fnins).


<br><br>
<a name="software"></a>
# Software

<a name="drivers"></a>
## Drivers
- [jAER (java Address-Event Representation) project](http://jaerproject.org/). *Real time sensory-motor processing for event-based sensors and systems*. [github page](https://github.com/SensorsINI/jaer). [Wiki](https://sourceforge.net/p/jaer/wiki/Home/)
- [caer (AER event-based framework, written in C, targeting embedded systems)](https://github.com/inilabs/caer)
- [libcaer (Minimal C library to access, configure and get/send AER data from sensors or to/from neuromorphic processors)](https://github.com/inilabs/libcaer)
- [evl (Open Source Computer Vision Library for Event-based camera and vision for C++)](https://github.com/EventVisionLibrary/evl)
- [ROS (Robotic Operating System)](https://github.com/uzh-rpg/rpg_dvs_ros)
- [YARP (Yet Another Robot Platform)](https://github.com/robotology/event-driven)
- [Prophesee ROS Wrapper](https://github.com/prophesee-ai/prophesee_ros_wrapper) ROS driver and messages for Prophesee event-based sensors

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
- <a name="Song18wrcsara"></a>Song, R., Jiang, Z., Li, Y., Shan, Y., Huang, K.,  
*[Calibration of Event-based Camera and 3D LiDAR](https://doi.org/10.1109/WRC-SARA.2018.8584215)*,  
WRC Symposium on Advanced Robotics and Automation (WRC SARA), 2018.
- <a name="DominguezMorales19access"></a>Dominguez-Morales, M. J., Jimenez-Fernandez, A., Jimenez-Moreno, G., Conde, C., Cabello, E., Linares-Barranco, A.,  
*[Bio-Inspired Stereo Vision Calibration for Dynamic Vision Sensors](https://doi.org/10.1109/ACCESS.2019.2943160)*,  
IEEE Access, vol. 7, pp. 138415-138425, 2019.


<a name="software-algorithms"></a>
## Algorithms
- [Several event-processing filters](https://sourceforge.net/p/jaer/wiki/FilterIndex_1/) in the [jAER (java Address-Event Representation) project](http://jaerproject.org/)
- [A collection of tracking and detection algorithms](https://github.com/robotology/event-driven) using the YARP framework
- [Some detection and tracking algorithms](https://github.com/EventVisionLibrary/evl) in EVL
- **Optical Flow**
    - [LocalPlanesFlow](https://sourceforge.net/p/jaer/code/HEAD/tree/jAER/trunk/src/ch/unizh/ini/jaer/projects/rbodo/opticalflow/LocalPlanesFlow.java), inspired by the paper [Benosman et. al. TNNLS 2014](#Benosman14tnnls).
    - [Several algorithms compared](https://sourceforge.net/p/jaer/code/HEAD/tree/jAER/trunk/src/ch/unizh/ini/jaer/projects/rbodo/opticalflow/) in the paper by [Rueckauer and Delbruck, FNINS 2016](#Rueckauer16fnins).
    - [Event-Lifetime estimation](https://www.github.com/uzh-rpg/rpg_event_lifetime), associated to the paper [Mueggler et. al. ICRA 2015](#Mueggler15icra).
    - [EV-FlowNet](https://github.com/daniilidis-group/EV-FlowNet), associated to the paper [Zhu et. al. RSS 2018](#Zhu18rss).
- **Feature Tracking**
    - [Event-based Feature Tracking with Probabilistic Data Association](https://github.com/daniilidis-group/event_feature_tracking), associated to the papers [Zhu et. al. ICRA 2017](#Zhu17icra) and [Zhu et. al. CVPR 2017](#Zhu17cvpr).
    - [Tracking code](https://github.com/uzh-rpg/rpg_eklt) associated to the paper [Gehrig et al. IJCV 2019]("#Gehrig19ijcv)".
    - [Evaluation code](https://github.com/uzh-rpg/rpg_feature_tracking_analysis) associated to the paper [Gehrig et al. IJCV 2019]("#Gehrig19ijcv)".
- **Intensity-Image reconstruction from events**
    - [Code for intensity reconstruction](https://github.com/uzh-rpg/rpg_image_reconstruction_from_events), inspired by the paper [Kim et. al. BMVC 2014](#Kim14bmvc).
    - [DVS Reconstruction code](https://github.com/VLOGroup/dvs-reconstruction) associated to the paper [Reinbacher et. al. BMVC 2016](#Reinbacher16bmvc).
    - [High-pass filter code](https://github.com/cedric-scheerlinck/dvs_image_reconstruction) associated to the paper [Scheerlinck et al. ACCV 2018](#Scheerlinck18accv)
    - [E2VID code](https://github.com/uzh-rpg/rpg_e2vid) associated to the paper [Rebecq et al. TPAMI 2020](#Rebecq20tpami).
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
- [Loris](https://github.com/neuromorphic-paris/loris) Python package to read files from neuromorphic cameras.
- Marcireau A., Ieng S.-H., Benosman R.,  
*[Sepia, Tarsier, and Chameleon: A Modular C++ Framework for Event-Based Computer Vision](https://doi.org/10.3389/fnins.2019.01338)*,  
Front. Neurosci. (2020), 13:1338. [Code](https://github.com/neuromorphic-paris/tutorials)

<br><br>
<a name="processors-platforms"></a>
# Neuromorphic Processors and Platforms
- <a name="Hofstaetter11icecs"></a>Hoffstaetter, M., Belbachir, N., Bodenstorfer, E., Schoen, P.,  
*[Multiple Input Digital Arbiter with Timestamp Assignment for Asynchronous Sensor Arrays](https://doi.org/10.1109/ICECS.2006.379767)*,  
IEEE Int. Conf. Electronics, Circuits and Systems (ICECS), 2006.
- <a name="Belbachir08icecs"></a>Belbachir, A., Hofstaetter, M., Reisinger, K., Litzenberger, M., Schoen, P.,  
*[High-Precision Timestamping and Ultra High-Speed Arbitration of Transient Pixels' Events](https://doi.org/10.1109/ICECS.2008.4674996)*,  
Int. Conf. on Electronics, Circuits and Systems (ICECS), 2008.
- <a name="Hofstaetter09biocas"></a>Hoffstaetter, M., Schoen, P., Posch, C.,  Bauer, D.,  
*[An integrated 20-bit 33/5M events/s AER sensor interface with 10ns time-stamping and hardware-accelerated event pre-processing](https://doi.org/10.1109/BIOCAS.2009.5372034)*,  
IEEE Biomedical Circuits and Systems Conference (BioCAS), 2009.
- <a name="Hofstaetter11icecs"></a>Hoffstaetter, M., Litzenberger, M., Matolin, D., Posch, C.,  
*[Hardware-accelerated address-event processing for high-speed visual object recognition](https://doi.org/10.1109/ICECS.2011.6122221)*,  
IEEE Int. Conf. Electronics, Circuits, and Systems (ICECS), 2011.
- [Dynamic Neuromorphic Asynchronous Processor (DYNAP) by aiCTX AG](https://ai-ctx.com/products/dynap/)
  - <a name="Qiao15fnins"></a>Qiao, N., Mostafa, H., Corradi, F., Osswald, M., Stefanini, F., Sumislawska, D., Indiveri, G.,  
  *[A reconfigurable on-line learning spiking neuromorphic processor comprising 256 neurons and 128K synapses](https://doi.org/10.3389/fnins.2015.00141),*  
  Front. Neurosci. (2015), 9:141. [PDF](https://capocaccia.ethz.ch/capo/raw-attachment/wiki/2015/hybrid15/frontiers14-nlp.pdf)
  - <a name="Indiveri15iedm"></a>Indiveri, G., Qiao, N., Corradi, F.,  
  *[Neuromorphic Architectures for Spiking Deep Neural Networks](https://doi.org/10.1109/IEDM.2015.7409623)*,  
  IEEE Int. Electron Devices Meeting (IEDM), 2015. [PDF](http://ncs.ethz.ch/pubs/pdf/Indiveri_etal15.pdf)
- <a name="Wiesmann12cvprw"></a>Wiesmann, G., Schraml, S., Litzenberger, M., Belbachir, A. N., Hofstatter, M., Bartolozzi, C.,  
*[Event-driven embodied system for feature extraction and object recognition in robotic applications](https://doi.org/10.1109/CVPRW.2012.6238898),*  
IEEE Conf. Computer Vision and Pattern Recognition Workshops (CVPRW), 2012.
- <a name="Galluppi14icra"></a>Galluppi, F., Denk, C., Meiner, M. C., Stewart, T. C., Plana, L. A., Eliasmith, C., Furber, S., Conradt, J.,  
*[Event-based neural computing on an autonomous mobile platform](https://doi.org/10.1109/ICRA.2014.6907270),*  
IEEE Int. Conf. Robotics and Automation (ICRA), 2014. [PDF](http://compneuro.uwaterloo.ca/files/publications/galluppi.2014.pdf)
- <a name="Graf14CSEDU"></a>Graf, R., King, R., Belbachir, A.,  
*[Braille Vision Using Braille Display and Bio-inspired Camera](http://dx.doi.org/10.5220/0004949302140219)*,  
Int. Conf. Computer Supported Education (CSEDU), SCITEPRESS Digital Library, (2014), pp. 214 - 219.


<br><br>
<a name="workshops"></a>
# Workshops and Tutorials
- [ICRA 2015 Workshop on Innovative Sensing for Robotics](http://innovative-sensing.mit.edu/), with a focus on Neuromorphic Sensors.
- [IROS 2015 Event-Based Vision for High-Speed Robotics (slides)](http://www.rit.edu/kgcoe/iros15workshop/papers/IROS2015-WASRoP-Invited-04-slides.pdf), Workshop on Alternative Sensing for Robot Perception.
- [ICRA 2017 First International Workshop on Event-based Vision](http://rpg.ifi.uzh.ch/ICRA17_event_vision_workshop.html) - Slides and Videos available on the website.
    - [Videos](https://www.youtube.com/playlist?list=PLeXWz-g2If94k8mw6GcKU5C9PUgM1sK0U)
- [IROS 2018 Unconventional Sensing and Processing for Robotic Visual Perception](https://www.jmartel.net/irosws-home).
- [CVPR 2019 Second International Workshop on Event-based Vision and Smart Cameras](http://rpg.ifi.uzh.ch/CVPR19_event_vision_workshop.html) - Slides and Videos available on the website.
    - [Videos](https://www.youtube.com/playlist?list=PLeXWz-g2If97iGiuBHmnW8IFIxwvSeCHx)
- [The Telluride Neuromorphic Cognition Engineering Workshops](http://telluride.iniforum.ch/accounts/login/?next=/).
    - [Videos](https://sites.google.com/view/telluride2020/about-workshop/videos)
- [Capo Caccia Workshops toward Cognitive Neuromorphic Engineering](http://capocaccia.iniforum.ch/).
- [IEEE Embedded Vision Workshop Series](https://embeddedvisionworkshop.wordpress.com), with focus on Biologically-inspired vision and embedded systems.
- [Neuro-Inspired Computational Elements (NICE) Workshop Series](https://niceworkshop.org/nice-2019/)
    - [Videos](https://www.youtube.com/channel/UCKTLpjY9e8cMK12d2-Z-usA)


<br><br>
<a name="theses"></a>
# Theses and Dissertations

<a name="theses-phd"></a>
## Dissertations
- <a name="Mahowald92PhD"></a>Mahowald, M.,  
*[VLSI Analogs of Neuronal Visual Processing: A Synthesis of Form and Function](http://resolver.caltech.edu/CaltechTHESIS:09122011-094355148)*,  
Ph.D. thesis, California Inst. Of Technology, Pasadena, CA, 1992. [PDF](http://www.ini.uzh.ch/~tobi/papers/mishathesis.pdf)  
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
- <a name="Kogler16PhD"></a>Kogler, J.,  
*[Design and evaluation of stereo matching techniques for silicon retina cameras](https://resolver.obvsg.at/urn:nbn:at:at-ubtuw:1-2178)*,  
Ph.D. Thesis, Technische Universität Wien, Vienna, Austria, 2016. [PDF](http://repositum.tuwien.ac.at/obvutwhs/download/pdf/1310930?originalFilename=true)
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
- <a name="Huang18PhD"></a>Huang, J.,  
*[Asynchronous high-speed feature extraction image sensor (CelePixel)](http://hdl.handle.net/10220/46625)*,  
Ph.D. Thesis, Nanyang Technological University, Singapore, 2018.
- <a name="Gibson18PhD"></a>Gibson, T. T.,  
*[Inspired by nature: timescale-free and grid-free event-based computing with spiking neural networks](https://doi.org/10.14264/uql.2018.664)*,  
Ph.D. Thesis, The University of Queensland, Brisbane, Australia, 2018.
- <a name="Martel19PhD"></a>Martel, J.,  
*[Unconventional Processing with Unconventional Visual Sensing. Parallel, Distributed and Event Based Vision Algorithms & Systems](https://doi.org/10.3929/ethz-b-000362900)*,  
Ph.D. Thesis, ETH Zurich, Zurich, Switzerland, 2019.
- <a name="Bardow19PhD"></a>Bardow, P. A.,  
*[Estimating General Motion and Intensity from Event Cameras](https://www.doc.ic.ac.uk/~ajd/Publications/Bardow-P-2019-PhD-Thesis.pdf)*,  
Ph.D. Thesis, Imperial College London, United Kingdom, 2019.
- <a name="Ye19PhD"></a>Ye, C.,  
*[Learning of Dense Optical Flow, Motion and Depth, from Sparse Event Cameras](https://doi.org/10.13016/fhqf-g7xr)*,  
Ph.D. Thesis, University of Maryland, USA, 2019.
- <a name="Zhu19PhD"></a>Zhu, A. Z.,  
*[Event-Based Algorithms for Geometric Computer Vision](https://repository.upenn.edu/edissertations/3566)*,  
Ph.D. Thesis, University of Pennsylvania, USA, 2019.
- See also [Theses from Delbruck's group at INI](https://www.ini.uzh.ch/~tobi/wiki/doku.php?id=publications#phd_thesis)


<a name="theses-master"></a>
## Master's (and Bachelor's) Theses
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
- <a name="Kaelber16BS"></a>Kaelber, F., (Everding, L, Conradt, J.,)    
*[A probabilistic method for event stream registration](https://mediatum.ub.tum.de/doc/1327653/1327653.pdf)*,  
Bacherlor Thesis, TU Munich, 2016.
- <a name="Galanis16BS"></a>Galanis, M., (Everding, L, Conradt, J.,)    
*[DVS event stream registration](https://mediatum.ub.tum.de/doc/1367575/1367575.pdf)*,  
Bacherlor Thesis, TU Munich, 2016.
- <a name="Nelson19MSc"></a>Nelson, K. J.,  
*[Event-Based Visual-Inertial Odometry on a Fixed-Wing Unmanned Aerial Vehicle](https://apps.dtic.mil/docs/citations/AD1076268)*,  
MSc. Thesis, Air Force Institute of Technology, USA, 2019. [PDF](https://apps.dtic.mil/dtic/tr/fulltext/u2/1076268.pdf)
- <a name="Attanasio19MSc"></a>Attanasio, G.,  
*[Event-based camera communications: a measurement-based analysis](https://webthesis.biblio.polito.it/11693/1/tesi.pdf)*,  
MSc. Thesis, Politecnico di Torino, 2019.
- <a name="Wang19MSc"></a>Wang, Z.,  
*[Motion Equivariance of Event-based Camera Data with the Temporal Normalization Transform](https://arxiv.org/pdf/1911.12801)*,  
MSc. Thesis, University of Pennsylvania, 2019.


<br><br>
<a name="people"></a>
# People / Organizations
- [Institute of NeuroInformatics](https://www.ini.uzh.ch/) (INI) of the University of Zurich (UZH) and ETH Zurich, Switzerland.
- [iniVation AG](https://www.inivation.com/) (commercialization of neuromorphic vision technology from INI), Switzerland.
- [Dynamic Vision Sensor (DVS) - asynchronous temporal contrast silicon retina](http://siliconretina.ini.uzh.ch/wiki/index.php)
- [Robotics and Perception Group](http://rpg.ifi.uzh.ch/research_dvs.html) of the University of Zurich (UZH) and ETH Zurich, Switzerland.
- [Institut de la Vision](http://neuromorphic-vision.com/) Neuromorphics group Paris, France.
- [GRASP Lab](https://www.grasp.upenn.edu/) at University of Pennsylvania, [Kostas Daniilidis](http://www.cis.upenn.edu/~kostas/).
- [AIT Austrian Institute of Technology](https://www.ait.ac.at/en/research-fields/new-sensor-technologies/) Sensing & vision solutions group in Vienna, Austria.
- [Event-Driven Perception for Robotics (EDPR)](https://www.edpr.iit.it) group at Istituto Italiano di Tecnologia (IIT), Italy.
- [Sinapse](http://sinapse.nus.edu.sg/) Singapore Institute for Neurotechnology, Singapore.
- [Western Sydney University’s International Centre for Neuromorphic Systems (ICNS)](https://www.westernsydney.edu.au/icns), Australia.
- [Perception and Robotics Group](http://prg.cs.umd.edu/) at University of Maryland (UMD). [Fermüller's Lab on Event-based vision](http://users.umiacs.umd.edu/~fer/dvs.html)
- [Intel Labs](https://www.intel.com/content/www/us/en/research/overview.html), [Mike Davies](https://newsroom.intel.com/news/bobbleheads-tool-test-neuromorphic-mind/#gs.nndw9d) (Intel’s neuromorphic computing program leader).
  - [Video CVPRW 2019](https://youtu.be/jhQgElvtb1s),  [Video Intel NICE 2018 Loihi](https://vimeo.com/264342847),  [Video Intel NICE 2018 Day 3](https://vimeo.com/258246382).
- [Robotics and Technology of Computers Lab - Sevilla (RTC)](http://www.rtc.us.es/) of the University of Seville (USE), Seville, SPAIN  

<br><br>
<a name="contributing"></a>
# Contributing
Please see [CONTRIBUTING](https://github.com/uzh-rpg/event-based_vision_resources/blob/master/Contributing.md) for details.
***
