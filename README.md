# Alembic Interpolation Problem

![Unity Editor Screenshot with alembic animations](./Docs/screenshot.png)

The alembic exported from Cinema 4D with RealFlow seems to not interpolate frames and also does not support motion vectors and therefore does not have any motion blur.

## Reproduce

Run `Scenes/SampleScene.unity`

### Expected Result
There is visible motion blur on the rotating cube, the flag and the water.

### Actual Result
There is motion blur on the rotating cube and the flag, but not the water even though the Vertex Motion Scale is pushed up to 100. Also, when stepping frame by frame, the water alembic only refreshes every second to third frame.

## Setup

* Unity `2020.1.2f1`
* Alembic `1.0.7` or `2.0.1-preview1`
* Timeline `1.4.2`
* Post Processing `2.3.0`
* Windows 10 Pro

Cinema Export settings

![Cinema Export Settings](./Docs/cinema-export.jpg)

Note: Exporting Normals and or UVs does not make any difference to the described behavior.