---
layout: page
title: PhD Project
description: Simulation of ember storms
img: assets/img/dom.PNG
importance: 1
category: work
---

Embers have been identified as the leading cause of house loss in previous fire events. Near the wildland–urban interface (WUI), areas where structures and developments meet wildland, embers pose a greater risk as small ember particles can flow over roads and terrain into properties, increasing the likelihood of structure damage. Although recent computational works have provided a significant insight into ember transport, the current models do not capture the near-ground behaviour and transportation of embers, and the entrainment (the process through which near-ground particles are introduced into the flow) of embers from the ground, both of which are key factors in ember storms. This project aims to improve current ember modelling to capture near-ground entrainment and relofting by analysing and adapting existing particle transport models and applying them to model ember storms using large eddy simulation (LES) in Nek5000, a popular spectral element solver. The implementation of these models will help develop more robust simulation techniques. This will ensure that authorities are better equipped to deal with wildfires at the WUI and formulate better mitigation strategies.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/wui.png" title="WUI" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    An example of a wildland-urban interface (WUI).
</div>

The project utilises computational fluid dynamics (CFD) as the primary tool. In CFD, fluid flow is simulated by numerically solving the mass, momentum, and energy conservation equations, collectively called the Navier-Stokes equations. There are three major CFD methods: direct numerical simulation (DNS), large eddy simulation (LES), and Reynolds-averaged Navier--Stokes (RANS). Because highly turbulent flows contain different scales of motion, it becomes computationally impossible to simulate large domain sizes (for example, atmospheric flows) using DNS. For such simulations, LES is a convenient method that captures the largest and more relevant scales of turbulent motion and accounts for the unresolved smaller scales using a turbulence dissipation model.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/dom.PNG" title="domain" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Schematic of a typical computational domain.
</div>

In current computational studies, embers are generally modeled as Lagrangian particles in LES. The project will implement certain models which will be used to investigate the effects of a number of parameters on ember transport, such as, forest type as quantified by leaf area index and idealised buildings, represented by regular shapes with a height and separation distance. These parameters will be systematically varied to study how embers behave at the WUI and identify areas of heavy and light ember accumulation based on building parameters. A potential application of this research is to develop a RANS model of ember accumulation.

WUI areas are rapidly growing; the fastest growing suburbs of Sydney, Canberra, and Hobart are on the wildland urban edges. The communities on the WUI must be resilient to bush fire hazards. This work will improve simulation of ember transport at an idealised WUI, with an eye towards future development of a reduced model of ember transport for risk management purposes. The knowledge gained from those simulations can then provide thresholds for the safe spacing between structures and potentially other mitigation measures within the WUI, thereby informing the development of safer WUI communities.
