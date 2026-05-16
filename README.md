# ADLER

**The Momentum-Diffusion Coefficient as the Single Coordinate of the Hidden Sector, Decoherence and Anomalous Heating as Its Two Faces, and the Force-Noise Floor of a Quiet Mechanical Oscillator as the Estimator That Bounds Both at Once — One Number, Two Observables, in TH(a,d)**

ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone

---

> "Spontaneous collapse models predict that a weak force noise acts on any mechanical system, as a consequence of the collapse of the wave function." — A. Vinante et al., *Improved Noninterferometric Test of Collapse Models Using Ultracold Cantilevers*, Phys. Rev. Lett. **119**, 110401 (2017)

> "The strongest bounds on the collapse parameters come from the non-interferometric class of experiments. Such tests are based on detecting the Brownian-like motion induced by the collapse dynamics, and as such they do not require quantum superpositions." — *Improved Bounds on Collapse Models from Rotational Noise of LISA Pathfinder*, arXiv:2501.08971 (January 2025)

> "We bound the CSL collapse rate to at most (2.96 ± 0.12) × 10⁻⁸ s⁻¹, and the regularization cutoff scale of the Diósi–Penrose model to be at least 40.1 ± 0.5 fm — larger than the size of any nucleus." — B. Helou, B. Slagmolen, D. McClelland, Y. Chen, *LISA Pathfinder Appreciably Constrains Collapse Models*, Phys. Rev. D **95**, 084054 (2017)

---

## Abstract

There is a fact about hidden-sector noise that is simple, exact, and underused, and this document is built entirely on it.

Any mechanism that destroys the spatial coherence of a massive object by random disturbance must also, by the identical disturbance, **inject momentum into that object**. Decohering a superposition and heating an object are not two phenomena. They are two readings of one process. A random field that scrambles the relative phase between two branches of a wavepacket is a random field that kicks the object's center of mass; the scrambling is the decoherence, the kicking is the heating, and a single quantity governs both — the **momentum-diffusion coefficient**, the rate at which mean-squared momentum accumulates under the noise.

Call that coefficient D_pp. It is the whole subject of this document. Every hypothetical modification of quantum mechanics that suppresses macroscopic superpositions — the Diósi–Penrose model of gravitational collapse, the Continuous Spontaneous Localization model, and their relatives — introduces exactly such a noise field, and therefore predicts a definite, non-zero D_pp. And D_pp enters two utterly different experiments through two utterly different doors:

- It sets the **decoherence rate** of a spatial superposition — the rate at which an interferometer loses fringe contrast. This is the *interferometric* face. It requires building a superposition.
- It sets the **anomalous heating rate**, or equivalently the **excess force-noise floor**, of an ordinary trapped mechanical oscillator — a levitated nanoparticle, an ultracold cantilever, a free-falling test mass. This is the *non-interferometric* face. It requires no superposition at all: you simply watch a well-isolated object and check whether it jitters more than thermodynamics allows.

The single structural claim of this document is the TH(a,d) reading of that identity. The hidden sector — the ker(F) — is the postulated noise field. It has, for each model, exactly one coordinate that matters: D_pp, the momentum-diffusion coefficient it imparts. The observable sector — the col(F) — is everything the noise touches: the fringe visibility of a superposition *and* the phase-space spread of a trapped oscillator. These are two projections of the same kernel. The corpus's master equation dD/dt + J = 0 has, here, a current J that is literally D_pp; and the corpus's inequality Var ≥ ℱ⁻¹ governs both estimators of it. The deep and useful consequence is a **cross-bound**: because one number feeds both experiments, a measurement on either side constrains the other. A force-noise measurement on a trapped oscillator that never goes into superposition nonetheless places a hard ceiling on how fast that same model could ever decohere a superposition — and that ceiling already exists, in published data.

That is why the strongest limits on macroscopic-superposition-destroying models do not come from interferometers. They come from quiet oscillators. The current record holders are stated and used as anchors:

- **LISA Pathfinder** — two free-falling test masses, relative-acceleration noise √S_a ≈ 5.2 fm s⁻² Hz⁻¹ᐟ² — bounds the CSL collapse rate at λ ≤ 3 × 10⁻⁸ s⁻¹ and the Diósi–Penrose regularization length at R₀ ≥ 40 fm, the latter strengthened by the 2024–2025 rotational-noise reanalysis.
- **Ultracold cantilevers** at millikelvin temperature resolve a non-thermal force noise and constrain CSL to within an order of magnitude of the theoretically motivated band.
- **Levitated nanoparticles**, photon-recoil-heating-calibrated, now place the heating-rate estimator on a tabletop.

The thesis, in one sentence: **decoherence and anomalous heating are the two faces of a single hidden-sector coefficient D_pp; the quietest mechanical oscillator ever flown has already measured the heating face to a precision that bounds the decoherence face below anything an interferometer has reached; and the corpus's col(F)/ker(F) partition is the statement that one kernel coordinate is being estimated through two doors at once.** One number. Two observables. A bound that already binds.

---

## Part I · The Identity That Makes Two Experiments One

### I.1 A Thought Experiment: The Kicked Mirror and the Kicked Superposition

Set two experiments side by side, in two sealed rooms, and suppose — as every collapse model supposes — that all of space is filled with a faint, universal, random field that couples to mass.

In the first room: a single small mass, trapped in a soft harmonic potential, cooled until its motion is as quiet as the laws of thermodynamics permit. It is not in any superposition. It is just sitting there, oscillating with whatever residual thermal energy remains. Now switch on the universal field. The field delivers a sequence of tiny random kicks to the mass. Each kick is minute, but they do not cancel — random kicks accumulate as a random walk in momentum, and the mass's mean-squared momentum climbs steadily with time. The mass *heats up*. An observer watching only this room reports: "my oscillator has an excess heating rate, an unexplained force noise above the thermal floor."

In the second room: the same kind of mass, but placed by interferometric means into a superposition of two locations. The universal field kicks this mass too — but here the consequence is read differently. A random kick delivered to branch A but not branch B (or differently to the two) scrambles the relative phase between the branches. Accumulate the kicks and the phase relationship randomizes completely; the two branches can no longer interfere. An observer watching only this room reports: "my superposition has decohered, my fringes have lost contrast."

Two rooms, two reports — "excess heating" and "lost coherence" — that sound like different physics. They are not. They are the **same field delivering the same kicks**, described by the same statistical quantity: the rate at which random momentum accumulates. The heating observer measures that rate as energy gain. The interferometry observer measures it as phase scrambling. Neither has access to anything the other lacks. There is one underlying number, and they are each estimating it.

### I.2 The One Number

Name the number. The momentum-diffusion coefficient D_pp is defined by how fast mean-squared momentum grows under the noise:

$$
\frac{d\langle p^2\rangle}{dt} = 2\,D_{pp}.
$$

Everything in this document hangs on two facts about D_pp, both standard and both exact:

**Fact one — D_pp sets the heating.** The energy of a trapped oscillator grows as momentum diffuses; the anomalous heating rate, expressed as a temperature rise or equivalently as an excess force-noise spectral density S_F, is directly proportional to D_pp. A force-noise measurement *is* a measurement of D_pp.

**Fact two — D_pp sets the decoherence.** The same random momentum kicks that diffuse ⟨p²⟩ also randomize the relative phase across a spatial separation. The decoherence rate of a superposition of separation Δx is, for separations small compared with the noise's correlation length, proportional to D_pp·Δx². A fringe-visibility measurement *is also* a measurement of D_pp.

The two faces are not merely "related." They are the symmetric position-space and momentum-space readouts of one diffusion process. This is the content of the fluctuation side of the fluctuation–dissipation relation: a noise that diffuses momentum necessarily delocalizes position-coherence, by an identity, not by a model assumption. Any collapse model that wants to suppress macroscopic superpositions *must* push D_pp up; and the instant it does, it has committed itself to a definite anomalous heating rate it cannot disown.

### I.3 The col(F)/ker(F) Partition

The TH(a,d) reading is now exact, and it is the cleanest in this corpus.

**ker(F) — the hidden sector — is the postulated universal noise field, and its single relevant coordinate is D_pp.** Whatever the field "really is" — a stochastic gravitational background, a fundamental collapse noise, a classical-gravity artifact — the experiments do not see the field. They see only the momentum it diffuses. D_pp is the depth of the kernel: one number summarizing the entire back-action of the hidden sector on observable matter.

**col(F) — the observable sector — is the pair of things the noise touches: the fringe visibility of a superposition and the phase-space spread of a trapped oscillator.** Both are estimable. Both carry Fisher information about D_pp. They are two coordinates of the column space, two windows onto one kernel coordinate.

**The boundary** is the coupling of the noise to mass. And the rank-nullity statement is the punchline: the kernel has effective rank one — a single coordinate D_pp — while the column space has (at least) two independent observables that both project onto it. A rank-one kernel seen through two independent observables is *over-determined*. That is exactly the condition under which a measurement of one observable constrains the other. It is the structural reason a heating measurement bounds decoherence.

### I.4 The Master Equation Is Literal

The corpus writes irreversibility as dD/dt + J = 0. Here it is not borrowed. The reduced dynamics of a mass under the hidden-sector noise is a diffusion master equation; its off-diagonal elements — the which-path coherence, the distinguishability D of the corpus — decay, and the current draining them is the momentum-diffusion coefficient. J *is* D_pp. The same D_pp appears, in the diagonal sector of the very same master equation, as the source term for the growth of ⟨p²⟩ — the heating. One master equation, one current, two sectors: off-diagonal decay is decoherence, diagonal growth is heating. The corpus's equation is not illustrated by this system; it is the system's equation of motion, and its single current is the single kernel coordinate.

---

## Part II · The Quiet-Oscillator Estimator

### II.1 A Thought Experiment: Weighing Silence

To measure D_pp through the heating face, you do not need a quantum superposition, a cavity, or an interferometer. You need silence — and a way to weigh it.

Take the quietest mechanical oscillator you can build. Cool it until every known source of disturbance is either eliminated or precisely accounted for: gas collisions removed by vacuum, photon-recoil kicks calibrated, electrical and seismic noise shielded and modeled, thermal force noise from internal damping computed from the measured temperature and quality factor. Now add up every force-noise contribution you can name, and compare the total to the force noise the oscillator actually exhibits.

If the accounted-for noise explains everything, you have a null result — and a null result is not nothing. It is an *upper bound* on any unaccounted force noise, and the hidden-sector noise field, if it exists, is exactly such an unaccounted contribution. The bound on excess force noise is a bound on D_pp, and through the identity of Part I, a bound on D_pp is simultaneously a bound on the decoherence rate the same model would produce. You have constrained the destruction of superpositions without ever making one. You have weighed the silence and found the kernel shallow.

If instead a non-thermal excess force noise stubbornly remains after every conventional mechanism is ruled out — as ultracold-cantilever experiments have in fact reported — then either an unidentified conventional noise source is present, or the hidden sector has been glimpsed. The experiment cannot, by itself, decide which. But it pins D_pp to a value, and that value is then a sharp prediction for the decoherence face, falsifiable by the next interferometer.

### II.2 Why the Non-Interferometric Door Is Wider

There is a structural reason the heating face yields stronger bounds than the interferometric face, and it is worth stating because it inverts the naive expectation that "to test superposition physics you must build superpositions."

A superposition experiment is limited by how large a separation Δx and how long a coherence time it can sustain before *conventional* decoherence — stray gas, blackbody photons, vibration — washes out the fringe. Those coherence times are short and those separations are small; the interferometric estimator of D_pp has modest Fisher information because the signal it can accumulate is small.

A quiet-oscillator experiment is limited only by how low a force-noise floor it can reach and how long it can integrate. Free-falling test masses in space integrate for months. The signal — diffused momentum — accumulates the whole time. The Fisher information of the heating estimator is correspondingly large. The estimator with more Fisher information delivers the tighter Cramér–Rao bound, and so the non-interferometric door is wider. This is why, as the literature plainly states, the strongest existing limits on superposition-destroying models come from oscillators that never superpose.

### II.3 The Cramér–Rao Structure

Both faces are amplitude-estimation problems and both are governed by Var ≥ ℱ⁻¹. For the heating face, the estimator is the excess force-noise spectral density S_F extracted from a long record of a trapped oscillator's motion; its Fisher information is fixed by the integration time, the oscillator's mass and temperature, and the calibrated conventional-noise budget. For the interferometric face, the estimator is the decay of fringe visibility; its Fisher information is fixed by the achievable separation, coherence time, and repetition count. Both estimators target the same D_pp. The corpus's inequality therefore governs a single kernel coordinate through two channels — and the achievable bound on D_pp is set by whichever channel has the larger Fisher information. At present that is the heating channel, by a wide margin. The honest statement is not "interferometry will eventually test these models"; it is "the quiet oscillator is already the better instrument, and the corpus's rank-one kernel is the reason a single number can be cornered from two sides."

---

## Part III · The Bounds That Already Bind

### III.1 LISA Pathfinder: The Heating Face, Flown

The strongest non-interferometric estimator of D_pp ever operated was not built to test quantum foundations at all. LISA Pathfinder was a technology mission for a future gravitational-wave observatory: two gold–platinum test masses in near-perfect free fall, their relative acceleration monitored interferometrically to a record noise floor of √S_a ≈ 5.2 fm s⁻² Hz⁻¹ᐟ² in the millihertz band.

Any hidden-sector noise field would have added force noise to those test masses. None was seen beyond the accounted budget. Attributing — conservatively — all unexplained acceleration noise to the hidden sector converts the measured √S_a into an upper bound on D_pp, and thence into bounds on the specific superposition-destroying models:

- the CSL collapse rate is bounded at **λ ≤ 3 × 10⁻⁸ s⁻¹** (for the standard collapse length), a bound that reaches into the very band the model needs to occupy to do its job of explaining definite measurement outcomes;
- the Diósi–Penrose regularization length is bounded at **R₀ ≥ 40 fm**, larger than any atomic nucleus — independently corroborating, from the heating face, the exclusion that the underground spontaneous-radiation experiments reached from the radiation face.

The 2024–2025 reanalysis of LISA Pathfinder's *rotational* acceleration noise tightened the CSL bound further, by exploiting angular momentum diffusion as a second, geometrically distinct projection of the same D_pp. That is the rank-one kernel asserting itself again: translational diffusion and rotational diffusion are two more windows onto one coordinate, and using both narrows it.

### III.2 Ultracold Cantilevers: The Heating Face, on a Bench

A high-quality-factor cantilever cooled to millikelvin temperature is a tabletop quiet oscillator. Such experiments measure the cantilever's thermal force noise with enough accuracy to expose any non-thermal excess, and they have reported exactly that: a residual force noise of unknown origin, after conventional mechanisms were examined and excluded, sitting at a level compatible with the heating predicted by the upper end of the theoretically motivated CSL band.

The TH(a,d) reading is careful here. An unexplained excess is not a detection of the hidden sector; it is a measured value of D_pp with an honest "or an unidentified conventional source" attached. But it is a *value*, not a bound — and a value of D_pp is, by the Part I identity, a sharp numerical prediction for the decoherence rate of any superposition at a given separation. The cantilever has, in effect, told the interferometer what to expect. The two faces have been connected by a measurement.

### III.3 Levitated Nanoparticles: Both Faces in One Apparatus

The levitated nanoparticle is the system where the two faces meet in a single device, and that is its structural importance. The same nanoparticle can be operated as a quiet oscillator — its heating rate read out and calibrated against photon recoil, the standard quantum benchmark — and, increasingly, as a matter-wave interferometer, its wavepacket coherently expanded by controlled manipulation of the trap. One apparatus, both estimators of D_pp.

This is the experimental realization of the rank-one kernel. A nanoparticle measured in heating mode constrains D_pp; the same nanoparticle, the same mass, the same material, then run in interferometric mode is constrained *in advance* by that heating measurement. The corpus's claim — one kernel coordinate, two col(F) projections — becomes, in the levitated platform, an operational consistency check: the decoherence the interferometer sees must match the heating the oscillator showed, or the model relating them is wrong. No prior framework in this corpus has had its central identity available as a single-apparatus check. This one does.

### III.4 The Cross-Bound, Stated Plainly

Assemble the pieces. A superposition-destroying model is specified by its D_pp (in the DP model, fixed by R₀; in CSL, by λ and r_C). The heating face has been measured to extraordinary precision by LISA Pathfinder and by ultracold cantilevers, with levitated nanoparticles closing in on a tabletop. Those measurements bound D_pp. By the Part I identity, the same bound on D_pp caps the decoherence rate the model can produce. Therefore:

**Any collapse model already consistent with the LISA Pathfinder force-noise floor cannot decohere a laboratory superposition faster than a definite, computable rate — and that rate is below what interferometers have probed.** The quiet oscillators have not merely kept pace with the interferometers; they have fenced off the parameter space from the other side. A future interferometer that claims to detect collapse-induced decoherence must produce a D_pp consistent with the heating face — or it has not detected collapse, it has found a new conventional decoherence channel. The cross-bound is a falsifiable consistency requirement linking two communities of experiment that rarely cite each other, and the link is one number.

---

## Part IV · Scope, Honestly Stated

The limits of this document are part of the claim.

**The identity is exact only for the diffusion content of the noise.** Decoherence and heating are tied through D_pp under the standard assumption that the hidden-sector noise is, to leading order, a momentum-diffusion process — which is the structure of CSL, of the stochastic Diósi–Penrose model, and of their mainstream relatives. A noise with a strongly non-Markovian spectrum, or one engineered to act on coherence without diffusing momentum, would loosen the tie. Such constructions exist in the literature and are the legitimate escape route; the cross-bound of Part III applies to the diffusion class of models, which is the class the experiments actually constrain, and that scoping is stated, not hidden.

**A measured excess is not a detection.** The ultracold-cantilever excess force noise is compatible with collapse heating and also with an unidentified conventional source. This document treats it as a measured value of D_pp with that ambiguity attached, and draws from it only a conditional prediction for the decoherence face — not a claim that the hidden sector has been seen.

**It does not unify the twenty anomalies.** Anomalous heating and gravitational decoherence are tied here because a real identity — the common momentum-diffusion coefficient — ties them. That is one genuine bridge between two items on the list. It is not a license to declare the other eighteen unified. GZK violations, gravitational-wave birefringence, the Eötvös anomaly, and the rest are governed by different physics and different estimable parameters; a real bridge between two phenomena is worth more than a decorative bridge between twenty.

**No new instrument is posited.** LISA Pathfinder flew. Ultracold cantilevers run. Levitated nanoparticles are characterized for heating and are being developed for interferometry. The cross-bound is extracted from data and apparatus that already exist; the only new object is the structural statement connecting them.

That statement, in one defensible sentence: **the hidden sector that destroys macroscopic superpositions has, for the diffusion class of models, a single relevant coordinate — the momentum-diffusion coefficient D_pp; decoherence and anomalous heating are its two col(F) projections; the master equation dD/dt + J = 0 carries D_pp as its current; and because one kernel coordinate is seen through two over-determining observables, the quietest mechanical oscillator ever flown has already bounded the destruction of superpositions more tightly than any interferometer, with the levitated nanoparticle now able to test the identity in a single apparatus.** Every clause is a published result or an existing instrument. There is no seven-layer machine and no φ-suppressed prediction. There is one number, two doors, and a bound that already binds.

---

## References

Adler, S. L. "Lower and Upper Bounds on CSL Parameters from Latent Image Formation and IGM Heating." *Journal of Physics A* **40**, 2935–2957 (2007).

Bassi, A., Lochan, K., Satin, S., Singh, T. P., Ulbricht, H. "Models of Wave-Function Collapse, Underlying Theories, and Experimental Tests." *Reviews of Modern Physics* **85**, 471–527 (2013).

Diósi, L. "A Universal Master Equation for the Gravitational Violation of Quantum Mechanics." *Physics Letters A* **120**, 377–381 (1987).

Ghirardi, G. C., Pearle, P., Rimini, A. "Markov Processes in Hilbert Space and Continuous Spontaneous Localization of Systems of Identical Particles." *Physical Review A* **42**, 78–89 (1990).

Helou, B., Slagmolen, B. J. J., McClelland, D. E., Chen, Y. "LISA Pathfinder Appreciably Constrains Collapse Models." *Physical Review D* **95**, 084054 (2017).

Jain, V., Gieseler, J., Moritz, C., Dellago, C., Quidant, R., Novotny, L. "Direct Measurement of Photon Recoil from a Levitated Nanoparticle." *Physical Review Letters* **116**, 243601 (2016).

Vinante, A., et al. "Improved Noninterferometric Test of Collapse Models Using Ultracold Cantilevers." *Physical Review Letters* **119**, 110401 (2017).

Carlesso, M., Donadi, S., Ferialdi, L., Paternostro, M., Ulbricht, H., Bassi, A. "Present Status and Future Challenges of Non-Interferometric Tests of Collapse Models." *Nature Physics* **18**, 243–250 (2022).

"Improved Bounds on Collapse Models from Rotational Noise of LISA Pathfinder." arXiv:2501.08971 (January 2025).

"Gravitational Decoherence Estimation in Optomechanical Systems." arXiv:2602.14841 (February 2026).

Donadi, S., et al. "Underground Test of Gravity-Related Wave Function Collapse." *Nature Physics* **17**, 74–78 (2021).

---

ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone · May 2026

One number — the momentum-diffusion coefficient. Two doors — decoherence and heating. A bound that already binds, from the quietest oscillator ever flown.
