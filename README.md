# sqo, sqp, sqt

Generators of Petri net models of a square grid with the following edge conditions: open edges, plugs on edges, truncated devices on edges, respectively


Description:
------------

There is a 2-dimensional square grid of size k on a plane. In each grid node a packet switching (and computing) device is situated which works in full duplex mode based on store-and-forward principle with its ports situated on facets of a unit-size square. 

sqo - edges of the grid are open, ports' places pending.

sqp - plugs, consisting of a single transition, are attached to the grid edges; a plug closes an output tract of a device port with its input tract. 

sqt - truncated devices on edges; in a truncated device, pending ports are removed together with other elements implementing the packet forwarding to/from them.

Please, consult sqo432.pdf, sqp432.pdf, and sqt432.pdf files for pictures of the obtained grids. 


Command line formats:
--------------------

>sqo k [p] [b] > pn_model.ndr

>sqp k [p] [b] > pn_model.ndr

>sqt k [p] [b] > pn_model.ndr


Parameters:
-----------

k   size of square grid (for sqt, k>1);

p   number of packets in each buffer section;

b   available buffer size.


Output (file) format:
---------------------

.ndr  "Time Petri nets graphic format" according to http://www.laas.fr/tina


Tools to display, edit, visualize, and analyze generated models:
----------------------------------------------------------------

Tina Toolbox for analysis of Petri nets and Time Petri nets http://www.laas.fr/tina

Exported from Tina, models are opened with other tools for Petri nets listed at http://www.informatik.uni-hamburg.de/TGI/PetriNets/tools/quick.html


An example:
-----------

>sgt 4 3 2 > sqt432.ndr

- Generate a model of a square grid of size 4 with truncated devices on edges; each device contains 3 packets forwarded to each of its ports, the available buffer size is 2. 

>nd sqt432.ndr

- Load the model into graphical environment of Tina. 

Menue: "Tools - stepper simulator - Rand"

- Watch the token game.


References:
-----------

Shmeleva T.R., Zaitsev D.A., Zaitsev I.D. Analysis of Square Communication Grids via Infinite Petri Nets, Transactions of Odessa National Academy of Telecommunication, no. 1, 2009, p. 27-35. 

Zaitsev D.A. Verification of Computing Grids with Special Edge Conditions by Infinite Petri Nets, Automatic Control and Computer Sciences, 2013, Vol. 47, No. 7, pp. 403–412. http://dx.doi.org/10.3103/S0146411613070262

Zaitsev D.A. Generators of Petri Net Models. Computer Communication & Collaboration, Vol. 2, Issue 2, 2014, 12-25. 
http://www.bapress.ca/ccc/ccc2014_2/2_14011024.pdf


---------------------------
http://member.acm.org/~daze
---------------------------

