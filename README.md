# Procedural Buildings

## Description

In this project, I created a multi-floor procedural building generator in Houdini.

Inspiration comes from traditional temple towers.

| <img width="300" alt="image" src="https://github.com/user-attachments/assets/3ec19c16-5026-4d64-8f5f-29e221846f8b" /> |
|---|
| *Temple Tower*|

## Demo:

https://github.com/user-attachments/assets/1b8c9790-5552-4afc-9c13-e83d8779d96f

## Part 0: Floor Box

First step of the project is to create box according to the params as the main body of current floor. Besides, I added some attributes here as well as a material.

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/4b82f5a9-25ed-4e9c-92c8-86f64bead09f" />

## Part 1: Windows and pillars

After that, I scattered the windows and pillars onto each walls according to the setting params. I also make sure that there will be no windows on the Z+ wall on first floor, which is expected to put doors on it.

Additionally, the width of these windows and pillars can be controlled by a controller node. And to ensure the pillars and windows are arranged as "PWPWP....WP " and centered, I implemented some logic in Attribute Wrangle and Chain nodes.

<img width="1958" height="1099" alt="image" src="https://github.com/user-attachments/assets/ccb2fc81-05fc-45fb-aba5-6dadcadb0731" />

## Part 2: Borders and Corner Pillars

In this part I created the border on the top of the floor using Sweep Node and four big pillars in each corners.

<img width="2140" height="877" alt="image" src="https://github.com/user-attachments/assets/0e19eb2d-5c5f-4de8-8310-a92b0fde4c53" />

## Part3: Supporting Roof between Floors

In this part, I created procedural roof between the floors just like those in my concept picture.

To implement this, I divided the roof into corner parts and tiles. Then I assembled them to fit the floor size of both floors.

There are quite a lot details in this part. For example, I moved up the floors to make the roof fit the geometry, and I dynamically changed the tile's scale to make it fit the whole edge.

<img width="2319" height="1009" alt="image" src="https://github.com/user-attachments/assets/c20a5e2b-03a8-4502-a07c-7578a0feecc1" />

## Part4: Top Roof

This part I implemented the roof on the top floor using similar logic as part 3. And I also created a top plane to cover the building.

<img width="2228" height="1119" alt="image" src="https://github.com/user-attachments/assets/737acd4a-84f8-4911-a621-24c78f8f77d6" />

## Part5: Details

In this part I added a controll node to modify the scale of some of the objects. I also added two stone lions and brick floor to the building. And the lion will be auto arranged according to the building's params.

<img width="1453" height="790" alt="image" src="https://github.com/user-attachments/assets/dc865d37-d405-4273-8335-604cba09b579" />

## Final Results

<img width="1487" height="1102" alt="image" src="https://github.com/user-attachments/assets/23bb1acd-b00c-4298-beb0-82730cf6be80" />
<img width="1126" height="1018" alt="image" src="https://github.com/user-attachments/assets/c6ca5716-d744-4883-9a00-3ffb8852f230" />
<img width="846" height="891" alt="image" src="https://github.com/user-attachments/assets/cc9a3dc1-87c5-440a-8000-a0d68ae79e54" />


