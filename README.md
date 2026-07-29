# FRA371 Lab 0 - Robot Setup

After the installation check passes, add your own robot to this project and confirm
it loads.

## 1. Move your robot into `my_robot/`

Your robot comes from a **URDF exporter** (your CAD tool): one `.urdf` file and a set
of `.stl` meshes.

1. Put your mesh files in `my_robot/meshes/`.
2. Save your URDF as `my_robot/robot.urdf`.

## 2. Re-path the meshes

In `my_robot/robot.urdf`, every mesh path **must** look like this:

```xml
<mesh filename="package://my_robot/meshes/YOUR_FILE.stl"/>
```

## 3. Check your robot

```
python check_robot.py
```

What you should see:

- `[ok] loaded ...` and `[ok] all mesh files found`
- a browser tab showing **your robot**, then it closes.

If a mesh is missing, the script lists the file - fix the path or add the file, then run
it again.
