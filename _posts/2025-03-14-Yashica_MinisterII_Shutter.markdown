---
layout: single
title:  "Yashica Minister II Shutter"
date:   2025-03-14 13:19:00 -0400
categories: Photography
# classes: wide
---
I recently purchased a new-to-me 62 year old rangefinder: a Yashica Minister II.  Apparently even just the name of the camera is a bit confusing, there are two different cameras that people will use the same name for.

<!-- Insert details on this here -->

Overall, the camera seems to be in remarkably good condition for its age.  The shutter and aperture adjustments turn well, with only a bit of stiffness as you move to longer shutter speeds.  One thing which was immediately obvious was the shutter times were incorrect for slower speeds.  By a 1/4th of a second, I could tell by ear that the timing was wildly inconsistent.  Before I put a roll of film through the camera, I wanted to know how reliable the shutter was at the faster speeds.  By ear it sounded close compared to a modern Nikon, but since I have a friend who works in an optics lab, I enlisted her help.

![Yashica Minister II](/assets/posts/2025-03-14/camera_on_optical_table.jpg)
*Setting up the camera on the optical table*

The idea was quite simple, align a laser through the lens and shutter aperture and measure the intensity with some photosensitive device.  Then, when we fire the shutter, we can see how long it was open by looking at the output of the photodetector on an oscilloscope.  

The good news: For the settings where the shutter sounds like it is working, it is quite quite consistent.  Shutter times varied less than 10% over many samples for shutter speeds of 1/8th and faster.  I'll admit I don't know what is a *good* consistency for a camera, but that feels reasonable to me.  Next time I have the chance and don't have film loaded in it, I'll try this experiment again with my Nikon FE and see how it does.

The bad news: The amount of time the shutter is open is incorrect for every shutter setting.  To summarize,

| Shutter (s) | Expected (ms) | Measured (ms) | Percent Error |
|---------    |----------     |----------     |---------------|
| 1/4         | 250.0         | 98.67         | 60%           |
| 1/8         | 125.0         | 290           | 132%          |
| 1/15        | 66.6          | 143.3         | 114%          |
| 1/30        | 33.3          | 74.6          | 123%          |
| 1/60        | 16.6          | 32.0          | 92%           |
| 1/125       | 8.0           | 13.6          | 70%           |
| 1/250       | 4.0           | 7.0           | 75%           |
| 1/500       | 2.0           | 3.0           | 50%           |

Not too great.  However, what's more interesting is that everything seems to be off by one stop.  If we calculate the error for all the shutter speeds being 1 stop slower that they're supposed to be, we get the following.

| Indicated Shutter (s) | Assumed Shutter (s) | Expected (ms) | Measured (ms) | Percent Error |
|---------              |--                   |----------     |----------     |---------------|
| 1/4                   |     --              | --            | --            | --            |
| 1/8                   |     1/4             | 250.0         | 290           | 16%           |
| 1/15                  |     1/8             | 125.0         | 143           | 14%           |
| 1/30                  |     1/15            | 66.6          | 74.6          | 11%           |
| 1/60                  |     1/30            | 33.3          | 32.0          | 4%            |
| 1/125                 |     1/60            | 16.6          | 13.6          | 18%           |
| 1/250                 |     1/125           | 8.0           | 7.0           | 12%           |
| 1/500                 |     1/250           | 4.0           | 3.0           | 25%           |

So it seems like the shutter works for (measured) speeds between 1/4th and 1/250th of a second, with the indicated shutter speed being one stop faster than the actual speed.  We lose a 1/500th shutter, which would be nice for sunny days, but overall still provides quite a usable range.  The built in light meter can still be used effectively as well by doubling the speed of the film, up to ISO 200 film (the highest speed metered for is 400).  Beyond that I'll just have to do the adjustment manually, which is fine until I mess it up.

I have a roll of Kentmere Pan 100 loaded that I'm about halfway through, once that is developed I'll share my thoughts on using it and some photos, assuming I'm happy with any of them.