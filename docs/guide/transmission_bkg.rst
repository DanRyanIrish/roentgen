Theory of Transmission and Absorption
=====================================

Mass Attenuation Coefficient
----------------------------
If a narrow beam of monoenergetic photons with intensity, :math:`I_0`, are impinged on a material of thickness
:math:`x`,the intensity is attenuated exponentially,

.. math::
  I(x) = I_0 \exp(-\mu x)

The parameter :math:`\mu` is called the linear attenuation coefficient and measures the absorptivity of the material. It
has units of :math:`cm_{-1}`. This value captures the sum of the probabilities of individual processes which might
remove an individual photon from the impinging beam. Those interactions most relevant to the x-ray and gamma-ray range
are the photoelectric interaction and Compton scattering. In a photoelectric interaction, the entire incident energy of
the interacting photon absorbed by the material while in Compton scattering, only a portion of the incident energy is
absorbed. These interactions are energy dependent which means that the linear attenuation coefficient is also.

Another more popular way to represent the linear attenuation coefficient is through the mass attenuation coefficient or

.. math::
  \mu_m = \frac{\mu}{\rho}

where :math:`\rho` is the density of the medium. It has units of :math:`cm^2 g^{-1}`. This is the measure used by this
module.

This equation can be re-written in the following form

.. math::
  \frac{\mu}{\rho} = \frac{1}{x} \ln(\frac{I_0}{I})

which suggests a method for measuring the mass attenuation coefficient.

Transmission and Absorption
---------------------------
As described above the probability of transmission through a material is given by

.. math::
  I_{trans} = I_0 \exp(- \frac{\mu}{\rho} x)

therefore the absorption is given by

.. math::
  I_{trans} = I_0 (1 - \exp(- \frac{\mu}{\rho} x))


Multiple Materials
------------------
Since we are dealing with probabilities of interactions if there are multiple materials present the probabilities
must be multiplied. For example, if we are interested in the amount of flux which passes through two materials, a
and b, it would be given by the following equation

.. math::
  I_{trans} = \exp(- \frac{\mu_a}{\rho_a} x) * \exp(- \frac{\mu_b}{\rho_b} x)

If we are interested in the amount of flux deposited in a detector after going traveling through a thin window

.. math::
  I_{trans} = \exp(- \frac{\mu_a}{\rho_a} x) * (1-\exp(- \frac{\mu_b}{\rho_b} x)


Reference
---------

* `Mass attenuation coefficient Wikipedia <https://en.wikipedia.org/wiki/Mass_attenuation_coefficient>`_