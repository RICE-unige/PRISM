# PRISM- Personality Research in Synthetic Minds


## PRISM Cognitive Architecture

![Architecture](images/PRISM_Architecture.png)

PRISM is a modular Cognitive Architecture designed to implement robotic personality in various agents.

### CEA Taxonomy

Personality is defined as a vector in a three-dimensional space defined by Conscientiousness, Extraversion, and Agreeableness (CEA), allowing the generation of infinite three dimentional personality profiles.  

$$
Personality= W_{c}C +  W_{e}E +  W_{a}A  (1)
$$

where \(C\), \(E\), and \(A\) are the unit vectors of the three axes, and \(W_{c}\), \(W_{e}\), and \(W_{a}\) represent the degree to which each trait is expressed, ranging from \([-1 (low), +1 (high)]\) with \(0\) indicating neutrality.

### Personality Generator

To model how personality influences action execution, we integrated language generation techniques into the Personality Generator, leveraging the BERT attention-based architecture. The personality model takes a defined personality (Equation 1) and a general action (e.g. speak about music, go near the person, pick the bottle.. ) as input, generating parameters that shape the action according to personality traits. These parameters include voice pitch, velocity, volume, language style, gaze behavior, gesture speed and amplitude, head movements, navigation speed, and proxemics. Here the set of parameters associated with the CEA traits.


**E**, **A**, **C** refer to personality traits (Extraversion, Agreeableness, Conscientiousness). **H** and **L** mean high and low values of the trait, respectively (e.g., **HE** = extraverted, **LE** = introverted).

| **Trait**                                       | **HE**                                                 | **LE**                      | **HC**                 | **LC**                                       | **HA**                                                             | **LA**                                                 |
| ----------------------------------------------- | ------------------------------------------------------ | --------------------------- | ---------------------- | -------------------------------------------- | ------------------------------------------------------------------ | ------------------------------------------------------ |
| **Language**<br>\[Andriella+2022, Garello+2020] | Verbose, Friendly, Talkative,<br>Enthusiastic, Excited | Reserved, Quiet,<br>Neutral | Scrupulous,<br>Precise | Thoughtless, Distracted,<br>Lazy, Disordered | Cooperative, Friendly,<br>Empathic, Forgiving,<br>Reliable, Polite | Competitive, Aggressive,<br>Provocative, Selfish, Rude |
| **Pitch**<br>\[Polzehl+2015]                    | High                                                   | Middle                      | Middle                 | Low                                          | Low                                                                | Middle                                                 |
| **Volume**<br>\[Polzehl+2015]                   | Very dynamic                                           | Middle                      | Middle                 | Low                                          | Dynamic                                                            | Dynamic                                                |
| **Velocity**<br>\[Polzehl+2015]                 | High                                                   | Middle                      | Low                    | Rather high                                  | Middle                                                             | Rather high                                            |
| **Gaze**<br>\[Luo+2022]                         | Mutual                                                 | Avoid                       | No active              | No active                                    | Mutual                                                             | Avoid                                                  |
| **Head Movements**<br>\[Madan+2023]             | Shaking                                                | Little shaking              | Tilt up shaking        | Tilt down shaking                            | Nodding                                                            | Little shaking                                         |
| **Gesture Amplitude**<br>\[Craenen+2018a,b]     | High                                                   | Low                         | Middle                 | Middle                                       | Middle                                                             | Middle                                                 |
| **Gesture Speed**<br>\[Craenen+2018a,b]         | High                                                   | Low                         | Middle                 | Middle                                       | Middle                                                             | Middle                                                 |
| **Navigation Speed**<br>\[Takayama+2009]        | High                                                   | Low                         | Middle                 | Middle                                       | Middle                                                             | Middle                                                 |
| **Proxemic**<br>\[Ritschel+2022]                | Near                                                   | Far                         | Middle                 | Middle                                       | Near                                                               | Far                                                    |



