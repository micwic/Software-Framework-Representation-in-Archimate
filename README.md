# Software-Framework-Representation-in-Archimate
![image](https://github.com/user-attachments/assets/15599d49-1f4a-4120-984a-7b2b84aea5ba)

### 1. **Intent**
The primary goal of this modeling is to test ArchiMate as a standard for documenting a system in the context of a pre-project opportunity study and/or as reference documentation during or after project execution, including the deployment.

The model presented is intentionally detailed and designed as a single, multi-layered representation to identify the most relevant layers for documenting complex systems.
This exercise aims to validate ArchiMate’s flexibility and rigor in supporting a unique, non-redundant, and comprehensive standardized technical documentation process throughout the software lifecycle, from vision to build and run.

While this approach intentionally goes beyond the initial scope of ArchiMate, it demonstrates the potential to extend the standard's use to cover the entire lifecycle of a solution, from design through implementation, deployment, and operations. By doing so, it maintains strong connections and coherence with the original vision and intent that underpin the change project, ensuring continuity between the strategic objectives and the technical execution.

### 2. **General Overview**
This ArchiMate model is based on a representative case designed to illustrate the final state of the system, which serves as the reference documentation. It does not include the various phases of the project due to time constraints but focuses on delivering a consolidated detailed view of the architecture once the project is completed. The model highlights the most pertinent architectural layers to be used as reference documentation.

The issue that prompted the intention to carry out this modeling is the difficulty in clearly positioning the integration of standard market software frameworks within business applications between the application and technology layers.

The initial models placed the use of these frameworks in the technology layer. However, this led to inconsistencies when functionalities or data objects were directly used by application functions. It also became apparent that these uses pertained to software architecture during the build phase of the solution, whereas the key elements of the technology layer were more aligned with system architecture during deployment and operations.

The imagined case is deliberately simple in terms of the business requirements to be met. It involves the automatic execution of an application process/function from a scheduler integrated into an application. The application function extracts data from Process Mining and conducts an analysis to derive relevant indicators. The user can access these indicators in dashboards and lists to facilitate a process review session. It is driven by a single Business Requirement to illustrate the possible links with the motivations that led to this intention.

The main subject of the modeling is to position the use of standard software frameworks in the design and realization of business applications. This is why the application is a Spring Boot application that integrates Spring Quartz to provide scheduling functionality. 

The intention to generalize the use of standard software frameworks is made visible by the implementation of a principle of compliance with norms and standards in the model. The adoption of this principle is expected to reach a level of capability maturity. It is explicitly shown in the model (and is even more important in the EA repository).

Each element in the model has been individually documented, providing a detailed understanding of the components and their relationships within the system. The model is available in GitHub as an Archi project.

### 3. **Findings**

Standard frameworks integrated into business applications are clearly and definitively an integral part of the business application. Their functionality is directly associated with business concepts. It is sometimes/often useful, depending on the context, to represent them to understand how the business logic is implemented. How the standard software framework is serving (let Spring Data expose getter or setter of an application data object) or realizing (let Spring Data create an application data object by using factory class) them.

Standard frameworks are most often well-documented, so it is essential to refer to this documentation rather than reproduce it. It may be beneficial to enrich it with what is specific to the context, but only for the elements that are useful to represent in the models, such as functionalities related to specific business concepts they implement.

Just like business logic - which is also an integral part of business applications - their deployment and execution rely on elements from the technology layer.

To the question of whether ArchiMate is an effective notation standard for the development of pre-studies, the design phase, and later as support for reference documentation of a business application, the answer is definitely yes.

The modeling of the representative case demonstrated that : 
- an architecture following BDD/DDD principles was feasible and represented in a meaningful way (software design by business analyst(input), software designer/developer, technology leader).
- the integration of functionalities offered by standard frameworks was feasible and represented in a meaningful way (software architecture by software architect, technology leader).
- the representation of artifacts, configurations, and infrastructure resources from the technology layer could be linked to relevant elements in the application layer to ensure deployment, integration, and operation process definition by system architects.

Beyond ensuring coherence, multi-layer modeling provides comprehensive cross-layer visibility, which is critical for coordinating the various specialists involved, thereby ensuring project success. Note that with this modeling approach, specialists retain control over their respective layers, unlike an approach that models software frameworks within the technology layer.

ArchiMate goes further by also making explicit the principles of good practices such as DDD or BDD. The models created during the design phase will clearly show any potential deviations or violations of domain segregation, for example. That said, the models should not be redundant with the code and its documentation. The models should be limited to the overall design and refer to the living documentation produced from the code for implementation details in the software. The same applies to behaviors and data.

The principles of BDD and DDD have been chosen because they are intended to be representative of business architecture. They align with what ArchiMate recommends for modeling application behaviors. Software constructions based on other principles will require interrelations between the behavioral aspects, which remain the rule in ArchiMate, and the implementation according to the software architecture. These interrelations should be handle on a documentary level; they do not need to be modeled in ArchiMate.

Of course, the behaviors of the standard software frameworks are modeled only once for the relevant parts to be represented, and they are referenced as many times as necessary in their integration into business applications. Among other benefits, this also allows for measuring the level of adoption of the principle and assessing the impact of any potential changes or analyzing risks related to a failure.

The representation of the software and application architecture in a unique detailed model reveals a considerable number of elements and relationships. So much so that only an automated and dynamic representation sourced from the repository makes sense, except for limited use cases where it is necessary to express a specific problem within a defined scope. 

### 4. **Conclusion**

The use of frameworks at the application level was not anticipated during the development of the Archimate standard. They are often considered part of the technology layer. While this is appropriate for virtualization, application containers, and other facilities, it is not relevant for application frameworks like Spring Boot, Angular, or React, which organize and structure application code.

For this reason, the use of serving and realization relationships should be allowed between low-level abstraction elements of the framework that realize or support higher-level abstraction elements of the business application within the application layer. This principle should potentially be generalized across all layers.

Application, Domain and Infrastructure Layer are BDD/DDD terminilogy.
