# TSV
## A repository for a blog on Through Silicon Via (TSV)
## Introduction
As the industry proceeds to move from 2-D to 2.5-D and finally 3-D integration of ICs, a major challenge in the integration of these ICs is the packaging methodology used. Traditionally, in order to integrate two different ICs a wire bond was used in a 2-D stacking setup. These were long wires, with comparable latency to a PCB. It also meant a constraint on the number of wires which could be connected from a particular IC to another. A major drawback of using ‘traditional’ wire bonding is the limit of bandwidth that it can support. By 3-D stacking various ICs, and using Through Silicon Vias (TSVs), the length of connections is reduced considerably, while increasing the number of connections it can support.

A major advantage of using TSV is the reduction of the overall package size and power consumption, resembling the advantages of newer process nodes. This is particularly helpful for example in cases like RF and other analog ICs which cannot be scaled down beyond a certain size, due to the inherent way analog ICs function. The advantage of 3-D stacking is that not all ICs need to be scaled down to the latest node. TSV plays a crucial role in enabling this, while also saving costs for companies as some of the ICs could be of older nodes. This is referred to as a System in Package.
What is TSV
TSV is an electrical connection or interconnect that is used to connect two different dies or interfaces or even carry signals faster within a device. The main advantage of using TSV is the benefits of shorter connections, while also offering a larger number of connections and higher bandwidths, when compared to older methods of connections like wire-bonding.
The image below shows how TSVs are used to connect DRAM dice with a high bandwidth Memory die interface. These connections are vertical and run throughout the dies. Image Source: [https://commons.wikimedia.org/wiki/File:High_Bandwidth_Memory_schematic.svg](url)

![High_Bandwidth_Memory_schematic svg](https://github.com/user-attachments/assets/b199b726-f0e7-4a85-b5f1-3e2c379c16a8)

![Through-Silicon_Via_Flavours svg](https://github.com/user-attachments/assets/2610bc63-567d-4eb7-b355-cf1def7280af)

The origins of TSV were in the 1980s, which were patented for use by Fujitsu, which described using TSVs in 3D chips. They were used in the MEMS (Microelectromechanical Systems) before eventually being used in Integrated Circuits.
Manufacturing Process of TSV
The manufacturing process could be categorized into three major categories: TSV-first, TSV-Middle, and TSV-last, the major difference being the order of which the TSV is fabricated. In TSV-first, the TSVs are fabricated before the individual components are patterned in the front end of line process. In TSV-middle, the TSVs are fabricated after individual components, but before the metal layers like M1, M2 etc. In TSV-last, the TSVs are fabricated after or during the back end of line process. The process includes etching, oxide deposition, barrier and seed layer deposition, 3-D lithography, and Via Filling. [https://commons.wikimedia.org/wiki/File:Through-Silicon_Via_Flavours.svg
](url) [https://www.semanticscholar.org/paper/Comprehensive-Review-of-Different-Methods-for-Via-Baru-Shahidin/e4d9a0c521756374d8c191b043d414005c626496/figure/0](url)



 ![3-Figure1-1](https://github.com/user-attachments/assets/f90f87d8-2faf-4481-8ae1-286ebccab2e4)




## TSV : Effects of stress and heat
## Stress
Some of the major issues with TSVs are thermal and TSV-induced stress. The effects of stress could accumulate in the TSV and get transferred to the transistors it is connected to. A potential solution to this could be using keep out zones which would enable TSVs to be separated from the transistors. However, as the die sizes and the nodes decrease, the Vias’ diameters would reduce as well. With this, the keep out zone would decrease as well, causing considerable challenges in terms of stress. A significant source of thermal stress would be the thermal expansion coefficient mismatch for the different materials used within TSVs, which could cause cracks at the interface with silicon.


## Heat
With decreasing sizes of ICs owing to the newer process nodes and Moore's law, more transistors are packed into similar or smaller areas than ever before. In 3D ICs, the heat generation increases considerably, which puts limitations on TSVs to efficiently dissipate heat away from the chip. Localized hotspots may get created in areas where temperatures increase more as compared to other parts of the chip. This temperature distribution would cause even more stress on the interconnect which would have a significant impact on the performance and reliability of the chip.



## References

2.5 D & 3D Chips: Interposers and Through Silicon Vias
Stacking Dies For Performance and Profit
https://semiconductor.samsung.com/us/support/tools-resources/dictionary/semiconductor-glossary-tsv/
Energy-Efficient Optical Interconnect: Lecture 1, Nano-Photonics and Optical Interconnects
Optical Interconnects in Data Centers with Rob Stone
https://iopscience.iop.org/article/10.1088/1748-0221/20/01/C01017/pdf
https://en.wikipedia.org/wiki/Through-silicon_via
https://semiengineering.com/strain-stress-in-advanced-packages-drives-new-design-approaches/
