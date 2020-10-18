# blackred-laser
anything i do for the black/red/redsail/orion motor tech lasers 


for the zZ table mod

* nema 17 motor 1.7A  http://www.zyltech.com/nema-17-stepper-motor-1-7-a-0-59-nm-84-ozin-1-3-or-5-pack/
* step/dir driver for motor https://www.amazon.com/UsongShine-Stepper-Controller-Arduino-Printer/dp/B07HHS14VQ/ only needs to be set to 0.7A
* pulleys and belts https://www.amazon.com/gp/product/B07ZBZ739T/ motor is 5 mm shaft is 7mm  i used 20T/60T and drilled out the larger pulley to a 7mm bore size. 6mm belt. unfortunately i had all the parts lying around to do this so i can't give the exact buy links. 
* two m5 bolts 10mm length , washers and nuts
* 4 m3's 6mm for the motor
* 1/8th plywood cut out
* two holes drilled in metal frame to mount the motor plate, clearance holes for 5mm bolts, 11mm from front end (furthest from bed) 18mm apart.
* sheet of 5mm rubber foam to go between the motor and the steel frame to dampen any vibration
* write to ruidia , step-/dir - and 5v to both dir+/step+ 
* 3 pin 100 phoenix connector https://www.amazon.com/gp/product/B07TQLYQ7W/
* ferrules on wires for the phoenix, https://www.amazon.com/gp/product/B07XBLGPCY llike this
* add power, piggybacked off one of the existing drivers
* routed through existing holes.
* configure z


link to fusion model for the plate https://a360.co/31iYAaa (slightly newer than dxf, but only diff is rounded corners)
and a dxf https://github.com/charlie-x/blackred-laser



* sketch of hole positions etc https://i.imgur.com/GI5tMqN.png
* foam sheet https://i.imgur.com/nw5YQlq.png
* back view https://i.imgur.com/fHuTyGB.jpg
* https://i.imgur.com/ZtqozoY.png nuts underneath
* drive power tapped from here https://i.imgur.com/az9yAoT.jpg (inital testing)
* dir/step/5v to the driver, go here https://i.imgur.com/dZJjmzx.jpg (inital testing)
* stepper driver wiring https://i.imgur.com/Y4kkJVZ.jpg connect motor phases per your stepper



* ena-/ena+ aren't used since enable on is default
* dir- to controller dir- 
* dir+ to controller +5v
* pul- to controller pul- 
* pul+ to controller +5v
* gnd to gnd on existing driver or main PSU
* VCC to power on existing driver, or main PSU. 24V make sure the driver you buy takes 24V, most do


set the current to 1.7A peak, start off with step set to 1 and make sure it moves, then step down.


since every table will be slightly different specs you may not be able to run down to 16/32 microstepping. make sure to set the acceleration in the controller. i inverted the keypad direction in the controller

only mods to the laser are the two holes for the M5 bolts , so 5.4mm drill or so.
