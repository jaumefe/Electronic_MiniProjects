# Project_2

## Description
This is a [LibrePCB](https://librepcb.org) project!

* Build a parallel resonant circuit for a frequence of 50Hz.
<center>
<img src="Project_2.png">
</center>

* A 10uF capacitor is compulsory to be used.
* In order to minimize the nominal value of the inductor, an equivalent element with operational amplifiers, resistors and capacitors must be used.

## Components
* Operational amplifier: LM741, TL071, TL081 or equivalent
* Resistors and capacitors
* Input voltage of +/-12V or +5V

## Solution
For a frequence of 50Hz, it is necessary to use an inductance of 1H. This inductance can be calculated knowing that f = 1//(2*pi*sqrt(C1*L1)).
As the inductance should be simulated with operational amplifiers, resistors and capacitors; it is used a circuit called inductance simulator, based on an AOP circuit and two resistors.
The equivalent inductance is computed as: Leq = R2/(R3*C*(2pi*f)²), so it is frequency dependent.
The values chosen are: R2 = 1k; R3 = 1k; C = 10uF.

## License

See [LICENSE.txt](LICENSE.txt).
