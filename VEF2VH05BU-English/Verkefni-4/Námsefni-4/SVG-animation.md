Inkscape is a powerful vector editor, but it does not have built-in functionality to create or preview SVG animations directly within the application's interface. 

The animation functionality described in older Inkscape wikis was part of proposed, but never fully implemented, features. 

Instead, you can achieve SVG animation using two primary methods:
Frame-by-frame animation in conjunction with an external program to create GIFs or videos.

Manual code editing using SVG's animation elements (SMIL) or CSS/JavaScript. 

Method 1: Frame-by-Frame Animation (Exporting as GIF) 

This method involves drawing each frame as a separate layer in Inkscape and then using an external program like GIMP or an online GIF maker (ezgif is a popular option) to compile the frames into an animated GIF. 

Steps:
- Prepare your artwork in Inkscape, using layers for each "frame" of your animation.
- Use meaningful names for your layers, as some tools allow you to specify the duration of each frame in the layer name (e.g., Layer1 (100) for a 0.1-second pause).
- Export the layers individually as PNG files using the Batch Export feature in Inkscape (File > Export > Export Batch). Ensure all frames have the same dimensions.
- Import the exported PNGs as layers into GIMP (File > Open as Layers) or upload them to a free online GIF creation tool.
- Set the timing and loop options within the external program, then export the final animated GIF. 
For tips on how to get the frames and timing right in Inkscape before exporting to GIMP:

Method 2: Manual Code Editing (Advanced)

This method involves preparing your SVG file in Inkscape and then manually adding animation code (SMIL, CSS, or JavaScript) using a text or code editor (like VS Code). 

Steps:

- Create your vector objects in Inkscape. 
- Assign meaningful IDs to the specific objects you want to animate using the XML Editor (Edit > XML Editor or Shift+Ctrl+X). This makes it easier to reference them in the code. Avoid default IDs like path3404 and use descriptive ones like left_arm or moving_circle.
- Save the file as "Plain SVG" (File > Save As > Plain SVG) to remove Inkscape-specific metadata that browsers ignore. Keep a copy of your original "Inkscape SVG" file if you plan to edit it further in Inkscape.

- Open the Plain SVG file in a code editor.
- Add animation code using standard web animation methods:
- SVG Animation elements (SMIL): Add <animate>, <animateMotion>, or <animateTransform> tags directly within the SVG code.
- CSS: Use @keyframes animations or transitions in a <style> block within the SVG or in an external CSS file.

JavaScript: Use the Web Animations API or libraries like Snap.svg for more complex or interactive animations.