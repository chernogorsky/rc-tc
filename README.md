# rc-tc
Railcore 300 Tool-Changer (HightTemp compatable)


STL is for files, original source was not publicly aviable

# Current status
Currently its a working setup, but has some minor flows to be addressed, so it may be named as a Beta stage.

I have fully functional 3 tool-heads (hemera, sherpamini+nova, bmg+mosquito, with space for another big tool), high-temp compatable (not all the plastic has been reprinted with HT version) tool changer based on RC300

# Goals


# E3D toolchange compatable railcore mod
Main goal of the project is to receive fully functiona tool changer printer based on RC300 supporint 4+ heads:
* e3d toolplate compatable. It should be able to use with little/no modification standard e3d TC heads
* e3d parking hardware compatable. Due to design diff e3d parking models may not be used without full redesign.

# High temperature compatable
Another objective is to have an option to perform under *135C* chamber temperature and HT extruders, 
So:
* all the motors are HT, or moved away from the chamber
* Z probe may be HT probe or HT microswitch
* all the plastic/other parts within enclosed area should be HT ready (HT plastic, silicon wiring, CNCed, ...)


# Stay as close to the original RC as possible
Here I want to be able to:
* utilize some of the upgrade I already have. so far in use:
  * all the frame alums upgrades
  * MR belts retainer
  * upper part of BMG ultralight mount (as part for BMG/Mosquito head)
* Be able to go back/forth without huge modification (currently its only removing the shaft)
 * you may use any plate-on mods, like mounts (except for fan shrounds)
 * no heavy hull mods 


# Dimentions
<img width="551" alt="rc-tc-drawing" src="https://user-images.githubusercontent.com/5332569/127501504-d607ab26-c6cb-4ddb-bb29-99ad0ac055d9.png">


## Height Diff
Height diff between rail mounts and center of the shaft is "-6.6 mm"

## Z
Z is below the shaft center by 27.57 mm

## X
X is 35.85 mm and 41.45 mm both sides from the center of the shaft

## Z
Z is 29.85 mm (without bltouch/httouch) / 46.4 mm with

# BOM

## CNC
* Face plate should be CNCed
* May wont to mill/cnc twist lock

## Plastic part
* Since it's a HT version of the tool changer, all of the parts should be print with HT plastics, eventially
* No heavy force is expected to any of the parts, except for the back pulley, so it may be print by any HT plastic. 
* Back pulley is better to be print from something rigid and solid (Polymaker PCMAX; PC; etc) (for me  HT PLA with 100% infil works during all the tests)
* Parking mounts - have to be rigid matereal, probably with CF inside.

## Remote lock
You need all the details for remote lock from jubilee design

(Not a full list)
* motor (im using stepperonline, so my mount is for it) (stepperonline/filastruder) (mine is 14HS13-0804S-PG5)
* spring guide (https://www.filastruder.com/collections/jubilee/products/wire-cable-and-spring-guide-set-for-jubilee)
* alum hub (https://www.filastruder.com/collections/jubilee/products/aluminum-hub-6mm-id)
* pulley spring (2x https://www.filastruder.com/collections/jubilee/products/rel-replacement-extension-spring)
* twist lock (https://www.filastruder.com/collections/jubilee/products/twist-lock-assembly-for-jubilee) * should be cutted with dremmel

## Nozzle cleaning/whiping
Im using mod from e3d mod and bigbrain3d whiper. If you decide to do that, you'll need 
* HT pancake motor (LDO-42STH25-1404MAH)
* 35 mm round HT motor with 8/10 teaths gear installed (LDO-36STH17-1004AHG8 or LDO-36STH17-1004AHG Stepper)

## Tools
Im using e3d plate and docks, so you may need some of these:
* plate only 
* plate with dock (https://www.filastruder.com/products/e3d-toolchanger-blank-tool-plate-and-dock-kit?_pos=4&_sid=0a385e1ae&_ss=r)
* dock only (https://www.filastruder.com/products/e3d-toolchanger-dock-fixings-kit?pr_prod_strat=copurchase&pr_rec_pid=4507212218439&pr_ref_pid=4507215724615&pr_seq=uniform)

## Electronics
This project is required you have control board with  support for:
* 5 axis (X, Y +3Z) steppers
* 4 (your number) heads steppers
* 1 remote lock motor steppers
* (optional) 1 remote probe servo control
* (optional) 2 steppers for HT wiper

My setup is duet3 6hc + 2x 3hc + 1x ToolBoard

## Power and electronics layouts
* I moved all the power supplies away from the printer
* I have 24V 400W rated (AWG12/16) main power lines
* I've utilized fully right side of the rc300 std electronic space and start using left side

## Enclosure/chamber
TBD,
there is a working solution from HighTemp3d, and several custom made


# Tested setups
## Original
Im using RC300 with: 
* alum full body (713Maker)
* all the alums upgrades (mandala rose + 713maker):
 * belt tention is from mandala rose
* magnum pulley (mandala rose)
* Halo for nema17 (713Maker)
* belts rated for 135C (e3d-online.com/hightemp3d.com)

* Enclosure TBD (mandala rose/hightemp3d/selfmade)

