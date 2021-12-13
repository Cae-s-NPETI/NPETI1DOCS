# NPETI1DOCS
Documentation for the **SledAway** infrastructure. **SledAway** is a simulated ride-sharing application made with emerging practices, e.g. microservices.

## Setup

There are two main repositories to clone, be sure to have these checked out.
- [backend](https://github.com/Cae-s-NPETI/backend)
- [frontend](https://github.com/Cae-s-NPETI/frontend)

Follow the individual set-up instructions given in the repositories.

## Documentation
![image](https://user-images.githubusercontent.com/93184095/145822603-973c6649-1f06-4cfe-ae06-ea56b9185abb.png)

### Domain analysis
Two main group of users:
- Passenger
- Driver

![image](https://user-images.githubusercontent.com/93184095/145822697-bcfce023-3876-4fc1-a60c-c887eabdf12a.png)

- The core of the application is centered around the assigning of drivers
- Passenger services, driver trip management are the main front for the teo main group of users. These are extensions of the core domain.
- User account management support the core domains

### Bounded context
![image](https://user-images.githubusercontent.com/93184095/145823663-74e18fa3-e330-470a-95a6-74527ce2c75e.png)

- These domains are split based on the primary purposes they serve, and entities related
- Minimise overlap

### Tactical DDD (Domain-Driven Design)
![image](https://user-images.githubusercontent.com/93184095/145824248-d6392346-7a9e-4a62-ada6-c7352dcfff1e.png) 

- A closer look into the relational entities involved in the system

### Identify microservices
![image](https://user-images.githubusercontent.com/93184095/145824741-6d2224b1-59a9-40d0-85b9-b950ef80cbda.png)

- Three main backend microservices, and a frontend that could be a microfrontend split into the two primary userbase
- Communication mostly by REST API
- Design in a way where interdependencies are kept minimal, e.g. one malfunctioning microservice would impact the whole application minimally

### Possible improvements
- Authentication / login service
- Central REST service (Anti-corruption layer)
- Ratelimits
- Use higher performing, fault tolerant interprocess communication (e.g. message queue)
![image](https://user-images.githubusercontent.com/93184095/145826144-c3c94c95-d7c2-4918-ba27-3f2e677ea970.png)

Note: These did not make it into the actual implementation as they are either out of scope or require more resources to implement (e.g. deployment of message queue server)



