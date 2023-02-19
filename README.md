# [Chromania](https://impawstarlight.github.io/chromania)
A collection of color tools\
[Click here](https://impawstarlight.github.io/chromania)
for live demo

### Deployment
## Direct Deploy
Clone the repo and open index.html to view in your browser

#or
Clone the repo and move it to your www/html folder or
download as zip file and unzip it on an appropriate folder

## Docker Deploy
To deploy it with docker with the latest version, run the following
```bash
docker run -d -p 80:80 devsh01/chromania:latest
```

## What's new:
### v1.3 - 12 April 2022
- Palette - Save your favorite colors
- Persist preferences - Continue from right where you left
### v1.2 - 10 April 2022
- New colorspace - [OKLAB](https://bottosson.github.io/posts/oklab) (& OKLCH)
- Proper gamut mapping - More accurate estimation for out of gamut colors
- Slider optimization - Say goodbye to lag
### v1.1 - 4 April 2022
- Nearby/Similar colors - Click the match color box
- Slider optimization - Less lag hopefully
- User interace explained - [See below](#user-interface)

## Overview
- **Name**\
Find the name of a desired color from a handpicked
list of ~4k [color names](https://github.com/meodai/color-names)

- **Convert**\
Convert between various color spaces as your need
with dyanamic *shiny* sliders

- **Palette & Gradient** <sup>Upcoming</sup>\
Create beautiful & well balanced color palettes
& gradients using perceptually uniform color
spaces to achieve best visual consistency

- **Auto/Random theme engine** <sup>Upcoming</sup>\
Let's see how it goes

# User Interface

![Hints](images/hint.webp)

Everything is pretty much intuitive, except a few
things...

![Start](images/start.webp)

![Light theme](images/light.webp)

- Click the input color block to get a random color

- Click the match color block to see nearby/similar colors

![Nearby colors](images/near.webp)

![Delta E](images/delta.webp)

- The number you may see inside the match color block is
the [color difference](https://en.m.wikipedia.org/wiki/Color_difference#CIEDE2000) between the input & match.
You may not see it clearly when the difference is small.

- You can use Regular Expression in the search box

![Regex search](images/regex.webp)

![Out of gamut](images/gamut.webp)

- An asterisk will appear in the input hex when
gamut clipping happens (RGB values are out of gamut/range)

- Geek mode: The missing parts of the slider
background strip are out of gamut colors that can't
be shown in RGB colorspace.
- The bottom strip shows
estimated colors in those places by clamping RGB
values within range.
- The top strip shows the estimated
colors with adjusted transparency indicating the extent of
gamut clipping, that is, the more out of range, the
more faint colors.

![Geek mode](images/geek.webp)

![All colorspaces](images/all.webp)

## Credits

***Inspired from***\
[Name that Color](https://chir.ag/projects/name-that-color)

***List of color names***\
[GitHub/meodai/color-names](https://github.com/meodai/color-names)

