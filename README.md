Schematic and layout in been updated to kicad 9 PCB for a quad bm1387 standalone miner
// skip if deemed off topic!
// Other versions made<b
// A single BM1391 version, obsolete as information on the asic is too scarce
// aSiNine Pharaonis: dual BM1387 version, compatible with the quad version (this)
// Unnamed project single BM1397 (in pre-alpha stage, pcb's are on the slow boat from China)

Motivation:
i have been interested on making a usb miner for home lotery mining using the bm1387 and hopefully other older asic chips with modem interface 
Properties (concept):
- Standalone miner to be connected to a mining pool or a private Bitcoin node that will serve the work (over websocket)
- Size: 80x60mm
- Programmable Vcore for the bm1387 asics
- ws2812 led for special effects ;)
- max. power usage targeted at ~10-15W
- Cooling: M.2 SSD cooler, tie-wrapped to the board with 5V fan.
- Low(est) cost possible!

Major parts used:
- 4x BM1387xx asics (tested bm1387bf & bm1387b)
- ESP32-C3-mini-1
- SY8208A or B step down regulator (8A) <s>(currently controlled by PWM, considering a cheap ($0.10) DAC)</s> controlled by a dac.
- XC6206P-18 lin. regulators for 1.8 & 0.8V
- SY8009B step down regulator (overkill) for the esp32c3, limiting the power supply to 5V only..
- usb-c connector for power (5V) and debugging 

todo: 
- redesign the power to use usb-c 12v to conected to some mosfets with a proper power managment ic 
- make a version but using 4 x bm1385 asic's
- build the firmware for the esp 
