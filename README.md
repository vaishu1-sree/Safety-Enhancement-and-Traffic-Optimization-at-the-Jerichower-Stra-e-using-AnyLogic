##  Safety Enhancement and Traffic Optimization at the Jerichower Street using AnyLogic


The traffic simulation model of the intersection at Jerichower Straße and Herrenkrugstraße in Magdeburg was created using AnyLogic simulation software. The goal of the simulation is to assess and improve traffic safety at this intersection by analyzing vehicle movements, traffic flows, and potential accident scenarios. AnyLogic software was used to model and run the simulation. To spawn cars in the conceptual model, the AnyLogic traffic library provides car sources that can be customized to reflect the calculated distributions. The library’s robust tools facilitate accurate modeling of traffic patterns and behaviors.

The simulation utilizes the Select Output pallet tool to route vehicles based on predefined probabilities, ensuring realistic traffic flow scenarios. The main streets were marked accordingly, and traffic rules were seamlessly implemented by configuring the crossroad section from the library. An initial speed limit of 10 km/h and a preferred speed limit of 55 km/h were set for all lanes, simulating realistic driver behavior, where drivers tend to exceed the allowed speed limit slightly, thus improving the quality of safety analysis.

For each incoming lane, a CarSource was implemented with the calculated inter-arrival time, accurately reflecting traffic volumes entering the intersection from various directions. Destinations within the simulation were defined using CarMoveTo blocks, allowing vehicles to follow turning and routing behaviors based on probabilities. The simulation also tracks the time vehicles spend driving below 0.1 m/s to calculate waiting times, as even at this minimal speed, cars are still considered in motion, enhancing accuracy. A car-count mechanism was implemented to measure the throughput of the intersection, providing valuable insights into traffic flow and identifying potential bottlenecks.

Bicyclists and pedestrians were also incorporated into the simulation to model their interactions with vehicular traffic. Cyclists were modeled as cars, allowing "real" cars to avoid collisions with them, while activating the yield property at stop lines before cyclist crossings enabled the simulation of vehicles yielding to cyclists appropriately. The model also includes traffic lights, configured with real-time data to reflect actual signal timings at the intersection. These traffic lights regulate the flow of vehicles, bicycles, and pedestrians, ensuring the simulation accurately represents real-world traffic conditions. The integration of real-time data allows for an assessment of the current traffic light timings and explores potential optimizations to reduce waiting times and improve traffic flow.

While trams were not involved in accidents, they were represented in the simulation through traffic light timings. To simulate potential accidents, a proxy was implemented, as AnyLogic itself does not have built-in accident modeling capabilities. Lane-switching accidents are triggered when the deceleration exceeds 98% of the maximum deceleration and the car is changing lanes, while car-bike accidents are considered to occur when deceleration reaches 75% of the maximum, and the car in front is a cyclist. These proxies were developed through experimentation to strike a balance between simulating too many or too few accidents, providing a realistic representation of accident scenarios.
