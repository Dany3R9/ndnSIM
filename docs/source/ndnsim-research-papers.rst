ndnSIM research papers
======================

Here is a list of ndnSIM-related papers.  If you want your paper to appear in this list, please send an email to our mailing list or to us directly.

General papers about ndnSIM
---------------------------

.. note::
    if you refer to ndnSIM in a published work, please cite this paper, not just the ndnSIM website

- **A. Afanasyev, I. Moiseenko, and L. Zhang, "ndnSIM: NDN simulator for NS-3," NDN, Technical Report NDN-0005, 2012** (`PDF <http://named-data.net/techreport/TR005-ndnsim.pdf>`_, `BibTex <http://lasr.cs.ucla.edu/afanasyev/bibwiki/bibtex/367>`_)

    Named Data Networking (NDN) is a newly proposed Internet architecture.
    NDN retains the Internet's hourglass architecture but evolves the thin waist.
    Instead of pushing data to specific locations, NDN retrieves data by name.
    On one hand, this simple change allows NDN networks to use almost all of the Internet's well tested engineering properties to solve not only IP's communication problems but also digital distribution and control problems.
    On the other hand, a distribution architecture differs in fundamental ways from a point-to-point communication architecture of today's Internet and raises many new research challenges.
    Simulation can serve as a flexible tool to examine and evaluate various aspects of this new architecture.
    To provide the research community at large with a common simulation platform, we have developed an open source NS-3 based simulator, ndnSIM, which faithfully implemented the basic components of a NDN network in a  modular way.
    This paper provides an overview of ndnSIM.


Research papers that use ndnSIM
-------------------------------

#. **L. Wang, A. Afanasyev, R. Kuntz, R. Vuyyuru, R. Wakikawa, and L. Zhang, "Rapid Traffic Information Dissemination Using Named Data," in Proceedings of the 1st ACM workshop on Emerging Name-Oriented Mobile Networking Design - Architecture, Algorithms, and Applications (NoM'12), Hilton Head Island, South Carolina, June 2012, pp. 7–12.** (`PDF <http://lasr.cs.ucla.edu/afanasyev/data/files/Wang/nom.pdf>`_, `BibTex <http://lasr.cs.ucla.edu/afanasyev/bibwiki/bibtex/365>`_, `simulation code <https://github.com/cawka/ndnSIM-nom-rapid-car2car>`_)

    Our previous work applied the Named Data Networking approach to vehicle-to-vehicle (V2V) communications and developed a simple design for traffic information dissemination applications. This paper uses simulations to evaluate the feasibility of the design as described in [1].
    Our results show that data names can greatly facilitate the forwarding process for Interest and data packets.
    With adequate vehicle density, data can propagate over long distances robustly at tens of kilometers per second and a requester can retrieve the desired traffic information 10km away in a matter of seconds.

#. **Z. Zhu, C. Bian, A. Afanasyev, V. Jacobson, and L. Zhang, "Chronos: Serverless Multi-User Chat Over NDN," NDN, Technical Report NDN-0008, 2012.** (`PDF <http://named-data.net/techreport/TR008-chronos.pdf>`_, `BibTex <http://lasr.cs.ucla.edu/afanasyev/bibwiki/bibtex/371>`_)

    Multi-user applications are commonly implemented using a centralized server.
    This paper presents a new design for multi-user chat applications (Chronos) that works in a distributed, serverless fashion over Named Data Networking.
    In Chronos, all participants share their views by exchanging the cryptographic digests of the chat room data set.
    A newly generated message causes a change of the digest at the message originator, which leads to retrieving the new data by all other participants in an efficient way and resynchronization of chat room views.
    Chronos does not have a single point of failure and eliminates traffic concentration problem of server-based implementations.
    We use simulations to evaluate and compare Chronos with a traditional server-based chat room implementation.
    Our results demonstrate Chronos' robustness and efficiency in data dissemination.
    Chronos' approach of replacing centralized servers by distributed data synchronization can be applied to a variety of distributed applications to simplify design and ease deployment.

#. **M. Vahlenkamp, "Threats on Information-Centric Networking", Hamburg University of Applied Sciences, Technical Report, 2012.** (`PDF <http://inet.cpt.haw-hamburg.de/teaching/ws-2012-13/master-projekt/markus-vahlenkamp_seminar.pdf>`_)

    The ICN approach aims for reflecting these changes in usage of the Internet and is thus dragging content awareness into the network, for instance to let the network itself decide where to acquire requested data from and thereby utilize content caches to increase the data dissemination efficiency. All this is backed by the use of the publish/subscribe paradigm that is utilised to announce content availability and request its delivery. Since the ICN paradigm is entirely different from todays Internet, new challenges arise within the area of network security. NDN/CCNx, as the most popular ICN approach, claims to solve a couple of different security flaws which the actual Internet is suffering from. This raises the questions of which vulnerabilities still exist and if maybe new issues arise.

#. **C. Yi, A. Afanasyev, I. Moiseenko, L. Wang, B. Zhang, and L. Zhang, "A Case for Stateful Forwarding Plane," Computer Communications, vol. 36, no. 7, pp. 779–791, 2013. ISSN 0140-3664** (`PDF <http://lasr.cs.ucla.edu/afanasyev/data/files/Yi/comcom-stateful-forwarding.pdf>`_, `BibTex <http://lasr.cs.ucla.edu/afanasyev/bibwiki/bibtex/380>`_, `simulation code <https://github.com/cawka/ndnSIM-comcom-stateful-fw>`_)

    In Named Data Networking (NDN), packets carry data names instead of source and destination addresses.
    This paradigm shift leads to a new network forwarding plane: data consumers send *Interest* packets to request desired data, routers forward Interest packets and maintain the state of all pending Interests, which is then used to guide *Data* packets back to the consumers.
    Maintaining the pending Interest state, together with the two-way Interest and Data exchange, enables NDN routers' *forwarding* process to measure performance of different paths, quickly detect failures and retry alternative paths.
    In this paper we describe an initial design of NDN's forwarding plane and evaluate its data delivery performance under adverse conditions.
    Our results show that this stateful forwarding plane can successfully circumvent prefix hijackers, avoid failed links, and utilize multiple paths to mitigate congestion.
    We also compare NDN's performance with that of IP-based solutions to highlight the advantages of a stateful forwarding plane.

#. **A. Afanasyev, P. Mahadevan, I. Moiseenko, E. Uzun, and L. Zhang, "Interest Flooding Attack and Countermeasures in Named Data Networking," in Proc. of IFIP Networking 2013, May 2013.** (`PDF <http://lasr.cs.ucla.edu/afanasyev/data/files/Afanasyev/ifip-interest-flooding-ndn.pdf>`_, `BibTex <http://lasr.cs.ucla.edu/afanasyev/bibwiki/bibtex/381>`_, `simulation code <https://github.com/cawka/ndnSIM-ddos-interest-flooding>`_)

    Distributed Denial of Service (DDoS) attacks are an ongoing problem in today's Internet, where packets from a large number of compromised hosts thwart the paths to the victim site and/or overload the victim machines.
    In a newly proposed future Internet architecture, Named Data Networking (NDN), end users request desired data by sending Interest packets, and the network delivers Data packets upon request only, effectively eliminating many existing DDoS attacks.
    However, an NDN network can be subject to a new type of DDoS attack, namely Interest packet flooding.
    In this paper we investigate effective solutions to mitigate Interest flooding.
    We show that NDN's inherent properties of storing per packet state on each router and maintaining flow balance (i.e., one Interest packet retrieves at most one Data packet) provides the  basis for effective DDoS mitigation algorithms.
    Our evaluation through simulations shows that the solution can quickly and effectively respond and mitigate Interest flooding.

#. **B. Zhou, C. Wu, X. Hong, and M. Jiang, "Algorithms for Distributed Programmable Controllers", Technical Report, March 2013.** (`PDF <http://hong.cs.ua.edu/DCP-techReport-March2013.pdf>`_)

    A few works on SDN (Software-Defined Networking) like those in Onix improve programmability of the distributed network control.
    The asynchronism and Byzantine issues of the control challenge the re-configurability of the service that is to safely program the control in atomic so as to avoid the transient control issues like the routing loops and black holes.
    We propose two important algorithms of the distributed control to enable the programmability: (1) the reconfiguration primitive allows the network control of the services being able to safely react to an external event; and (2) the reuse primitive allows the control states of a service being accessible for all services. We give concepts and algorithms of two primitives.
    In addition, we provide the concrete cases of the current approaches for ICN (Information-Centric Networking) and CDN (Content Distribution Networks) for quests of the reconfigurability and programmability.
    Then, we evaluate the performance of ICN in both simulation and the PlanetLab testbed.
    The evaluation results show that the layer improves the lowers 19.6% of the Interest delays in the ICN that is heavily congested and lowers 97% delays in the PlanetLab with 9 nodes on usual case.
    In addition, the evaluation of CDN on the PlanetLab shows that it reduces 81% request delay on usual case.

#. **M. Tortelli, L. A. Grieco, and G. Boggia, "Performance Assessment of Routing Strategies in Named Data Networking", in Proc. of GTTI 2013 Session on Telecommunication Networks, 2013** (`PDF <http://www.gtti.it/GTTI13/papers/Tortelli_et_al_GTTI2013.pdf>`_)

    Information Centric Networking (ICN) architectures are currently being investigated to orient the Future Internet towards a content centric paradigm, thus allowing the provisioning of more secure, efficient, and scalable services.
    In this work, we focus on the Named Data Networking (NDN) proposal to analyze the impact of several routing and forwarding strategies, which play a fundamental role in ICN.
    In particular, thanks to the recently devised ns-3 based NDN simulator, namely ndnSIM, we conduce an extensive simulation campaign using the GEANT topology as a core network.
    We monitor different distinctive metrics, such as file download time, server load reduction, hit ratio, hit distance, and communication overhead, in different topologies and traffic conditions.
    Simulation results show that the election of a single best forwarding strategy is a difficult task.
    Indeed, the pros and cons of each strategy are heavily influenced by the popularity distribution of contents, which, in turn, affects the effectiveness of the distributed caching mechanisms typically used in the NDN architecture.

#. **S. Seo, J.-M. Kang, A. Leon-Garcia, Y. Han, and J. W.-K. Hong, "Secure and Efficient Context Data Collection using Content-Centric Networking", in Proc. of International Workshop on Smart Communication Protocols and Algorithms (SCPA), 2013** (`PDF <http://dpnm.postech.ac.kr/papers/SCPA/13/sesise/scpa13.pdf>`_)

    Context data collection is a fundamental and important process for realizing context-aware recommender or personalization systems.
    The existing context data collection approaches are based-on traditional TCP/IP that has several disadvantages such as lack of mobility and security.
    On the other hand, Content-Centric Networking (CCN) provides advantages in terms of mobility, security, and bandwidth efficiency compared to TCP/IP.
    In this paper, we propose a secure and efficient context data collection and provision approach based on CCN.
    Simulation results show that this approach can reduce bandwidth consumption by 52.7%–98.9% in comparison to a TCP/IP-based one.

#. **J. Ran, N. Lv, D. Zhang, Y. Ma, and Z. Xie, "On Performance of Cache Policies in Named Data Networking", in International Conference on Advanced Computer Science and Electronics Information (ICACSEI 2013), 2013** (`PDF <http://www.atlantis-press.com/php/download_paper.php?id=7640>`_)

    Named Data Network (NDN) is gaining increasingly concerns, as an important direction of the future Internet architecture research centered on content.
    Content caching has played a key role in NDN.
    Existing cache replacement policies like Least Frequently Used (LFU) and Least Recently Used (LRU) have failed to make full use of the popularity of contents, which leads to a low cache efficiency in the dynamic network.
    In order to make the best use of content popularity in the cache strategy, this paper has proposed a cache replacement policy based on content popularity (CCP), and designed the data structure format and replacement algorithm.
    For fully studying and analyzing the performance of different cache policies in NDN in terms of network throughput, server load and cache hit ratio, we have done a lot of simulations to show how they will improve the network.
    The simulation results show that our proposed CCP can significantly decrease the server load with a higher cache hit ratio and increase the network capacity at the same time compared with LRU and LFU.
    And the average throughput is reduced significantly by nearly 47% in comparison to that of the case without in-networking caching.
    Moreover, it also shows the performance under different sizes of content store.
    The effectiveness of the CCP strategy is proved during the simulation.

#. **M. Wahlisch, T.C. Schmidt, and M. Vahlenkamp, "Backscatter from the Data Plane--Threats to Stability and Security in Information-Centric Network Infrastructure", in Computer Networks, 2013** (`DOI 10.1016/j.comnet.2013.07.009 <http://dx.doi.org/10.1016/j.comnet.2013.07.009>`_)

    Information-centric networking (ICN) raises data objects to first class routable entities in the network and changes the Internet paradigm from host-centric connectivity to data-oriented delivery.
    However, current approaches to content routing heavily rely on data-driven protocol events and thereby introduce a strong coupling of the control to the data plane in the underlying routing infrastructure.
    In this paper, threats to the stability and security of the content distribution system are analyzed in theory, simulations, and practical experiments.
    We derive relations between state resources and the performance of routers, and demonstrate how this coupling can be misused in practice.
    We further show how state-based forwarding tends to degrade by decorrelating resources.
    We identify intrinsic attack vectors present in current content-centric routing, as well as possibilities and limitations to mitigate them.
    Our overall findings suggest that major architectural refinements are required prior to global ICN deployment in the real world.

#. **Xiaoke Jiang and Jun Bi, "Technical Report: Named Content Delivery Network", 2013** (`PDF <http://netarchlab.tsinghua.edu.cn/~shock/THU-NetArchLab-ICN-TR-nCDN-20130730.pdf>`_)

    CDN (Content Delivery Network) focuses on delivering requested data to users, no matter where the data comes from; but the fundamental goal of IP is to connect hosts.
    The essential mismatching leads to complexity and inefficiency.
    More specifically,
    1) CDN has to build components to map what to where, which is resource consuming;
    2) CDN has to monitor real-time network state on the application layer, which is complex and not accurate.
    In contrast, NDN (Named Data Networking), provides the information and function that traditional CDN devotes a great deal of effort to achieve, since NDN routes by name, its routing plane holds the "what", information of content distribution, and its stateful forwarding plane can detect and adapt to dynamic of the Internet.
    Thus this work enhances current CDN with NDN, here dubbed Named Content Delivery Network, or nCDN.
    In nCDN, CDN itself focuses on services such as accounting, data analysis etc; NDN runs over IP and takes charge of content routing and delivery.
    nCDN is more adaptive to the dynamic of the Internet and improves the performance, especially in a scenario where content copies are hosted in several hosts.
    nCDN makes it easier to implement optimization solutions and CDN Interconnecting. Our simulations demonstrate that nCDN is better than traditional CDN on almost all aspects, including the scalability, reliability, and QoS.

#. **Xiaoke Jiang, Jun Bi, Youchao Wang, and You Wang, "Interest Set Mechanism to Improve the Transport of Named Data Networking", in proceedings of ACM SIGCOMM13 (poster), Hongkong, China, 2013** (`PDF <http://netarchlab.tsinghua.edu.cn/~junbi/SIGCOMM2013-1.pdf>`_)

    Named Data Networking (NDN) is currently a hot research topic promising to be one of the most advanced developments in future Internet architectures. 
    Researches have built real software systems over NDN which work on speciﬁed scenarios. 
    In this paper, we proposal an new mechanism which aggregate similar Interest packets to improve the efficient of transport of NDN. 
    Firstly we prove the optimal chunk size which simultaneously minimize the latency and maximize the valid payload ratio during a complete data acquiring process. 
    That's why we aggregate the Interest packet but not increase the size of Data packet. 
    Secondly we introduce the Interest Set mechanism that which is able to maintain a conversational "channel" between the data consumer and provider to cover the space and time uncertainty of data packet generating and at the same time reduces the number of FIB lookups and compresses the PIT.

#. **Z. Zhu and A. Afanasyev, "Let's ChronoSync: Decentralized Dataset State Synchronization in Named Data Networking," in Proceedings of the 21st IEEE International Conference on Network Protocols (ICNP 2013), Goettingen, Germany, October 2013** (`PDF <http://lasr.cs.ucla.edu/afanasyev/data/files/Zhu/chronosync-icnp2013.pdf>`_)

    In supporting many distributed applications, such as group text messaging, file sharing, and joint editing, a basic requirement is the efficient and robust synchronization of knowledge about the dataset such as text messages, changes to the shared folder, or document edits. 
    We propose ChronoSync protocol, which exploits the features of the Named Data Networking architecture to efficiently synchronize the state of a dataset among a distributed group of users. 
    Using appropriate naming rules, ChronoSync summarizes the state of a dataset in a condensed cryptographic digest form and exchange it among the distributed parties.
    Differences of the dataset can be inferred from the digests and disseminated efficiently to all parties.  
    With the complete and up-to-date knowledge of the dataset changes, applications can decide whether or when to fetch which pieces of the data.
    We implemented ChronoSync as a C++ library and developed two distributed application prototypes based on it.
    We show through simulations that ChronoSync is effective and efficient in synchronization dataset state, and is robust against packet losses and network partitions.

#. **Y. Wang, N. Rozhnova, A. Narayanan, D. Oran, and I. Rhee, "An improved hop-by-hop interest shaper for congestion control in named data networking". In Proceedings of the 3rd ACM SIGCOMM workshop on Information-centric networking, 2013** (`PDF <http://conferences.sigcomm.org/sigcomm/2013/papers/icn/p55.pdf>`_)

    Hop-by-hop interest shaping has been proposed as a viable congestion control mechanism in Named Data Networking (NDN). 
    Interest shaping exploits the strict receiver-driven traffc pattern and the symmetric bidirectional forwarding in NDN to control the returning data rate. 
    In this paper, we point out that both interests and contents contribute to congestion and their interdependence must be considered in any interest shaping algorithm. 
    We first analyze this issue mathematically by formulating it as an optimization problem to obtain the optimal shaping rate. 
    Then a practical interest shaping algorithm is proposed to achieve high link utilization without congestive data loss. 
    We further note that ﬂow differentiation in NDN is complicated and design our scheme independently of traffc ﬂows. 
    We demonstrate our hopby-hop interest shaper in conjunction with simple AdditiveIncrease-Multiplicative-Decrease (AIMD) clients using the ns3-based NDN simulator (ndnSIM). 
    Our results show that the proposed shaping algorithm can effectively control congestion and achieve near-optimal throughput.

#. **S. Arianfar, P. Sarolahti, and J. Ott, "Deadline-based Resource Management for Information-Centric Networks". In Proceedings of the 3rd ACM SIGCOMM workshop on Information-centric networking, 2013** (`doi 10.1145/2491224.2491226 <http://dx.doi.org/10.1145/2491224.2491226>`_)

    Unlike in traditional IP-based end-to-end network sessions, in information-centric networks the data source may change during a communication session.
    Therefore the response time to subsequent data requests may vary signiﬁcantly depending on whether data comes from nearby cache, or a distant source.
    This is a complication for designing resource management, reliability and other algorithms, that traditionally use RTT measurements for determining when data is considered lost and should be retransmitted (along with related congestion control adjustments). 
    This paper discusses a different approach for designing resource management in information-centric networks: data packets are assigned with a lifetime, that is used as a basis for scheduling and resource management in the network, and for congestion control and retransmission logic at the end hosts. 
    We demonstrate an initial evaluation of this approach based on ns-3 simulations on CCN framework
