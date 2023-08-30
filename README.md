# Instruction for Merging 360 Clips for Youtube

## Export Flatten 360 Videos (Insta360 Studio)

Export flatten 360 videos from `Insta360 Studio`
1. Select all the 360 clips wanted
2. Right click, then select `Export all`, with the following settings:
   - `Original resolution`
   - `Extreme high` bitrate
   - `H.265` (same quality as H.264 but smaller size)
   - Select `Video`, not `Video (original)`


## Merge Multiple Flatten 360 Videos Into One Flatten 360 Video
Download a free tool from https://github.com/mifi/lossless-cut
- The executable version is free

Steps:
1. Set working directory to `Download`
2. Add all the flatten 360 videos to be merged
3. On the `Batch File List` on the left, select the icon `Merge/Concatenate Files...`
4. **Uncheck any options about metadata** in `Options`, since they seem not work for Youtube.
5. Output as `MP4`, then click on `Merge`.

The merged video **does not** contain 360 metadata for Youtube.


## Adding 360 Metadata to Flatten 360 Videos

Download the source code:
> tags > v2.1 > download source > unzip > open `spatialmedia` folder > run `python gui.py` with python 2

Steps:
1. `Open` the merged video
2. Check `spherical (360)`
3. Uncheck anything else.
4. Click on `Inject Metadata`


### How to Install Python 2.7 With Conda

> CONDA_SUBDIR=osx-64 conda create -n py27 python=2.7

from: https://stackoverflow.com/questions/67380286/anaconda-channel-for-installing-python-2-7






# Spatial Media
A collection of specifications and tools for 360&deg; video and spatial audio, including:

- [Spatial Audio](docs/spatial-audio-rfc.md) metadata specification
- [Spherical Video](docs/spherical-video-rfc.md) metadata specification
- [Spherical Video V2](docs/spherical-video-v2-rfc.md) metadata specification
- [VR180 Video Format](docs/vr180.md) VR180 video format
- [Spatial Media tools](spatialmedia/) for injecting spatial media metadata in media files
