# HST_sky_RMS

**Codes to determine sky background RMS and contamination rates of HST images.**

Takes drizzled _Hubble space Telescope_ (HST) images, with `build=True` in `Astrodrizzle` from [DrizzlePac](https://www.stsci.edu/scientific-community/software/drizzlepac.html), as inputs. Code creates a segmentation map with `photutils` for source detection.

**For RMS test:** Code measures the root-mean-squared (RMS) of the sky background within randomly placed apertures where there are no objects. Then plots a histogram, Gaussian of distribution, and averages of the RMS measurements. With additional user inputs, can determine a limiting magnitude of the image within a user-defined aperture size.

**For contamination rates:** Code places random apertures (size set by user to best match sources of interest) and determines how many have significant overlap (set by user) with objects in the segmentation map. Determines a contamination rate for sources in the input image.
