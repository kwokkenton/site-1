---
layout: single
title:  "Layperson summary- Optical Projection Tomography"
date:   2023-07-26 16:00:55 +0100
categories: physics 
---

# Optical Projection Tomography: CT scans but for mice?

![Illustration of the OPT setup on the left and an OPT volume image of a mouse embryo on the right.](/files/opt.png " ")

Developmental biologists are people who are interested in studying how organisms grow. They may study embryos, larvae and even whole organisms. As you may well know, scientists cannot directly perform these experiments on humans due to certain ethical reasons (imagine the uproar!). This is one reason why developmental biologists result to studying ‘model organisms’ such as mice and their embryos, that are structurally similar to humans. 

There is a need to image these millimetre-sizeed specimens. The traditional way to do this has been cutting up the embryo into hundreds of slices, imaging them sequentially and computationally stitching them together. However, this is extremely time-consuming. Optical Projection Tomography (OPT) is a relatively new volumetric bioimaging technique that does this non-invasively and is the optical analogue of X-ray CT. A few hundred images of the sample are taken, as it undergoes a complete rotation (unlike medical CT scans when the source and detector rotate instead). The stack of images is then processed using a computer with what is called the filtered backprojection algorithm to do a slice-by-slice reconstruction of your sample— allowing you to look inside it without cutting it up. This is done using visible light because biologists know how to label specific proteins or genetic material with either precipitates that attenuate light or fluorescent markers that emit light when excited with photons that correspond to its energy gap. These markers do not exist with other similar techniques such as MRI or X-ray CT. 

Biological tissue is usually milky in appearance due to the scattering of light. However, one requirement of OPT is that samples have to be see-through. Thankfully, a range of chemical techniques have been developed to perform optical clearing for us.

We constructed an OPT setup (think screws and Allen keys), wrote the image processing scripts (lots of debugging) and applied it to image an optically cleared mouse embryo (with gloves because the clearing substance is somewhat toxic). 
                      
As physicists, we wanted to determine the limits of imaging performance. One such measure is image resolution, which is the minimum distance two signals can be separated for them to still be distinguished. The resolution is limited by diffraction from the aperture in the lens, which is best at large aperture sizes. As we needed the whole sample to be in focus when imaged, we also wanted to have a large depth of field, which is favoured with small aperture sizes. This unfortunately is the trade-off in OPT! We took images of known physical targets (a sharp knife edge and a fluorescent sample bead sample) to quantify this effect so OPT users can know the optimum aperture size for their sample. 

![](/files/opt/mouse.gif " ")
*3D render of the mouse embryo we imaged.*

In addition, we also prototyped a new system that uses an LED matrix as illumination. We discovered that by illuminating successive halves of the LED and taking images over a complete rotation, we can reconstruct the entire 3D refractive index of the sample! This is pretty exciting as existing methods that do this are complicated and expensive. It can be applied to label-free imaging of zebrafish, which developmental biologists know and love. We enjoyed this project as it’s a manifestation of how physical principles, experimentation and computation all have a role in understanding complex biology— one embryo at a time.

_This article is the lay summary, meant for public engagement (with an intended audience of A-level students), that I submitted for my Master's project at Imperial College London._

<!-- You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %} -->

<!-- Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk]. -->

<!-- [jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/ -->
