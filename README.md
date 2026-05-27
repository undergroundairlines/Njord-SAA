# Njord-SAA
The Njord SAA (Submersible Amphibius Aircraft) is a submersible aircraft which can transition automatically from underwater travel to aerial flight. To resurface, it can empty it's 2 ballast tanks, pitch almost 90° directly up, and launch itself above the surface. When the surface is breached, it deploys 2 sets (yes, that means 4 wings total) of wings, and switches motors to a much higher RPM to produce enough thrust for flight.
<img width="2560" height="1440" alt="Njord SAA v2" src="https://github.com/user-attachments/assets/211fdac3-f863-4c79-8a53-dfd4f5994471" />
# Features 
* Deployable wings: The main visual feature of the Njord SAA is its wings, having 2 sets of deployable wings which allow having good hydrodynamics underwater, while still being able to produce enough lift to fly. The rear set of wings deploy forwards and meet the forward most wings at their tips.

* ~2:1 Thrust to Weight Ratio: Due to having 2 large 3 bladed props, and motors that are way too overpowered, at max thrust it will be able to produce (slightly more than) double the crafts weight in thrust. This will make it incredibly fast, decently manouverable, and much cooler!

* Tailerons: Due to the wings being deployable, there is not enough room to house servos for the ailerons. No matter! Instead, we will repurpose the elevators (and possibly rudders as well) to do both pitch and roll.

* Auto Land: There will be a sort of Auto land feature to be added eventually, where at the flick of a button the craft can automatically bring itslef to the ground safely, and softly.

* Groud Avoidance System (GAS): Any time the pilot brings the aircraft too close to the ground, it will automatically pull up just before the perfect moment to ensure the pilot remains under control right until it's almost too late. Uses data from the gyro, and laser rangefinder to (semi-realistically) estimate its height, which allows the  computer to know when to pull up.

* As an opposite to the Ground Avoidance System, there will be a system to resurface the craft when submerged if the batteries become dangerously low, or it loses signal.

# CAD
The cad files for the Njord SAA were made in autodesk inventor professional. There are 5 seperate modules for the elevators, wings, tail, body and nose. There were lots of struggles with the cad on multiple occasions, such as how I had to fully redesign the body nose and tail a few times. The main reason for this was because I had very little design constraints to work from, and mostly figured it out as I went.
<img width="1204" height="859" alt="image" src="https://github.com/user-attachments/assets/14e38fd2-397e-4809-99ca-ab20a8106bc0" />
<img width="1038" height="694" alt="image" src="https://github.com/user-attachments/assets/6cbd354e-d135-40a2-a862-14884e549e99" />






# PCB
This is the PCB for the Njord SAA! It is a standard 4 layer PCB featuring all elements needed for a flight computer like an IMU, barometer, an ESP32, and many pin headers for devices like servos, motors, and other sensors. It was designed originally in Eagle, but I switched to KiCad bacause there were a lot more sources for help, and it both looks and feels more modern.
<img width="1018" height="538" alt="image" src="https://github.com/user-attachments/assets/1cd167ff-dee4-4ac0-b21b-43a03130883d" />


<img width="1315" height="687" alt="image" src="https://github.com/user-attachments/assets/787c179d-4afc-437e-8548-65247d33fbfb" />

