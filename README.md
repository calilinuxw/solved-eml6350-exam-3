Download Link: https://assignmentchef.com/product/solved-eml6350-exam-3
<br>
This is a open book and open notes exam. Copying someone else’s code or solution is considered a violation of the university honesty policy. NOTE: READ ALL THE INSTRUCTIONS. If you need to make any assumptions, list them (e.g., if you need to restrict the domain, assume some trigonometric property, etc.). UPLOAD A SINGLE PDF OF YOUR SOLUTIONS AND YOUR CODE IN A SINGLE ZIP FILE ONLINE. PLOTS NOT FOLLOWING THE CORRECT FORMAT WILL NOT GET FULL CREDIT. IF SOMETHING IS NOT CLEAR PLEASE ASK.

<ol>

 <li>Consider the following switched dynamic system of a vehicle moving through a field with intermittent feedback of the position</li>

</ol>

<em>mη</em>¨(<em>t</em>)       = −<em>cη</em>˙ (<em>t</em>) + <em>τ </em>(<em>t</em>) + <em>d</em>(<em>t</em>)

where are the x-y position, velocity, and acceleration of the mass,

<em>m,c </em>∈R<em>&gt;</em><sub>0 </sub>are the unknown constant mass and resistance coefficient, <em>τ </em>∈R<sup>2 </sup>is the input, and <em>d </em>∈R<sup>2 </sup>is an unknown time-varying bounded disturbance. Assume <em><u>m </u></em>≤ <em>m </em>≤ <em>m</em>, <em><u>c </u></em>≤ <em>c </em>≤ <em>c</em>, and ∥<em>d</em>(<em>t</em>)∥≤ <em>d </em>where the bounds are all known. The vehicle is equipped with a well calibrated devices to measure acceleration and velocity at any time; however, measurements of position are infrequently available. All of the measurements have an unknown time-varying bounded noise with the following measurement models where is the time of the <em>j</em>th measurement of the position, <em>η<sub>m</sub>,η</em>˙<em><sub>m</sub>,η</em>¨<em><sub>m </sub></em>∈R<sup>2 </sup>are the measured values and <em>ω<sub>η</sub>,ω<sub>η</sub></em><sub>˙</sub><em>,ω<sub>η</sub></em><sub>¨ </sub>are the bounded noise values with the known bounds ∥<em>ω<sub>η </sub></em>(<em>t</em>)∥ ≤ <em>ω<sub>η</sub></em>, ∥<em>ω<sub>η</sub></em><sub>˙ </sub>(<em>t</em>)∥ ≤ <em>ω<sub>η</sub></em><sub>˙</sub>, and ∥<em>ω<sub>η</sub></em><sub>¨ </sub>(<em>t</em>)∥ ≤ <em>ω<sub>η</sub></em><sub>¨</sub>. The goal is to track a circle trajectory of radius <em>R </em>∈ R, at a frequency <em>f </em>∈

R which we model as , implying , and <em>η</em>¨<em><sub>d </sub></em>(<em>t</em>) =

despite position measurements intermittent availability.        For the following,

assume <em>m </em>= 250 kg, <em>c </em>= 25 kg/sec, <em><u>m </u></em>= 200 kg, <em>m </em>= 300 kg, <em><u>c </u></em>= 20 kg/sec, <em>c </em>= 30 kg/sec, <em>d </em>= 0<em>.</em>5 N, <em>ω<sub>η </sub></em>= 0<em>.</em>1 m, <em>ω<sub>η</sub></em><sub>˙ </sub>= 0<em>.</em>005 m/sec, <em>ω<sub>η</sub></em><sub>¨ </sub>= 0<em>.</em>01 m/sec<sup>2 </sup><em>R </em>= 100 m, <em>f </em>= 0<em>.</em>003 Hz. (a) (30 pts) Let the estimation error <em>η</em>˜ be defined as

<em>η</em>˜ = <em>η </em>− <em>η</em>ˆ

where <em>η</em>ˆ is the estimate. Since <em>η </em>is unknown except at specific times, determine the maximum amount of time (the maximum dwell-time) between each measurement, that ensures the estimation error of ∥<em>η</em>˜∥≤ 10 m. Hint: <em>η</em>˜˙ = <em>η</em>˙ − <em>η</em>ˆ<sup>˙ </sup>= <em>η</em>˙ − <em>η</em>˙<em><sub>m</sub></em>.

<ul>

 <li>(30 pts) Using the determined dwell-time from Part (1.a) to dictate when measurements of theposition are available <em>η<sub>m </sub></em>(i.e., only provide measurements <em>η<sub>m </sub></em>every ∆<em>t<sup>q </sup></em>but assume <em>η</em>˙<em><sub>m </sub></em>and <em>η</em>¨<em><sub>m </sub></em>are always available), let the estimated tracking error <em>e</em>ˆ and filtered tracking error <em>r</em>ˆ be defined as</li>

</ul>

<em>e</em>ˆ = <em>η<sub>d </sub></em>− <em>η</em>ˆ

<em>r</em>ˆ = <em>e</em>ˆ<sup>˙ </sup>+ <em>αe</em>ˆ

Design a controller that ensures the estimated tracking error and filtered tracking error are stable using Lyapunov-based methods (this could be adaptive, robust, or a mixture). Show all your work. Hint: <em>e</em>ˆ<sup>˙ </sup>= <em>η</em>˙<em><sub>d </sub></em>− <em>η</em>˙<em><sub>m</sub></em>, <em>e</em><sup>¨</sup>ˆ = <em>η</em>¨<em><sub>d </sub></em>− <em>η</em>¨<em><sub>m </sub></em>= <em>η</em>¨<em><sub>d </sub></em>− <em>η</em>¨(<em>t</em>) − <em>ω<sub>η</sub></em><sub>¨ </sub>(<em>t</em>).

1

<ul>

 <li>(40 pts) Simulate the above switched system for at least one complete circle, where <em>η</em>ˆ → <em>η<sub>m </sub></em>at each time <em>t<sup>q</sup><sub>j </sub></em>(remember, only provide measurements <em>η<sub>m </sub></em>every ∆<em>t<sup>q </sup></em>and reset the estimated position to the measured position but assume <em>η</em>˙<em><sub>m </sub></em>and <em>η</em>¨<em><sub>m </sub></em>are always available),m, <em>η</em>˙ (0) = 0<sub>2×1</sub>, and <em>η</em>¨(0) = 0<sub>2×1</sub>, and model all noise or disturbances as Gaussian distributions that remain within the bounds 99.7 percent of the time (i.e., 3 standard deviations are less than each bound for each model of noise or disturbance). Additionally, provide the following:</li>

</ul>

<ol>

 <li>Discuss the approach you took and why.</li>

 <li>Plot the norm of your position estimation errors over time.

  <ol>

   <li>Did the position error remain less than the upper limit?</li>

   <li>Did the position error ever get close to the upper limit?</li>

   <li>Based on A and B, was the dwell-time conservative?iii. Plot the norm of your estimated tracking errors over time and the norm of the true tracking error .</li>

   <li>Based on these plots, how well did the designed controller track the desired trajectory.</li>

  </ol></li>

 <li>If you did an adaptive approach, plot the norm of your parametric errors over time and discusswhether the parameters converged or how close they were to the true values.</li>

 <li>If you did an adaptive approach, plot the norm of the total input, the feedback portions ofthe input, and the feedforward portions of the input and discuss how the total input behaved over time (e.g., did the input rely on feedback the majority of the time or did the feedforward portion become the majority of the input over time).</li>

 <li>Based on the plots, use quantitative and qualitative descriptions of the plots and data tosupport you discussion of the following</li>

 <li>Briefly discuss whether your simulation matches your stability result and describe anything you think would improve the result.</li>

</ol>

2