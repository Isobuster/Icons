# IsoBuster.Icons
Use custom icons with IsoBuster

It is possible to use your own icons with IsoBuster (>= 5.x)

To do this:

1. Navigate to the IsoBuster "Styles" folder, which was created during installation.
  For instance here: "C:\Program Files (x86)\Smart Projects\IsoBuster\Styles" (32bit)
  Or here: "C:\Program Files\Smart Projects\IsoBuster\Styles" (64 bit)
  
2. Create a sub-folder: "Icons"

3. Place *.png files with very specific names in this folder.

On startup, IsoBuster looks in this folder and loads all the pngs that are named correctly.
The naming convention is:
[Group].[Number]-[Dimension].png

There are 5 groups:

0. State icons (the additional icons shown on the left hand side of normal icons, in the (right hand side) ListView
1. Media icons (Folder, Partition, CD, ..)
2. Overlay icons (Deleted, not yet expanded/explored, ..)
3. File System icons (UDF, NTFS, ..)
4. General application icons (Help, Refresh, ..)

Depending on the group there are a number of icons.

Per [Group].[Number] IsoBuster tries to load icons with very specific dimensions.
IsoBuster looks for: 16, 20, 24, 32, 40, 48, 64, 128 and 256
Other dimensions are ignored.  Obviously 16 means: 16x16, 20 means: 20x20 etc.

During program operation, IsoBuster picks the most appropriate dimension to display.
This depends on the required size and the system dpi settings. IsoBuster also scales it to the required size on the fly.

For icons that scale well it is sufficient to provide only one or two dimensions.  
For instance, if a large 256x256 icon scales well to 16x16 it is sufficient to only provide the [Group].[Number]-256.png icon.
Realistically speaking, if your system setting scales 100-150%, 64x64 suffices, but if you use higher scaling settings, larger icons will improve the crispness of display.
For icons that don't scale well or need slightly different variants in the smaller sizes, it is best to provide those dimensions as required.
