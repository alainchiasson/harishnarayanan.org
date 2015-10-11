---
date: 2012-06-01
title: Modelling the active mechanical response of the heart
short_title: Cardiac mechanics
thumbnail: /img/research/cardiac-mechanics/biventricle-mesh.png
description: Modelling the active mechanical response of ventricular myocardium.
kind: primary
period: 2011 – 2012
---

Ventricular myocardium serves as the functional tissue of the heart
wall. Driven by intracellular calcium waves, the tissue rhythmically
contracts to finite strains. Modelling this behaviour is a key step
toward modelling the complex, coupled electro-chemo-mechanical
behaviour of the heart.

Our chemo-mechanical formulation for describing and studying the
active response of the myocardium is posed within the general
framework of continuum thermodynamics. Following the recent work of
[Holzapfel and Ogden (2009)][HolzapfelOgden2009], we treat the passive
mechanical response of the tissue as non-homogeneous, orthotropic,
nonlinear elastic and nearly-incompressible. Our automated
computational framework for nonlinear elasticity,
[CBC.Twist](/research/automated-mechanics/), allows us to easily
implement and test this physiologically-relevant constitutive model.

{{< figure src="/img/research/cardiac-mechanics/orthotropic-passive-stress.png" title="The orthotropic response of the myocardium model demonstrated by varying simple shear-stress responses along different planes defined by the muscle fibre (f), myocite sheet (s) and sheet-normal (n) directions." >}}

We then introduce, via a multiplicative decomposition of the
deformation gradient ([Ambrosi and Pezzuto,
2011][AmbrosiPezzuto2011]), an “active strain” to model the active
response of the myocardium. We carefully consider physiological facts
to arrive at a suitable functional form for this active strain in
terms of active contraction of cardiac muscle fibres. The active fibre
contraction is related to the chemical kinetics of crossbridge cycling
in cardiac muscles, which we model by a set of ordinary differential
equations ([Rice et al., 2008][Riceetal2008]). Our active model
satisfies key physical properties, including obeying the second law of
thermodynamics and ellipticity of the total stress.

We are currently designing and implementing an interface to allow us
to couple the mechanics capabilities of
[CBC.Twist](/research/automated-mechanics/) with the chemical kinetics
of cross-bridge cycling. This should soon allow us to solve numerical
problems on realistic geometries to demonstrate key aspects of the
coupled active response of the myocardium.

{{< figure src="/img/research/cardiac-mechanics/biventricle-mesh.png" title="A finite element mesh of a generic biventricle generated with CGAL." >}}

The code for this effort (Python sitting atop the [FEniCS
Project](http://fenicsproject.org/)) will be released under the GPL
once we iron out the kinks.

[HolzapfelOgden2009]: http://www.biomech.tugraz.at/files/publications/Holzapfel-Ogden_Phil_Trans_R_Soc_A-2009
[AmbrosiPezzuto2011]: http://mox.polimi.it/~ambrosi/Papers/jelast.pdf
[Riceetal2008]: http://www.ncbi.nlm.nih.gov/pubmed/18234826
