# Tube Detection

### Images

`data/annotated_images/` contains **70 PNG images** (640x480, RGB).

Each image is an overhead photo of a surface with microcentrifuge tubes. The number of tubes per image varies (3-6). Backgrounds include desks, white surfaces, black surfaces, and mixed-color surfaces.

### Annotations

`data/annotations.csv` contains ground truth for all 70 images (371 total tubes).

| Column      | Type   | Description                                                |
|-------------|--------|------------------------------------------------------------|
| `image`     | string | Image filename (e.g. `2659ffa5-color.png`)                  |
| `center_x`  | float  | Tube lid center, x-coordinate in pixels                    |
| `center_y`  | float  | Tube lid center, y-coordinate in pixels                    |
| `bbox_x`    | float  | Bounding box top-left x                                    |
| `bbox_y`    | float  | Bounding box top-left y                                    |
| `bbox_w`    | float  | Bounding box width                                         |
| `bbox_h`    | float  | Bounding box height                                        |
| `bbox_rotation` | float | Bounding box rotation in degrees (clockwise)           |
| `angle_deg` | float  | Tube lid rotation angle in degrees, range [0, 360), defined by joint-to-tab direction |

### Coordinate System

- Origin is the **top-left** corner of the image.
- X increases rightward, Y increases downward.
- Angle 0 degrees points along the **positive X-axis** (rightward).
- Angles increase **counter-clockwise**.
- Rotation angle of the tube is defined by the direction of the joint to the tab.

