# Rust Fltk GUI for 7z

The reason for this project is to provide another GUI for 7z.

For now it can only extract 7z, Rar and Zip, if 7z plugin is installed

GUI was written in Rust FLTK.

This application was compiled for LibC 2.35. To find out which version is installed on Linux, run `ldd --version`, or in Ubunto/Debian run `dpkg -l | grp libc6`. if you see that version is 2.35 or higher - application will work.

This application was compiled without Pango package, so it uses only Cairo to apply font full hinting without anti-aliasing. This can not be changed by desktopp settings. 

Application looks like this:

<img width="700" height="494" alt="Screenshot_2026-07-13_12-17-36" src="https://github.com/user-attachments/assets/4ec08503-7451-4dac-9985-846422f91e0a" />



Archive needs to be drag-and-dropped into beige area. Application doesn't have a field for an archive path to type into.
Green rectangles "7z, Rar, Zip" indicates that those formats are supported.

So idea is very simple, drag archive into beige area. As soon as one releases mouse button, application will try to show an archive files list without a password. If this succeed files list will be provided, if not, application will put message to the low output area with error, which most likely "password is needed". So type or paste password into password input and press "list" button. Application should create archive files list. Then it is possible to extract all files by clicking axtract or select some files just clicking on them. Application calculates extracted files size for all files or for selected.

This application always extract into new folder called "Extract_date_time". It was designed to make sure that extracted file won't go into source location as a pile of files. If extraction failed folder will be empty.

After successful extraction files list will be cleaned, but not the password, so if password is the same for a few archives no need to enter it again and again.

When application starts, it creates config file in user home `/.config` directory. File name is `fltk-archiver.conf`. It has explanation inside.

If you like this application, please consider support farther development.
