# What's the best wildlife (especially birds) camera?

I'm interested in wildlife photography (especially of birds), but I'm intimidated by all the expensive equipment on offer. Of course, there are plenty of blogs and vlogs suggesting the optimal "setup", but I don't trust people's opinions.

I trust data, and thankfully, Cornell's [Macaulay library](https://www.macaulaylibrary.org/) of wildlife photography has lots of it, including stunning photographs with detailed information about the cameras and lenses that took them. I thought about manually clicking through my favorites and making a mental note of the photographer's preferred equipment. But that would still be subjective. Instead, I decided to do little programming and scale this approach into something useful...

---

## Approach

Frustratingly, [Macaulay's search feature](https://search.macaulaylibrary.org/catalog?view=list) limits downloads to metadata for 10,000 photographs and does not allow filtering by rating. Thankfully, sorting by rating *is* an option. To get the most information, I'll download the maximum amount of data for each of the seven continents. I'll also restrict the data to photos from the last 10 years to enrich for cameras that you can find in retail stores.
