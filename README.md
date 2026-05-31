<img width="799" height="1232" alt="image" src="https://github.com/user-attachments/assets/0d9de1e9-dcd2-48ef-b938-b2a1d21ee5d1" />


# Njord-SAA
The Njord SAA (Submersible Amphibius Aircraft) is a submersible aircraft which can transition automatically from underwater travel to aerial flight. To resurface, it can empty it's 2 ballast tanks, pitch almost 90° directly up, and launch itself above the surface. When the surface is breached, it deploys 2 sets (yes, that means 4 wings total) of wings, and switches motors to a much higher RPM to produce enough thrust for flight.
The reason for this project was we thought a amphibius aircraft so we designed It. We always wanted a drone/plane and this was our best chance to get one.
<img width="2560" height="1440" alt="Njord SAA v2" src="https://github.com/user-attachments/assets/211fdac3-f863-4c79-8a53-dfd4f5994471" />
# Features 
* Deployable wings: The main visual feature of the Njord SAA is its wings, having 2 sets of deployable wings which allow having good hydrodynamics underwater, while still being able to produce enough lift to fly. The rear set of wings deploy forwards and meet the forward most wings at their tips.

* ~1.5:1 Thrust to Weight Ratio: Due to having 2 large 3 bladed props, and motors that are way too overpowered, at max thrust it will be able to produce mor than the crafts weight in thrust. This will make it incredibly fast, decently manouverable, and much cooler!

* Tailerons: Due to the wings being deployable, there is not enough room to house servos for the ailerons. No matter! Instead, we will repurpose the elevators (and possibly rudders as well) to do both pitch and roll.

* Auto Land: There will be a sort of Auto land feature to be added eventually, where at the flick of a button the craft can automatically bring itslef to the ground safely, and softly.

* Groud Avoidance System (GAS): Any time the pilot brings the aircraft too close to the ground, it will automatically pull up just before the perfect moment to ensure the pilot remains under control right until it's almost too late. Uses data from the gyro, and laser rangefinder to (semi-realistically) estimate its height, which allows the  computer to know when to pull up.

* As an opposite to the Ground Avoidance System, there will be a system to resurface the craft when submerged if the batteries become dangerously low, or it loses signal.

  # How to buld

  ### !! MAKE SURE TO WEAR PROPER PPE WHEN WORKING ON CURED CARBON FIBER & FIBERGLASS !!
  (resperator and eye protection, full body suit for fiberglass)

 ### Prepare fuselage:
1. 3d print the main body, tail section, nose cone and hatches, then remove supports and clean up the prints
2. Lightly sand the nose cone and main body to ensure a proper adhesion to the epoxy
3. Cut carbon fiber weave to the correct size to wrap the main body section, then cut out sections for the wing pins, ESC slots and battery hatches. Do the same for fiberglass to the nose cone
4. Make sure the cuts fit the subsequent part BEFORE mixing any epoxy
5. Mix 2 part epoxy in the correct ratio supplied by the manufacturer, then with a foam roller wet out both cuts on both sides until and squeeze out the excess epoxy
6. Wrap the carbon fiber around the body section, smooth out any wrinkles and air pockets, then apply peel ply to the surface. Repeate process for the fiberglass on the nose cone (peel ply is optional for fiberglass) and leave both to cure for 24-48 hours
7. After drying, drill out screw holes (you can shine a light through the holes in the 3d print to see the outline) and dremel the edges of the pre cut sections for wing pins and hatches until their sizes match the 3d print
 ### Prepare Control Surfaces & Wings:
1. 3d print rudders, elevons, and wings, then remove supports and clean up the prints
2. Lightly sand all surfaces of all parts for good adhesion, and pre cut carbon fiber weave to the correct sizes for each part seperately
3. Repeat steps 4-7 from the Fuselage Preperation instructions for each part
5. Cut 8mm carbon fiber rods so they will just stick out of the wing spar holes, there are 2 8mm rods in each of the four wings. Coat each rod with epoxy, then push as far into the hole as possible and let cure for 12-24 hours. After cured, cut the CF rods as close to the wing as possible and sand or file the rest until it is flish with the wing.
6. Repeat step 5, but with 5mm carbon fiber rod and for the elevators.
### Install Electronic Hardware:
1. Neatly solder the PCB using the stencil provided by JLCPCB. Make sure to test for improperly soldered compenents after soldering
2. Install the following hardware into their respective places:
   * Rear servos; Each servo is held in by 2 screws (make sure the cables get routed through the cable hole), then sealed using Sikaflex for waterproofing. Connect to control surfaces using push rods
   * Motors; Install to motor mounts with 4 screws
   * ESCs; Sikaflex each ESC into the slots, making sure it is facing the correct direction and wires are through the holes
   * Centre servo; Screw 2 screws into internal mount located on the rear of the body section. Connect to all 4 wings' release pins with push rods
   * Ballast Pumps; Slot pump into the slot and Sikaflex it into place. Connect tubing from pump input to the connecor on the wall, and the out into the connector on       the ballast tank. Repeat for both sides
   * Batteries: Slide in the two 5200mah batteries into the secure slot in the top and bottom hatch
   * LiDaR; Insert LiDaR into the nose cone and Sikaflex it to solidify its position
   * PCB; Slot PCB into the tray inside the nose cone and screw the 2 screws into the corners
### Cable Routing:
1. Start with the tail section:
   * Servos; The servos' cables should be routed through the cable route and be exposed to the forwards-most part of the tail.
   * Motors; Route the motor cables along the inset channels on the rear side of the motor mount and into the tail. Once into place, use Sikaflex to fill the rest of       the channel and the hole that enters the tail section.
   * ESCs;

3d print the body, wings, tail, elevators and nose
Wrap the body, wings, elevators and ruddders in carbon fiber weave
install or the componets the PCB mottors and servos
route the wires
put eveything together
assembe the body with silicone around the mating surfaceses
ready to fly or swim.

# CAD
The cad files for the Njord SAA were made in autodesk inventor professional. There are 5 seperate modules for the elevators, wings, tail, body and nose. There were lots of struggles with the cad on multiple occasions, such as how I had to fully redesign the body nose and tail a few times. The main reason for this was because I had very little design constraints to work from, and mostly figured it out as I went.
<img width="1204" height="859" alt="image" src="https://github.com/user-attachments/assets/14e38fd2-397e-4809-99ca-ab20a8106bc0" />
<img width="1038" height="694" alt="image" src="https://github.com/user-attachments/assets/6cbd354e-d135-40a2-a862-14884e549e99" />






# PCB
This is the PCB for the Njord SAA! It is a standard 4 layer PCB featuring all elements needed for a flight computer like an IMU, barometer, an ESP32, and many pin headers for devices like servos, motors, and other sensors. It was designed originally in Eagle, but I switched to KiCad bacause there were a lot more sources for help, and it both looks and feels more modern.
<img width="1588" height="832" alt="image" src="https://github.com/user-attachments/assets/209b0849-b538-439a-b2f3-88c1d9132299" />

<img width="1020" height="542" alt="image" src="https://github.com/user-attachments/assets/206f2173-46a9-4b15-ad38-f54aa713e713" />


<img width="917" height="631" alt="image" src="https://github.com/user-attachments/assets/c1f1fc88-a78a-4e04-892a-7a89090506dc" />



