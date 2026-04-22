# Automated and Intelligent Traffic Signal System for assisting Emergency Vehicles

## Problem Statement  

The existing traffic signal systems operate on fixed or semi‑adaptive timetables that do not prioritize emergency vehicles, leading to unnecessary delays during critical response times due to regular signal cycles, congestion‑induced stopping, and the inability to dynamically recognize and respond to approaching emergency vehicles. This project addresses the problem by designing an automated and intelligent traffic signal system that reliably detects emergency vehicles using a multimodal approach—combining RF transmitters integrated with sirens as the primary identification mechanism, real‑time computer vision for vehicle recognition, and audio sensing for siren detection—thereby enabling the traffic signal to safely override its normal cycle, grant right‑of‑way to the emergency vehicle, and resume regular operation with minimal disruption to general traffic.



### Expected Outcome  
The implemented system is expected to (1) accurately detect approaching emergency vehicles in diverse real‑world conditions (occlusions, poor visibility, ambient noise), (2) dynamically override normal signal phases to create timely, safe green corridors for emergency vehicles, (3) measurably reduce emergency response delays at controlled intersections, and (4) maintain low false‑activation rates and minimal disruption to regular traffic flow, demonstrating its practicality for deployment in intelligent transportation infrastructure. 


## Project Description 
 Working:
- Camera: live feed will be used to detect emergency vehicles in real time using real time computer vision, OpenCV.
- Transmitter & Receiver: We use these for a fool proof system. Our main system will consist of a physical receiver and only emergency vehicles will exclusively be fitted with transmitters. One very important thing is that the transmitter will only switch ON and transmit signals only when the siren is switched ON (both are connected that way). The transmitters and the receivers play a very important role in the entire project. Therefore it will act as our main primary identification of an emergency vehicle
<br><br> Cases of flaws and their solution:
1) We cant 100% rely on computer data, maybe a distorted vision of an emergency vehicle like similar looking vehicle might be recognized as an emergency vehicle which would trigger the system BUT the use of transmitters and receivers can get rid of that flaw as it is being used for the primary identification of an emergency vehicle.
2) Also in a case where an emergency vehicle is only passing by and is not actually occupied, the system wont perform a false trigger.
3) In a common case where emergency vehicle might not be visible in the camera but the siren is audible, we use signals from the transmitters to identify direction and perform a correct trigger. If we have sirens audible in 2 different detectors, we can use the signal strength to find closest detection and figure out which direction the vehicle is arriving from.
4) Another case where both vision and sound is blocked, we can again use transmitters to identify and use signal strength for directions.
Next is the signal overriding. 
Signal overriding: steps-
1) Normal signal cycle being carried out.
2) Emergency Vehicle is detected.
3) Current green signal will immediately switch to yellow for 3-5 seconds to perform a safe transition.
4) Next, all the signals are red for 1 sec OR all the signals may display a symbol to show that an emergency vehicle is passing by.
5) The lane for the emergency vehicle turns green until it passes.
6) Traffic signals then go back to following normal cycles. So the last lane that was green before the transition will have a resetted timed green signal.

---

### **Team Members**  

#### **Saish Darge**  

#### **Aayush Desai**  

#### **Vignesh Dukare**  

#### **Saujanya Shetty**  
 


---

