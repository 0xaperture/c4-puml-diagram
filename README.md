# C4 Plant UML Diagram
Using the C4 model with PlantUML for threat modeling brings structure, clarity, and maintainability to security design work. Because C4 defines systems at four intentional levels—context, containers, components, and code—it naturally aligns threats to where they exist in the architecture, rather than forcing a diagram to represent too much at once.

PlantUML adds a “diagrams-as-code” approach, enabling version control, automated updates, and peer review just like application code. This makes models easier to evolve as architectures change, reduces stale documentation, and supports collaboration across engineering and security teams. The result is a more accurate, scalable, and traceable threat model that stays relevant throughout the system lifecycle.

C4 plant Unified Modeling Language (UML) for application visualizaton and threat-modeling.

### Context Template
A context diagram is the highest-level view in a system architecture. It shows your system as a single box and identifies the external actors, systems, and data flows that interact with it. The goal is to clearly define the system’s boundaries—what’s inside your responsibility and what isn’t—while illustrating how information moves in and out.

In threat modeling, this helps identify:
- Who or what can access the system
- Where trust boundaries exist
- Potential high-level attack surfaces (e.g., public APIs, external integrations)

[Context Diagram](c4DiagramTemplate_Context.puml)
![Context Diagram](./assets/c4DiagramTemplate_Context3.png)

### Container Template
A container diagram is the second level of the C4 model and breaks the system into its major building blocks—called containers. These aren’t physical shipping containers, but logical units such as web apps, APIs, mobile apps, databases, message queues, or background workers. The diagram shows how these containers communicate, the technologies they use, and how responsibilities are divided across the system.

In threat modeling, container diagrams are valuable because they clarify:
- Where data is stored, processed, and transmitted
- Internal trust boundaries between components
- Specific attack surfaces (e.g., service endpoints, admin consoles)
- Security controls that must apply per container or boundary

[Container Diagram](c4DiagramTemplate_Container.puml)
![Container Diagram](./assets/c4DiagramTemplate_Container.png)

### Component Template
A component diagram is the third level of the C4 model and dives deeper into a single container to show the major internal building blocks—components—that provide its functionality. Components typically represent logical groupings of functionality such as services, modules, controllers, repositories, or processors, rather than individual classes.

This diagram clarifies how responsibilities are organized inside a container, which components talk to each other, and how they depend on external systems or libraries.

For threat modeling, component diagrams help identify:
- Specific areas where sensitive logic or data resides
- Interfaces and internal APIs where unauthorized access could occur
- How security controls should be applied within the architecture
- Risk concentrations and potential lateral movement paths

### References
- Plant UML - https://github.com/plantuml-stdlib/C4-PlantUML
- C4 Diagram - https://c4model.com/
