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


# CAD
The cad files for the Njord SAA were made in autodesk inventor professional. There are 5 seperate modules for the elevators, wings, tail, body and nose. There were lots of struggles with the cad on multiple occasions, such as how I had to fully redesign the body nose and tail a few times. The main reason for this was because I had very little design constraints to work from, and mostly figured it out as I went.

Nose cone:
<img width="1204" height="859" alt="image" src="https://github.com/user-attachments/assets/14e38fd2-397e-4809-99ca-ab20a8106bc0" />

Tail:
<img width="1038" height="694" alt="image" src="https://github.com/user-attachments/assets/6cbd354e-d135-40a2-a862-14884e549e99" />


# PCB
This is the PCB for the Njord SAA! It is a standard 4 layer PCB featuring all elements needed for a flight computer like an IMU, barometer, an ESP32, and many pin headers for devices like servos, motors, and other sensors. It was designed originally in Eagle, but I switched to KiCad bacause there were a lot more sources for help, and it both looks and feels more modern.

Render top:
<img width="1080" height="573" alt="image" src="https://github.com/user-attachments/assets/6551b520-e1e2-42bf-8c92-33d5cd51548c" />


Wiring diagram:
<img width="1092" height="570" alt="image" src="https://github.com/user-attachments/assets/05c93473-d113-4e4c-b8a8-d59644529e2e" />


Schematic:

<img width="917" height="631" alt="image" src="https://github.com/user-attachments/assets/c1f1fc88-a78a-4e04-892a-7a89090506dc" />


  # How to buld

  ### !! MAKE SURE TO WEAR PROPER PPE WHEN WORKING ON CURED CARBON FIBER & FIBERGLASS !!
  (resperator and eye protection, full body suit for fiberglass)

 ### Prepare fuselage:
1. 3d print the main body, tail section, tail tip, nose cone, bulkhead, and hatches, then remove supports and clean up the prints
2. Lightly sand the nose cone and main body to ensure a proper adhesion to the epoxy
3. Cut carbon fiber weave to the correct size to wrap the main body, then cut out sections for the wing pins, ESC slots and battery hatches. Do the same for fiberglass to the nose cone
4. Make sure the cuts fit the subsequent part BEFORE mixing any epoxy
5. Mix 2 part epoxy in the correct ratio supplied by the manufacturer, then with a foam roller wet out cuts on both sides and squeeze out the excess epoxy
6. Wrap the carbon fiber around the body section, smooth out any wrinkles and air pockets, then apply peel ply to the surface. Repeate process for the fiberglass on the nose cone (peel ply is optional for fiberglass) and leave both to cure for 24-48 hours
7. After drying, drill out screw holes (you can shine a light through the holes in the 3d print to see the outline) and dremel the edges of the pre cut sections for wing pins and hatches until their sizes match the 3d print
 ### Prepare Control Surfaces & Wings:
1. 3d print rudders, elevons, and wings, then remove supports and clean up the prints
2. Lightly sand all surfaces of all parts for good adhesion, and pre cut carbon fiber weave to the correct sizes for each part seperately, with cutout areas for the wing bearings
3. Repeat steps 4-7 from the Fuselage Preperation instructions for each part
5. Cut 8mm carbon fiber rods so they will just stick out of the wing spar holes, there are 2 8mm rods in each of the four wings. Coat each rod with Sikaflex, then push as far into the hole as possible and let cure for 12-24 hours. After cured, cut the CF rods as close to the wing as possible and sand or file the rest until it is flush with the wing
6. Press fit a bearing into each wing in the provided slot
7. Repeat step 5, but with 5mm carbon fiber rod and for the back holes only in the elevators
### Install Electronic Hardware:
1. Neatly solder the PCB using the stencil provided by JLCPCB, and plug in the ESP32-S3 DEVKITC along with the MINI-560 buck converter. Make sure that the buck converter and esp32 are placed the correct way around, and test for improperly soldered components
2. Install the following hardware into their respective places:
   * Rear servos; Each servo is held in by 2 screws (make sure the cables get routed through the cable hole), then sealed using Sikaflex for waterproofing.
   * Motors; Install to motor mounts with 4 screws 
   * ESCs; Sikaflex each ESC into the slots, making sure they are facing the correct direction and wires are through the holes. Use more Sikaflex to create a flush surface over the ESCs for aerodynamics
   * Centre servo; Screw 2 screws into internal mount located on the rear of the body section. Connect to all 4 wings' release pins with push rods
   * Ballast Pumps; Slot pump into the slot and Sikaflex it into place. Heat insert the brass tube fittings into the wall holes and ballast tank holes, then connect tubing from pump input to the outside connecter, and the output to the connector on the ballast tank. Repeat for both pumps
   * Batteries: Slide in the two 5200mah batteries into the secure slot in the top and bottom hatches, ensuring the cables go towards the front
   * FS CVT01; Secure one side to the bottom of the forward part of the main body section using either hot glue, or Sikaflex
   * LiDaR; Insert LiDaR into the nose cone and Sikaflex it to solidify its position
   * PCB; Slot PCB into the tray inside the nose cone and screw the 2 screws into the corners
   * iA6B; Insert iA6B below the PCB, with the antenna facing forwards and pins pointing rearwards. Secure in place with hot glue, or Sikaflex
### Cable Routing:
##### Tip: lable each cable before installing so you know what  is what
1. Start with the tail section:
   * Rear servos; Route the servo's cable through the channel for them to bring them to the forwards most part of the tail, and connect a cable extender to the cable. Repeat for all 4 servos
   * Motors; Route the motor cables along the inset channels on the rear side of the motor mount and into the tail. Once into place, use Sikaflex to fill the rest of       the channel and the hole that enters the tail section. Solder and heatshrink a similar thickness cable to each of the 3 wires on the motor, and repeat for both motors
2. Main Body section:
   * ESCs; Route the wires through the holes that lead into the body, and seal the cable holes with Sikaflex. Connect the 3 pin cable to an extender and run it below the wing box to the front of the body, and repeat on the other side. Solder both ESCs' + and - input cables to a single xt-60 connector, making sure to put the + and - the correct way around. Attach an XT-60 cable extender (make it yourself with 2 spare wires and XT-60 connectors) to the plug, and run it down the body with the 3 pin cable
   * Centre Servo; Plug a servo cable extender into the connector, then run it internally below the wing box and out of the front of the body
   * Ballast Pumps; Strip the tip off of 2 spare wires, then twist them to the + and - of the pump. Solder a small amount of solder onto the connection to ensure good connection, then pull a piece of shrink wrap over the exposed wire and shrink with a heat gun. Repeat on both pumps
   * FS CVT01; Cut the connectors off of the two 1 pin cables, and solder them directly to the XT60 connector (make sure the polarity is correct)
3. Nose Cone:
   * LiDaR; Connect 5 pin cable to the "GY-TOF10M" labled 5 pin header on the pcb
   * iA6B; Plug a 3 pin cable into the "Servo" section on the iA6B, and connect it to the horizontal 3 pin header on the pcb. Optionally, you can shorten the  3 pin cable by cutting it to length, removing the connector, and re soldering it to the fixed length
### Final Assembly:
##### Connect tail section and main body:
 1. Solder and heatshrink the 3 motor cables to the matching 3 cables on the ESC. Repeat on both motors
 2. Route servo cables down the body section along with the cables already going that direction
 3. Slide the body section half way into the tail's slot, then lightly coat the inner wall of the outer rim of the tail section with Sikaflex and slide it fully in. Moving quickly, Screw in the tail section to the body through the 4 screw holes, placing a bead of Sikaflex below the screw's head before fully screwing it in
##### Install Bulkhead:
 1. Pass all loose cables hanging out of the body section through the hole in the bulkhead, and plug in the following cables to the PCB:
       * Servos; Servo plugs on the PCB are labled, and connect as follows: servo 1: left elevon, servo 2: right elevon, servo 3: top rudder, servo 4: bottom rudder, and servo 5: wing release servo
       * ESCs; 3 pin cables plug into "ESC_1" for left ESC and "ESC_2" for right ESC
       * Ballast Pumps; connect cables to screw terminals "Pump_1" and "Pump_2". It does not matter which side connects to which terminal
       * FS CVT01; DOES NOT PLUG INTO PCB, instead it plugs into the "sense" plug on the radio reciever
 2. Put bulkhead far enough from the nose to fit a screw driver to the 2 PCB screws, and pull all cables through the bulkhead to this length. Sikaflex the cable hole completely shut to prevent any leaking
 3. Insert O-ring into the groove in the nose cone and push the bulkhead into the nose cone. Screw in all 8 screws in a star pattern to fully seal the nose, with a bead of Sikaflex enderneath each screw's head
##### Attach nose cone to body:
 1. Drop a bead of Sikaflex onto the nose cone's outer rim and slide the body into the nose cone's slot.
 2. Screw in the 4 screws around the attachment area, with a bead of Sikaflex below each screw's head
##### Attach wings:
 1. Insert the wing into the wing slot, ensuring that the leading edge of the wing is facing outwards of the body
 2. Push an 8mm CF rod into the hole in the body that corresponds to the wing, and cut it down to a size where you can file the rest
##### Attach elevators and rudders:
 1. Place a 5mm CF rod loosely into the front hole of the left elevator
 2. Push the other side of the CF rod through the hole located just in front of the elevator servo, and place the right elevator on the other end of the CF rod
 3. Attach pushrods to both servos that attach to each elevator
 4. Slot rudders into the hinge joints located on the top and bottom of the tail, and insert a 2mm steel rod (you can cut up a push rod to use as this) into the hinge and   attach onto the hings with a small bead of Sikaflex
 5. Attach rudders to rudder servos with a push rod
##### Final attachments:
 1. Connect the props to the motors with the nut that screws into the motor shaft. Make sure the props are facing the correct way
 2. Attach the hatches by putting a small amount of Sikaflex around the channels on the body, then press them in
### Firmware:
 1. Download firmware from Github page
 2. Connect ESP32 to computer via the USB-C port on the ESP32
 3. Upload the firmware onto the board

### Conquer the seas and skies!


