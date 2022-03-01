# FULL ADDER TOPOLOGIES AND CARRY SAVE ADDER

## TABLE OF CONTENTS

[ABSTRACT](#ABSTRACT)

[FULL ADDER TOPOLOGIES](#FULL-ADDER-TOPOLOGIES)

[28T FULL ADDER](#28T-FULL-ADDER)

[8T FULL ADDER](#8T-FULL-ADDER)

[20T TRANSMISSION GATE FULL ADDER](#20T-TRANSMISSION-GATE-FULL-ADDER)

[CARRY SAVE ADDER](#CARRY-SAVE-ADDER)

[AUTHOR](#AUTHOR)

[ACNOLEDGEMENTS](#ACHNOLEDGEMENTS)

[REFERENCE](#REFERENCE)


## ABSTRACT

Adders are functional building block of ALU, Digital signal processors, micro-processors. This work presents design and implementation of cmos based carry save adder and full adder [ 28T, 20T , 8T ] topologies. The implementation was done on Synopsys Custom Compiler tool using 28nm technology node. Low power, area and high-speed are the principal factors to be considered in VLSI design of adders. Conventional 28T Full adder has higher power consumption and area but is more immune to noise and hence highly stable. Transmission Gate Full 20T Adder performs better than CMOS Full Adder in case of power dissipation as well as delay with lesser number of transistors being used. 8T full adder is better in terms of area and speed but is more succeptible to noise. Carry Save Adder is a kind of parallel multi-bit multi-input adder that stores the carry reducing the delay caused by propogation of the carry.

## FULL ADDER TOPOLOGIES

Full adder logical expressions for Sum and Carry are stated below:

![image](https://user-images.githubusercontent.com/46755232/156183807-b0901bef-821c-45b7-be11-f4f79f8c81d7.png)


### 28T FULL ADDER 
[ CONVENTIONAL FULL ADDER ]

The topology consists of pull-up and pull-down network of PMOS and NMOS transistors. This design style offers good driving capability and full swing in output voltage. But the transistor count being more in the circuit results in higher power consumption and delay.

The design is achieved by manipulating the basic equation of full adder which will optimize the implementation is stated below. 

![image](https://user-images.githubusercontent.com/46755232/156184037-e422f08d-4935-4d50-93fc-6bc72880f614.png)

![image](https://user-images.githubusercontent.com/46755232/156216015-55d516e0-3188-4b68-ba49-bb37101af70d.png)

28T full adder reference circuit


![28T FA](https://user-images.githubusercontent.com/46755232/156160340-50d90818-33d1-40ba-87ac-86ba5f8c2285.png)   
                                       28T full adder CMOS circuit


![image](https://user-images.githubusercontent.com/46755232/156161886-c928f0a6-7236-475b-bb8a-b5c868d428f8.png)
                                        Transient analysis simulation waveforms

![image](https://user-images.githubusercontent.com/46755232/156165564-bb795cb1-276f-4b55-b125-8c8a300c5a38.png)
                                         
  28T full adder cell view symbol


### 20T TRANSMISSION GATE FULL ADDER 

Transistor count is reduced to 20 in this design. Due to the reduction in number of transistors used in this circuit the delay will also reduce compared to 28T Full Adder. The architecture is based on XOR gate which is realized by transmission gate. A PMOS and an NMOS transistor are connected in parallel to form the transmission gate and complementary control signals drive them.  Since transmission gate passes entire voltage range at its output, so the output voltage degradation of the adder is very less.


![image](https://user-images.githubusercontent.com/46755232/156162101-fcf34662-6fce-4b63-87a8-f4018acf9a72.png)

20T full adder CMOS circuit

![image](https://user-images.githubusercontent.com/46755232/156162189-46e084c4-b47a-42bb-a93c-aaf8db6eb7f1.png)

Transient analysis simulation waveforms

![image](https://user-images.githubusercontent.com/46755232/156165268-61b70fab-a094-4e6f-a6a4-6d38d456a8f2.png)

20T full adder cell view symbol



### 8T FULL ADDER

In the proposed 8T full adder sum is generated using 3T XOR module twice, and carry is generated using NMOS and PMOS pass transistor logic devices as shown in below figure. The bsic full adder equations  are modified so as to visualise the 8T full adder design. The modified equations for 8T full adder design are:

![image](https://user-images.githubusercontent.com/46755232/156181063-2570437a-9628-46d6-aa85-3dc8214ff58f.png)



![image](https://user-images.githubusercontent.com/46755232/156162240-168cfb7e-484a-4f64-a148-d34bce03bfe8.png)

8T full adder CMOS circuit


![image](https://user-images.githubusercontent.com/46755232/156162273-88388cf2-a35b-4a4f-a7a4-7c2235659bcd.png)

Transient analysis simulation waveforms



## CARRY SAVE ADDER 

![image](https://user-images.githubusercontent.com/46755232/156215826-d1dfa2e7-c203-485e-ad53-61a60f6cc158.png)
 
 CSA reference circuit

The implentation shows 4 bit carry save adder using structural modelling  with 4 inputs. A carry-save adder (CSA) is a type of digital adder, used in computer architecture to compute the sum of three or more n-bit numbers in binary. The carry-save unit consists of n full adders, each of which computes a single sum and carry bit based solely on the corresponding bits of the three input numbers. Given the three n-bit numbers a, b, and c, it produces a partial sum ps and a shift-carry sc. The straight forward way of adding together m numbers (all n bits wide) is to add the first two, then add that sum to the next, and so on. This requires a total of m − 1 additions with a large delay due to carry propagation. Using carry save addition, the delay can be reduced further still. The idea is to take 3 numbers that we want to add together, x + y + z, and convert it into 2 numbers c + s such that x + y + z = c + s. This is achieved by using  2 CSA blocks  , and then the final Ripple carry adder block. The cin of each full adder in csa block is used as the third input

### CARRY SAVE ADDER USING 28T FULL ADDER

![image](https://user-images.githubusercontent.com/46755232/156162328-c90a2a95-cd8b-4b81-999a-d2ad62e08f8e.png)

CSA using 28T full adder circuit

![image](https://user-images.githubusercontent.com/46755232/156162352-d8c92d50-5002-44b6-a4dc-8d632407b046.png)
Transient analysis of CSA simulation waveforms-1 

![image](https://user-images.githubusercontent.com/46755232/156162369-ef274f7c-6e29-4d0b-b5f6-2277a1842db8.png)
Transient analysis of CSA simulation waveforms-2

### CARRY SAVE ADDER USING TRANSMISSION GATE FULL ADDER:

![image](https://user-images.githubusercontent.com/46755232/156164925-f8cab396-b1ee-438a-8789-b0e7061bbf16.png)

CSA using 20T full adder circuit

![image](https://user-images.githubusercontent.com/46755232/156164828-85aff1ae-9984-4dcf-8fca-0073bd08a201.png)

Transient analysis of CSA simulation waveforms-1

![image](https://user-images.githubusercontent.com/46755232/156164864-21450d32-60d7-4170-803c-1d0f26e204c1.png)

   Transient analysis of CSA simulation waveforms-2

The main application of carry save algorithm is, well known for multiplier architecture and is used for efficient CMOS implementation of many wider variety of algorithms for high speed digital signal processing. 

## AUTHOR

Amrutha V.
## ACHNOLEDGEMENTS

[Synopsys Inc](https://www.synopsys.com/)

[IIT Hyderabad](https://iith.ac.in/)

[Analog IC Design Hackathon](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)

## REFERENCE

[1]Karthik Reddy . G, Kavitha Khare, Low Power- Area GDI & PTL based full adder designs. 

[3]N.H.E.Weste.Cmosvlsidesign:Acircuitsandsys-temsperspective.https://cutt.ly/InNnZPb


