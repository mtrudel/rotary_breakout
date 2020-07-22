# Rotary Breakout

<img src="https://644db4de3505c40a0444-327723bce298e3ff5813fb42baeefbaa.ssl.cf1.rackcdn.com/0a38596faf87c3f658f8245b33c8096c.png" width="200"/>

A simple breakout board for PEC11 rotary encoders (as [sold by Adafruit](https://www.adafruit.com/product/377)).

Designed to be paired with a 4 pin JST header

Pinouts in the above image from top to bottom are:

* Ground
* A (quadrature trigger)
* B (quadrature direction)
* Z (button press)

## Usage Guide

If you're new to rotary encoders, their use can be non-obvious. The typical approach I take is to:

0. Set up pullup resistors on both pins A and B.
1. Set up an edge triggered GPIO monitor on pin A, looking at rising edges only.
2. When you see a rising edge on A, immediately read the value of B. If it's high, you just rotated clockwise. If it's low, you just rotated counter-clockwise. 

Available at [OSH Park](https://oshpark.com/shared_projects/ICPLLnfp)

# License

MIT
