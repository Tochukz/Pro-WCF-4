# Pro WCF 4
## Second Edition (2011)
#### Practical Microsoft SOA Implementation
__By Nishith Pathak__   
[Github Source Code](https://github.com/Apress/pro-wcf-4)   

## Chapter 1: WCF and SOA Basics
__Understanding SOA__  
A service _providers_ are components that execute some business logic based on predetermined inputs and outputs, and expose this functionality through an SOA implementation.   
A _consumer_, on the other hand, is a set of components interested in using one or more of the services offered by the provider.  
A _repository_ contains a description of the services, where the providers register their services and consumers find what services are provided.   

__What Is a Service__   
You should use services to represent the functions of the business and explicitly define the boundaries of what the business does, which essentially will define what the service can and cannot do.  
The term _loose coupling_ refers to situations in which any tow entities reduce the assumptions they make about each other when they try to exchange information.

#### Fundamental Tenets of Services
__Tenet 1: Boundaries Are Explicit__   
Some of the design principles to keep in mind for the first tenet are as follows:  
1. Know your boundaries
2. Services should be easy to consume  
3. Avoid remote procedure call (RPC) interfaces
4. Keep the service surface area small
5. Don't expose implementation details.  

__Tenet 2: Services Are Autonomous__   
Services need to be isolated and decoupled to accomplish the goal of making them autonomous.  
The design principles to keep in mind for the second tenet are as follows:  
1. Service versioning and deployment are independent of the system in which they are deployed.
2. Contracts, once published, should not be changes.
3. Adopt a pessimistic approach, and isolate services from failure.  

__Business Process Execution Language__  
Business Process Execution Language (BPEL) is a business process language that is based on XML and built using web service standards. You can use BPEL to define and manage a long-running business process.  
BPEL is an orchestration language and is used for abstracting the “collaboration and sequencing” logic from various web services into a formal process definition that is based on XML, Web Services Description Language (WSDL), and XML Schema. BPEL is also known as BPEL4WS or WSBPEL  

__Tenet 3: Services Share the Schema and Contract, Not the Class__    
Services interact using policies, schemas and behaviors instead of classes. The service contract should contain the message formats (defined using an XML schema, message exchange patters (MEPs, which are defined in WDSL), any WS-policy requirements, and any BPEL that may be required.
1. Service contracts constitute data, WSDL, and the policy do not change and remain stable.  
2. Contracts should be as explicit as possible   
3. If breaking service contract is inescapable, then version the services.  
4. Do not expose internal data representation publicly.

__Tenet 4: Service Compatibility Is Based on Policy__   
At times you will not be able to express a;; the requirements of service interaction via WSDL alone; this is when you can use policies. Policy expressions essentially separate the structural and semantic compatibilities.

#### A Brief History of the Microsoft Distributed Stack   
Microsoft developed the _Component Object Model (COM)_ to enable applications to interact with each other and to promote reusability. COM is a set of specifications that, when followed, allows software components to communicate with each other. COM was not designed to work ell with remote components.     
Microsoft developed the _Distributed Component Object Mode (DCOM)_, a proprietary wire protocol standard that extends COM, so it works in distributed environments.    
DCOM provides basic infrastructure support, such as reliability, security, location independence, and efficient communication between COM objects that reside across processes and machines.  
_.Net Remoting_

__Create a simple WCT service__  
You can create a WCF project using Visual studio's `WCF Service Library` project template .
If you do not see the WCF project template, you can install it as an _individual component_ using Visual Studio Installer.      
