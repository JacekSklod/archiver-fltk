# Rust Fltk GUI to 7z

The reason for this project is to provide another GUI for 7z.

For now it can only extract 7z, Rar and Zip, if 7z plugin is installed

GUI was written in Rust FLTK.

This application was compiled for LibC 2.35. To find out which version is installed on Linux, run `ldd --version`, or in Ubunto/Debian run `dpkg -l | grp libc6`. if you see that version is 2.35 or higher - application will work.

This application was compiled without Pango package, so it uses only Cairo to apply font full hinting without anti-aliasing. This can not be changed by desktopp settings. 

Application looks like this:
<img width="939" height="662" alt="Screenshot_2026-07-13_12-17-36" src="https://github.com/user-attachments/assets/2a232e07-099b-449b-b998-2ab9426d5854" />

Archive needs to be drag-and-dropped into baige area. Application doesn't have a field for an archive path to type into.
Green rectangles "7z, Rar, Zip" indicates that those formats are supported. 
