
## What is Sinewave

A sine wave is a smooth, periodic oscillation that represents the graph of the mathematical sine function. It is a fundamental waveform in mathematics, physics, engineering, and signal processing

![[sin.png]]
### Sinewave Formula
![[formula_sinewave.png]]

### Applying the formula in Unity 

````csharp
float y = amplitude * Mathf.Sin((Tau * frequency * x) + (Time.timeSinceLevelLoad * speed)); // Formula 
````

### Full code

https://github.com/fixin0/UnitySinewaveTest



### Reference

https://youtu.be/6C1NPy321Nk?si=G1CCVdo2yz899VVf
https://vru.vibrationresearch.com/lesson/construction-sine-wave/
