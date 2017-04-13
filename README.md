# web-demo-turbulence-simulator

This simulator generates a wind speed time series that can be used in wind energy simulations. The times series is generated using the Shinozuka method, a method for generating stochastic time series. In this example, a Kaimal two-sided power spectral density (PSD) is used in the Shinozuka calculations to generate the turbulent component of wind. 

I used a very similar methodology in my electrical engineering master's thesis on the modeling and simulation of a wind turbine. Having worked in the wind energy industry for over six years now, I've unfortunately never had a reason to use it professionally! But I still think it's a neat algorithm.

The Shinozuka method is named after civil engineer Masanobu Shinozuka and I believe the method is generally attributed to his 1972 paper titled "Digital simulation of random processes and its applications". 

From the paper's abstract...
<p>"Efficient methods are presented for digital simulation of a general homogeneous process (multidimensional or multivariate or multivariate-multidimensional) as a series of cosine functions with weighted amplitudes, almost evenly spaced frequencies, and random phase angles...Possible applications include simulation of (i) wind-induced ocean wave elevation, (ii) spatial random variation of material properties, (iii) the fluctuating part of atmospheric wind velocities and (iv) random surface roughness of highways and airport runways." </p>

The "weighted amplitudes" (of cosines) mentioned in this abstract are generated through a user-defined power spectral density or PSD. Different PSD's can be selected depending on the use case, and for wind specifically there are a handful of different PSD's recognized to represent turbulence to varying degrees (Davenport, von Karman, Kaimal, etc). The one used in this example is the Kaimal PSD, which I believe was outlined in another 1972 paper titled "Spectral characteristics of surface-layer turbulence".  

All that being said, it's been a loooong time since I read any of the source material for this type of work so I'm a little rusty on making sure the math and physics assumptions line up. Either way, I really appreciate the Shinozuka methodology for the ability to generate a stochastic time series that represents a physical process such as wind. Ordo Ab Chao.

<ul>
<li><a href="http://www.sciencedirect.com/science/article/pii/0022460X72906001?via%3Dihub" target="_blank">Digital simulation of random processes and its applications, M. Shinozuka and C.M. Jan, 1972</a></li>
<li><a href="https://en.wikipedia.org/wiki/Masanobu_Shinozuka" target="_blank">Masanobu Shinozuka, Civil Engineer</a></li>
<li><a href="http://onlinelibrary.wiley.com/doi/10.1002/qj.49709841707/abstract" target="_blank">Spectral characteristics of surface-layer turbulence, J.C. Kaimal et al, 1972</a>
</ul>
