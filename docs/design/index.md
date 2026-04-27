# Design Considerations
<div style= "text-align: justify"> 
The design of the hotswap system was guided by a combination of electrical and mechanical constraints. The goal was to develop a solution that is not only functionally reliable, but also reproducible and accessible. In addition to the hotswap mechanism itself, the supporting charging infrastructure was designed as an integrated module, ensuring safe energy delivery, efficient thermal management, and ease of maintenance, you can better follow the decisions that molded this project in the text bellow.



## Component Accessibility and Cost Efficiency

A central design principle was the use of widely available, low-cost components. The adoption of the NBR 14136 connector (20 A rating) reflects this approach, as it is commonly found in the Brazilian market and does not require specialized procurement channels. This choice reduces the overall system cost and simplifies maintenance, as replacement parts can be easily sourced. Additionally, the system can be easily adapted to support other types of connectors or power outlets. Furthermore, the use of 3D printing for structural components allows for rapid replacement and customization without significantly increasing production costs. This approach also enables iterative improvements to the design.

This philosophy extends to the charger module, which integrates four NBR 14136 20A sockets into a single enclosure, allowing multiple batteries to be charged using a shared infrastructure. The use of a commercially available 42V switched-mode power supply further reduces cost and complexity, avoiding the need for custom power electronics design.


<figure style="text-align: center;">
  <img src="../_static/design_img/NBR_support.png" width="400">
  <figcaption><i>In our system, we use this piece to support the NBR 14136 after the modifications that will be later explained.</i> </figcaption>
</figure>


## Electrical Reliability

The system was designed to ensure stable electrical contact under dynamic operating conditions. The selected connector provides sufficient current capacity for high power requirements, while also offering robust physical contacts. The integration of XT30 connectors between the battery and the main connector improves modularity and facilitates safe handling during battery replacement. Furthermore, the use of fork (spade) terminals ensures secure and maintainable connections at the interface with the NBR connector. Care was taken to minimize contact resistance and avoid intermittent connections, which could compromise system performance or damage electronic components.

Within the charging module, electrical reliability is reinforced through the use of custom PCBs designed to handle currents up to 10A, with appropriately dimensioned traces. A voltage and current sensing system is also integrated, enabling real-time monitoring of charging conditions.


## Mechanical Guidance and Error Prevention

A key challenge in hotswap systems is preventing incorrect insertion, which may lead to short circuits or mechanical damage. To address this, the design incorporates guiding rails that constrain the motion of the battery drawer, allowing insertion only along a predefined path. These rails act as a passive alignment mechanism, ensuring that the electrical contacts engage properly. This reduces user error and eliminates the need for complex active alignment systems.

In addition to the guiding rails, the connector is intentionally positioned off-center within the enclosure. This asymmetry introduces a geometric constraint that further prevents incorrect insertion. Even in the unlikely event that the guiding rails are bypassed or worn, the off-centered configuration reduces the probability of improper mating between connectors, enhancing overall system safety.

This design philosophy is also reflected in the charger enclosure, where internal supports ensure correct positioning of batteries and connectors, minimizing the risk of user error during insertion and removal.

<figure style="text-align: center;">
  <img src="../_static/design_img/align_rail_view.png" width="400">
  <figcaption><i>Better view of the assymetric alignment rail.</i></figcaption>
</figure>


## Passive Retention and Dynamic Stability

The system must remain mechanically stable during machine operation, particularly under acceleration and vibration. Instead of relying on locking mechanisms, the design employs a passive retention strategy.

A slight inclination of 5° is introduced between the battery drawer and the socket base. This inclination resolves the force into components, reducing the portion that acts to disengage the battery from the connector. This effect, together with other friction-enhancing mechanisms, counteracts inertial forces that could otherwise cause disconnection. At the same time, the absence of active locks allows for quick battery replacement, which is essential for practical usability.

Additionally, the charger module enclosure was mechanically reinforced and modified to support continuous operation. Structural adaptations to the external toolbox include internal partitions for component fixation and airflow channels, ensuring that vibrations or movement do not compromise internal connections or component stability.

## Modularity and Maintainability

The design emphasizes modularity, allowing individual components (such as connectors, wiring, or printed parts) to be replaced independently. This reduces maintenance complexity and increases the system’s lifespan. The separation between components also enables easier diagnostics in case of failure.


<figure style="text-align: center;">
  <img src="../_static/design_img/hotswap_exploded.png" width="400">
  <figcaption><i>Hotswap exploded for better view of the project modularity.</i> </figcaption>
</figure>

</div>