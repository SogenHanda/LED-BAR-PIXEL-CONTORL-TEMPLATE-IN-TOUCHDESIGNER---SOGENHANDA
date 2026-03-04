# LED-BAR-PIXEL-CONTORL-TEMPLATE-IN-TOUCHDESIGNER---SOGENHANDA


# TouchDesigner LED Bar Pixel Mapping Template (.tox)

This `.tox` is a TouchDesigner template for controlling LED bar lights using a pixel mapping workflow.

The system converts a TOP-based pixel map into DMX signals, allowing easy visual control of the bar light using standard TouchDesigner TOP operators.

## Supported Light

This template is designed for the following LED bar light:

https://www.amazon.co.jp/dp/B0D7PZ1LYR

The system assumes **1 × 28 pixel mode (112CH DMX mode)**.

Each pixel contains **RGBW**, resulting in a total of **112 DMX channels**.

## Features

- Control the LED bar light directly using a **Ramp TOP**
- Easily create dynamic lighting using **Transform TOP**, **Level TOP**, or other TOP operators
- Simple pixel-mapping workflow inside TouchDesigner
- Automatic conversion from pixel color data to **112CH DMX signal**

## Workflow

The system works with the following process:

1. Create a **1 × 28 pixel map** using a TOP.
2. Calculate **RGBW values for each pixel**.
3. Convert the pixel data into **112CH DMX signals** using DAT and CHOP operators.

### White Channel Extraction

The **W (white) channel** is extracted using **minimum RGB separation**:

```
W = min(R, G, B)
```

This helps maintain color consistency when converting RGB to RGBW.

## Contact

If you have any questions or feedback, feel free to contact:

sogenhanda@gmail.com

## License

Sogen Handa — All rights reserved.
