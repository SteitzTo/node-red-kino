# Node-Red-Kino


Hi,

this is my first publishing on Github.


At home I always had the problem when I wanted to start a film evening, I had to switch on all the devices, adjust the denon receiver to the correct volume and channel, etc.

It would also be compulsory if you could do everything in one swing and the Alexa. So I dealt with my Raspi, Node-Red and the additional modules and this control came out.


## Dependencies:


[node-red-contrib-denon](https://flows.nodered.org/node/node-red-contrib-denon)

[node-red-contrib-shelly](https://flows.nodered.org/node/node-red-contrib-shelly)

[node-red-contrib-tuya-smart-device](https://flows.nodered.org/node/node-red-contrib-tuya-devices)

[node-red-contrib-virtual-smart-home](https://flows.nodered.org/node/node-red-contrib-virtual-smart-home)

[node-red-contrib-alexa-remote2-applestrudel](https://flows.nodered.org/node/node-red-contrib-alexa-remote2-applestrudel)

[node-red-node-wol](https://flows.nodered.org/node/node-red-node-wol)



## Additonal Information:

My Denon Receiver is a AVR-X3700H.  You can control it via Telnet and Webinterface.

For my implementation i use the Denon AVR-Control Protocol.

I think it works also wiht other Denon AVR Models.

I trigger the Blinds with a [Shelly 2 PM](https://www.shelly.com/de/products/shelly-plus-2pm)

The [Lamp](https://www.amazon.de/gp/product/B08BFPGWZ1/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1) is a Alexa-Ready Standlamp with a Tuya Interface.

The [Plugs](https://www.amazon.de/gp/product/B08BFPGWZ1/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1) are some Tasmota Plugs from Amazon

TV ist starting over Wake on Lan   (must be enable in TV)



----------------------------------------------------

![HomeCinema](https://github.com/user-attachments/assets/cf091b8a-aa76-477d-9895-e96a1cb37dd6)


How it works:

If you say: "Alexa turn the Kino on"    

> Denon Receiver is switched on<br>
> Denon Receiver is switched to Input Channel TV<br>
> Denon Receiver is set to Volume 20<br>
> Tasmota Plug is switched on via http request  (It turns TV an Mediabox on)<br>
> The blinds going down till 80%<br>
> The Livingroomlamp is switched on ans brighten the light to 10%<br>
> MY LG-TV start over Wake on Lan

                                             
If you say: "Alexa turn the Kino off"   

> Denon Receiver is switched off<br>
> Tasmota Plug is switched off via http request<br>
> The Livingroomlamp is switched off after 20 seconds<br>
                                             
------------------------------------------------------------------



If you want to use it too: have fun with it.

Torsten
