# Design Considerations
<div style= "text-align: justify"> 
The design of the hotswap system for the M.I.C.K.Y. robot was guided by a combination of electrical and mechanical constraints. The goal was to develop a solution that is not only functionally reliable, but also reproducible and accessible, you can better follow the decisions that molded this project in the text bellow.
</div>


## Component Accessibility and Cost Efficiency

<div style= "text-align: justify">
A central design principle was the use of widely available, low-cost components. The adoption of the NBR 14136 connector (20 A rating) reflects this approach, as it is commonly found in the Brazilian market and does not require specialized procurement channels. This choice reduces the overall system cost and simplifies maintenance, as replacement parts can be easily sourced. Additionally, the system can be easily adapted to support other types of connectors or power outlets. Furthermore, the use of 3D printing for structural components allows for rapid replacement and customization without significantly increasing production costs. This approach also enables iterative improvements to the design.
</div>


<figure style="text-align: center;">
  <img src="../_static/design_img/NBR_support.png" width="400">
  <figcaption><i>In our system, we use this piece to support the NBR 14136 after the modifications that will be later explained.</i> </figcaption>
</figure>


## Electrical Reliability

<div style= "text-align: justify"> 
The system was designed to ensure stable electrical contact under dynamic operating conditions. The selected connector provides sufficient current capacity for the robot’s power requirements, while also offering robust physical contacts. The integration of XT30 connectors between the battery and the main connector improves modularity and facilitates safe handling during battery replacement. Furthermore, the use of fork (spade) terminals ensures secure and maintainable connections at the interface with the NBR connector. Care was taken to minimize contact resistance and avoid intermittent connections, which could compromise system performance or damage electronic components.
</div>


## Mechanical Guidance and Error Prevention

<div style= "text-align: justify"> 
A key challenge in hotswap systems is preventing incorrect insertion, which may lead to short circuits or mechanical damage. To address this, the design incorporates guiding rails that constrain the motion of the battery drawer, allowing insertion only along a predefined path. These rails act as a passive alignment mechanism, ensuring that the electrical contacts engage properly. This reduces user error and eliminates the need for complex active alignment systems.

In addition to the guiding rails, the connector is intentionally positioned off-center within the enclosure. This asymmetry introduces a geometric constraint that further prevents incorrect insertion. Even in the unlikely event that the guiding rails are bypassed or worn, the off-centered configuration reduces the probability of improper mating between connectors, enhancing overall system safety.
</div>


<figure style="text-align: center;">
  <img src="../_static/design_img/align_rail_view.png" width="400">
  <figcaption><i>Better view of the assymetric alignment rail.</i></figcaption>
</figure>


## Passive Retention and Dynamic Stability

<div style= "text-align: justify"> 
The system must remain mechanically stable during robot operation, particularly under acceleration and vibration. Instead of relying on locking mechanisms, the design employs a passive retention strategy.

A slight inclination of 5° is introduced between the battery drawer and the socket base. This inclination resolves the force into components, reducing the portion that acts to disengage the battery from the connector. This effect, together with other friction-enhancing mechanisms, counteracts inertial forces that could otherwise cause disconnection. At the same time, the absence of active locks allows for quick battery replacement, which is essential for practical usability.
</div>


## Modularity and Maintainability

<div style= "text-align: justify"> 
The design emphasizes modularity, allowing individual components (such as connectors, wiring, or printed parts) to be replaced independently. This reduces maintenance complexity and increases the system’s lifespan. The separation between components also enables easier diagnostics in case of failure.
</div>


<figure style="text-align: center;">
  <img src="../_static/design_img/hotswap_exploded.png" width="400">
  <figcaption><i>Hotswap exploded for better view of the project modularity.</i> </figcaption>
</figure>
