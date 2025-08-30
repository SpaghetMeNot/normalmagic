# Smooth Normals :construction_site:

Smooth Normals will smooth mesh normals without smoothing mesh topology. 

Some common use-cases for this are:

- Achieve good shading on difficult topology. (Pinched, uneven or distorted normals).
- Achieve stylized effects:
    - Improve cel shading contours.
    - Flatten normal islands.
    - Fake SSS by mixing face corner and point normals together.
    