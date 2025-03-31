<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-mechanics:actions)=
# Actions

<!--
**What's an action?** Newton conceives the concept of an action, including both forces and moments, as the **causes of changes of the true motion** of mechanical systems, or **causes of difference of true motion w.r.t. a [general relative motion](classical-mechanics:kinematics:relative)**.
-->

**What is an action?**[^action-def] Following the introduction of fundamental mechanics concepts in his *Principia Naturalis*, Newton conceived the concept of action—including both **forces** and **moments**—as the possible **causes of variation in the "true motion"** of a mechanical system or, equivalently, the causes of the **difference between true motion and a** [**generic relative motion**](classical-mechanics:kinematics:relative).

[^action-def]: The answer to the question "what is an action?" might imply a "true" knowledge—whatever that means—of the object-concept "action." Here too, as in other cases, the question "what is...?" can be replaced with "what do we mean by...?", and an "operational answer" can be considered satisfactory, as it reflects the mode of knowledge and formation of understanding in the scientific field: without delving into more abstract philosophical domains, in physics, we are content to define something through its interactions and effects on other systems, its properties, and a reliable process for its measurement.

```{prf:definition} "True motion"
:label: def:true-motion
Newton's concept of *true motion* is meant as the motion w.r.t. an inertial reference frame. So what is an [**inertial reference frame**](classical-mehcanics:dynamics:principles:inertial-ref-frame)? From an operational point of view, dynamometers measure no force and moment associated with uniform motion w.r.t. a inertial reference frame.
```

A force is a vectorial physical quantity that, from an operational point of view, can be measured with a **3-axis force sensor** (which measures its three components in a 3-dimensional space) or with a **dynamometer** (which measures its intensity), provided it is free to orient itself along the force direction or if the force direction is known and the instrument is aligned with it.

<!--
**Models.**
- Types of action:
  - concentrated force, moment of a force, force couples; equivalent loads
  - distributed actions: volume actions, and surface actions (stress and pressure)
- Work and power; conservative actions
- Examples:
  - gravitation: universal gravitation, near the Earth's surface; brief mention of distance interaction
  - elasticity
  - constraint reactions
  - contact: normal reaction and friction
  - brief mention of other actions (between electric charges, charges in EM fields,...; examples: levmag,...)
-->

```{prf:definition} True forces in classical mechanics
:label: def:true-forces

Referring to the [four fundamental interactions](physics:intro:current-status:fundamental-interactions), the significant interactions in the realm of classical mechanics are only those of [**gravitational**](classical-mechanics:actions:gravitation) and **electromagnetic** nature. Electromagnetic interactions can manifest with bodies having a net charge or, more frequently in classical mechanics, between bodies with no net charge. Among the latter cases, in classical mechanics, it is common to observe the macroscopic manifestation of the microscopic electromagnetic interaction between the elementary components of matter in the form of:
- [**contact**](classical-mechanics:actions:reactions:contact) interactions, where it is possible to distinguish:
   - a **normal** component to the contact surfaces responsible for the impenetrability of bodies,
   - and a tangential component to the surfaces that manifests as [**friction**](classical-mechanics:actions:reactions:contact:friction)
- material response to stresses, such as in the elastic constitutive law for [springs](classical-mechanics:actions:spring)
```

A measured action that is not a result of the fundamental interactions is due to non-inertial motion of the dynamometer - or, very unlikely, to a new interaction you've just discover. If you experience this situation, please remember to send me an invitation for the Nobel cerimony.

