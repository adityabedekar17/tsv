# TSV
## A repository for a blog on Through Silicon Via (TSV)
## Introduction
As the industry proceeds to move from 2-D to 2.5-D and finally 3-D integration of ICs, a major challenge in the integration of these ICs is the packaging methodology used. Traditionally, in order to integrate two different ICs a wire bond was used in a  chiplet setup. These were long wires, with comparable latency to a PCB. It also meant a constraint on the number of wires which could be connected from a particular IC to another. A major drawback of using ‘traditional’ wire bonding is the limit of bandwidth that it can support. Chiplet ICs, and using Through Silicon Vias (TSVs), the length of connections is reduced considerably, while increasing the number of connections it can support.

A major advantage of using TSV is the reduction of the overall package size and power consumption, resembling the advantages of newer process nodes. This is particularly helpful for example in cases like RF and other analog ICs which cannot be scaled down beyond a certain size, due to the inherent way analog ICs function. The advantage of chiplets is that not all ICs need to be scaled down to the latest node. TSV plays a crucial role in enabling this, while also saving costs for companies as some of the ICs could be of older nodes. This is referred to as a System in Package. What distinguishes 2.5D chiplets ( side-by-side chiplets) from 3-D chiplets is: TSVs. TSVs enable stacking of chiplets which form a crucial interconnect technology used to connect chiplets.

## What is TSV
TSV is an electrical connection or interconnect that is used to connect two different dies or interfaces or even carry signals faster within a device. The main advantage of using TSV is the benefits of shorter connections, while also offering a larger number of connections and higher bandwidths, when compared to older methods of connections like wire-bonding.
The image below shows how TSVs are used to connect DRAM dice with a high bandwidth Memory die interface. These connections are vertical and run throughout the dies. The origins of TSV were in the 1980s, which were patented for use by Fujitsu, which described using TSVs in 3D chips. They were used in the MEMS (Microelectromechanical Systems) before eventually being used in Integrated Circuits. Image Source: https://commons.wikimedia.org/wiki/File:High_Bandwidth_Memory_schematic.svg
![High_Bandwidth_Memory_schematic svg](https://github.com/user-attachments/assets/52f5811a-de1a-492a-a8b0-93ef2d99d486)

## Manufacturing Process of TSV
The manufacturing process could be categorized into three major categories: TSV-first, TSV-Middle, and TSV-last, the major difference being the order of which the TSV is fabricated. In TSV-first, the TSVs are fabricated before the individual components are patterned in the front end of line process. In TSV-middle, the TSVs are fabricated after individual components, but before the metal layers like M1, M2 etc. In TSV-last, the TSVs are fabricated after or during the back end of line process. The process includes etching, oxide deposition, barrier and seed layer deposition, 3-D lithography, and Via Filling.
![Through-Silicon_Via_Flavours svg](https://github.com/user-attachments/assets/bbd3e3b4-2b67-4425-87fe-9976ee4cd099)

## Comparision of 2.5D and 3D IC
Both of these techniques use TSVs. TSVs are particularly crucial in 3D ICs as the form factor reduces considerably, while also enabling chiplets like RF and MEMS to have larger form factors ![image](https://github.com/user-attachments/assets/11d3961a-27e5-43a0-8b7e-5cc158b07e89)

## TSV compatible tool flows
- Process Modelling: Source : https://www.lamresearch.com/products/semulator3d/
This simulator is a predictive 3D process modelling platform that helps perform virtual fabrication which saves time and the costs to experiment and implement new process technologies, especially for advanced nodes and architectures like 3D, GAAFET, patterning.
- Modelling and Extraction:  Source : https://www.synopsys.com/manufacturing/tcad/interconnect-simulation/raphael.html
Raphael is intended to be used for analyzing complex on-chip interconnect structures and the influence it has on process variation

- Cadence Design Systems: Source Amongst other solutions, this also is targeted towards extraction of interconnects. It is used to create compact models from silicon layout data for a PDN ( Power Delivery Network) or a signal network.

- 3D Multi-Die Simulator: https://www.ansys.com/applications/3d-ic
Redhawk IC solution has simulation tools for a physics based analysis of electromagnetic, thermal, structural effects of the 3D IC. It is also used to design, simulate and verify Interposers and TSVs. The main advantage, from a primary review, seems to be integration with any EDA tools and flexibility to integrate with other Ansys Products.

- Floorplanning, PnR:  Cadence Innovus: Source: https://community.cadence.com/cadence_blogs_8/b/breakfast-bytes/posts/3dic-webinar
Provides support for Floorplanning and Placement and Routing. Synopsys IC Compiler-II has a similar solution for TSVs. Source: https://www.synopsys.com/implementation-and-signoff/physical-implementation/ic-compiler.html

## Foundries with support for TSVs
- TSMC: TSMC offers CoWoS ( Chip on Wafer on Substrate and SOIC ( System on IC) for 
Enabling 3D stacking. Source : https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/cowos.htm
- Intel:  Foveros by Intel, helps in enabling shorter interconnects by using TSVs. The first generation started with a 10nm process. Source: https://en.wikichip.org/wiki/intel/foveros
- Samsung: Samsung specialises in Memory Chips, and their solution, X-Cube, is the first 3-D SRAM logic for 7nm and beyond. The main advantage of this IP is enabling reliable TSV interconnects at EUV process nodes. Source: https://semiconductor.samsung.com/news-events/news/samsung-announces-availability-of-its-silicon-proven-3d-ic-technology-for-high-performance-applications/#:~:text=Leveraging%20Samsung's%20through%2Dsilicon%20via,well%20as%20mobile%20and%20wearable
- GlobalFoundries: Source : https://gf.com/gf-press-release/globalfoundries-demonstrates-3d-tsv-capabilities-20nm-technology/

 ## TSV : effects of stress and heat
 - Stress
   Some of the major issues with TSVs are thermal and TSV-induced stress. The effects of stress could accumulate in the TSV and get transferred to the transistors it is connected to. A potential solution to this could be using keep out zones which would enable TSVs to be separated from the transistors. However, as the die sizes and the nodes decrease, the Vias’ diameters would reduce as well. With this, the keep out zone would decrease as well, causing considerable challenges in terms of stress. A significant source of thermal stress would be the thermal expansion coefficient mismatch for the different materials used within TSVs, which could cause cracks at the interface with silicon. This makes floorplanning difficult, as TSVs must be distributed in a perfect grid pattern to reduce the risks of warping and cracking.

With newer technologies, steps such as wafer thinning, chip stacking, TSV drilling and filling, solder balls - all of these may potentially manifest as additional sources of stress that can affect the performance of the TSV.  For managing mechanical stresses, instead of using TCAD tools - which have the drawback of not being feasible for larger degrees of freedom, physics-based tools are used instead. Distribution of Stress, Strain, Young’ Modulus could be computed accurately by die-scale simulation of such mechanical properties.
- Heat
With decreasing sizes of ICs owing to the newer process nodes and Moore's law, more transistors are packed into similar or smaller areas than ever before. In 3D ICs, the heat generation increases considerably, which puts limitations on TSVs to efficiently dissipate heat away from the chip. Localized hotspots may get created in areas where temperatures increase more as compared to other parts of the chip. This temperature distribution would cause even more stress on the interconnect which would have a significant impact on the performance and reliability of the chip.  
Source: https://www.e3s-conferences.org/articles/e3sconf/pdf/2018/13/e3sconf_icemee2018_04026.pdf

![Screenshot 2025-03-07 160707](https://github.com/user-attachments/assets/b2a72375-0ff1-493d-b164-b5b267be43f2)

## Applications of TSV
An older presentation at NASA Electronics that covers TSVs:
TSVs form a crucial part of chips that enable RF, MEMS, Memory and Logic Dies in 3D stacking. Source: https://nepp.nasa.gov/docs/etw/2012/Tuesday/T08_Dillon_Through_Silicon_Via.pdf
### Chips that use TSV
- AMD's 3D V-Cache ( Ryzen 7 5800X3D). Source:https://www.techpowerup.com/review/amd-ryzen-7-5800x3d/2.html
![image](https://github.com/user-attachments/assets/ff87a452-7db6-44c7-b4b8-56ea8ba3bfd0)
-  Nvidia A 100: Source: https://jonathan-hui.medium.com/ai-chips-a100-gpu-with-nvidia-ampere-architecture-3034ed685e6e
  ![image](https://github.com/user-attachments/assets/39bf0022-3c5a-49a9-95a0-29c352b2bd9e)

## TSV challenges
With stacking of the chips, the heat dissipation becomes critical and this causes a significant challenge in the floor planning and partitioning stage. As per reports by EDA tool vendors, 3D stacking leads to a creation of hotspots which requires cooling solutions. As TSVs get narrower, the cost of fabrication increases due to the longer etching time and precision required.Additionally, yield defects from stress and poor filling could lead to increase in costs and time to market.
TSVs also introduce capacitance and signal integrity issues, which call for additional modelling and simulation of these effects.

## References
- https://youtu.be/L7ojK4U67Ik?si=A7F8gnnvtbQwJJJt
- https://youtu.be/5uuRduTpl4Q?si=FuvbvQM-E7meeppG
- https://semiconductor.samsung.com/us/support/tools-resources/dictionary/semiconductor-glossary-tsv/
- https://youtu.be/zC1PH2oe6es?si=qM_cODbcmgJUozg3
- https://youtu.be/-G-jtmCdeuQ?si=jV9JQ8smWZgTYyb9
- https://iopscience.iop.org/article/10.1088/1748-0221/20/01/C01017/pdf
- https://en.wikipedia.org/wiki/Through-silicon_via
- https://semiengineering.com/strain-stress-in-advanced-packages-drives-new-design-approaches/
- https://semiengineering.com/whats-next-for-tsvs/
- https://www.nist.gov/system/files/documents/pml/div683/conference/Sukharev_2011.pdf
- https://www.e3s-conferences.org/articles/e3sconf/pdf/2018/13/e3sconf_icemee2018_04026.pdf
