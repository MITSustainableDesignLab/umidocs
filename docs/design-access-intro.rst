
.. _design_access:

Design Accessibility
====================

Motivation
----------

The utilization of high density and diversity in land-use is an effective strategy that decreases automobile dependency and contributes to more sustainable modes of transportation (namely walking and biking), as a short proximity between amenities encourages human powered transportation (HPT).To quantify the impact of applying such principles, the integration of simulation tools that evaluate cities’ “walking friendless” in the design process is becoming significant. Assessment of neighborhood walkability has long been considered a function of quarter mile to one and a half mile walking distances from housing units to vital amenities. This idea has been adapted by many walkability evaluation schemes in different forms, and has been proven to be a good indicator of “walking environments.” Popular indices such as the “Walkscore” have been validated in terms of estimating neighborhood walkability and health as well as real estate prices.

How it Works
------------

Walkscore measures the ease of residing in a certain area without depending on your car. We adapted this web-based tool to be used within the design environment of Rhino as a comprehensive modeling approach. The algorithm tests points of interest for proximity to nine North-American oriented amenities (Schools, Restaurants, Coffee, Shopping, Entertainment, Parks, Banks, Grocery and Books). Each amenity receives a different weight based on importance. Egress points for addresses are then rewarded based on distances to amenities, and a polynomial distance decay function is used to calculate scores. Within a distance of quarter mile, a full score is received, and at one mile, amenities receive about 12% of the score as a penalty. After one mile, scores slowly decrease with greater distance, until it reaches zero at 1.5 miles. There are other reward scores received by examined points based on street intersection densities and average block length. Scores range from 0 to 100.

Scoring is implemented by constructing a pedestrian travel network and performing a series of shortest-path calculations using Dijkstra's algorithm.

.. raw:: html

   <iframe width="100%" max-height="315" height="315" src="https://www.youtube-nocookie.com/embed/qgw62iRkbEU?rel=0" frameborder="0" allowfullscreen></iframe>
