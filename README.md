# MCP23008 io-wing

* IO expander wing for adafruit feather boards

Missing IO pins in your feather project? The MCP23008 I2C GPIO expander is great for situations like this. It attaches to the I2C bus and you can include up to 8 of these chips on a single device.

## Configure I2C adress

On the left side of the wing you'll notice 3 small solder jumpers labeled A0 - A2. By shorting out the solder jumper A0, A1, and A2 you can change the I2C address of the MCP23008 chip. To make this board flexible, the solder jumpers connect to VCC (shorting the jumper sets value 1) and there are 10K pull-down resistors on the address lines. 

| A2 | A1 | A0 | Address |
| --- | --- | --- | --- | 
| open | open | open | 0x20 |
| open | open | closed  | 0x21 |
| open | closed | open | 0x22 |
| open | closed | closed | 0x23 |
| closed | open | open | 0x24 |
| closed | open | closed  | 0x25 |
| closed | closed | open | 0x26 |
| closed | closed | closed | 0x27 |

## Using interupt

To use the interupt pin from the MCP23008 short the solder jumper on the backside of the wing to connect the interupt to the corresponding pin. 
