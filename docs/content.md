# What's the best camera for bird photography?

I'm interested in wildlife photography (especially of birds 🦜), but I'm intimidated by all of the expensive equipment. Of course, there are plenty of blogs and vlogs suggesting the optimal "budget setup", but I don't trust opinions.

I trust data, and thankfully, Cornell's [Macaulay library](https://www.macaulaylibrary.org/) of wildlife photography has lots of it. Including stunning photographs with detailed information about the cameras and lenses that took them.

I thought about manually clicking through my favorites and making a mental note of the photographer's preferred equipment. But that would still be subjective. Instead, I decided to do little programming and scale this approach into something useful.

## Approach

The [Macaulay library](https://www.macaulaylibrary.org/) has a staggering 68.5 million photographs of birds, and many are annotated with technical details of the photographer's camera. Additionally, the photos are rated on a scale of 1-5 by dozens of community members. Sorting the photos by rating returns the most stunning images in the entire library. *All of the cameras that took those images are worthy of purchasing, but are there cameras that take a disproportionate number of these amazing photos? If there are, wouldn't those be the best cameras to buy?*

The great people of Cornell Ornithology made it possible to download metadata of the images in the library. Sadly, you can only download 10,000 records at a time.

To maximize the number of images, I downloaded the metadata for 10,000 rating-sorted records of photos taken in the last nine years in each of the seven continents. This resulted in 70,000 of the "best" images from around the world in the [Macaulay library](https://www.macaulaylibrary.org/).

I wanted to ensure my data included *high quality* photos taken by a *wide range* of people, so I filtered the data to remove images with poor (less than 4) or few (less than 20) ratings. Then, I ranked each photographer's images by its rating weighted by number of people who rated it. I took the top image from each photographer, resulting in a dataset of the best rated images of ~3,200 individuals.

Frustratingly, the camera information is included on the website but not in the downloadable metadata. I remedied this by scraping the camera information off the page associated with each photo's catalog number. I only kept the ~2,700 records that specified the camera's model. *My thought is that the camera that's taken the majority of these 2,700 photos must be the best camera.*

Of course, this isn't a particularly *scientific* analysis, and several confounders will influence the top cameras. Ultimately, camera choice is a product of industry preferences, blogs, vlogs, and all the subjective stuff I hoped to avoid. But, these cameras *are* responsible for the some best photographs of birds, and although the cameras at top of this dataset represent *preference*, they also represent *proven tools* of wildlife photography. This isn't to say that cameras absent from this dataset aren't capable. But, cameras in this dataset are *safe* choices for those getting into wildlife photography.

## Results

There are two facets of the results: *which cameras are the most popular*, and *what lenses work best with those cameras*.

### Which cameras are best?

Below, I've plotted every camera in the dataset by it's frequency——how popular it is——and it's cost on the used market. I encourage you to explore the data yourself: **mouseover** a point to see details; **click** on a point in the legend to show only that brand;**pinch** to zoom into a tightly clustered region of the plot; **click** on a point to see the most highly rated image that camera's taken.

<div class="vega-plot" id="summary_scatter" data-plot-id="summary_scatter"></div>

Two cameras stand out: the **Canon EOS 7D Mark II** and **NIKON D500**. I noticed that both cameras were responsible for a large percentage of nice photos from my local area prior to doing this analysis. It's interesting to see "global" trends reflecting the preferences of photographers in my local park.

### What lenses are best?

Lenses are brand and camera specific so identifying the most "popular" lens won't be much use. However, I can use the knowledge of the focal length and aperture from each picture to figure out which specifications your lens should have.

First, I looked at the distribution of focal lengths in the data.

<div class="vega-plot" id="focal_length_hist" data-plot-id="focal_length_hist"></div>

The average focal length used to capture these top images was roughly 500mm. Almost 80% of all top images are taken between 250mm and 600mm, a range covered by many affordable lenses.

Next, I looked at which aperture was the most common. Wide apertures (low numbers) come at a premium.

<div class="vega-plot" id="aperture_hist" data-plot-id="aperture_hist"></div>

A large bulk of the photos are taken with apertures between f/5.6 and f/8. There are lenses with a minimum aperture of f/11, and it's probably best to avoid these.

## Conclusion

I don't know 🤷🏻. This is mostly a resource. It certainly suggests that the **Canon EOS 7D Mark II** and **NIKON D500** are excellent choices. They're cumulatively responsible for nearly a third of the highest rated images in the [Macaulay library](https://www.macaulaylibrary.org/) taken by ~3,000 different photographers. I think that's significant. What's more, both are fairly affordable——the **Canon EOS 7D Mark II** in particular.

For lenses, the data suggests that you *want* a lens with an aperture at least as wide as f/5.6. You also *want* a lens with at least 400mm of zoom. Honestly, a 400mm f/5.6 prime lens wouldn't be a bad choice. Alternatively, if you can afford a 200-500mm lens, you've got the reach of most cameras in the dataset.
