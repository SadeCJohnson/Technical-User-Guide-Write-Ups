# High Level Plan for the Developer Guide

## Scope
This document serves as a **suggested** high level plan for developing a **Native XRP Ledger Wallet**.

## Audience
- Developers
- Infrastructure Engineers

## Tools Required:
The tools required for setting up the developer workstation is <span style="color:red;">**COMING SOON**</span>

## Ripple's Software EcoSystem Tech Stack Representation:


![alt text](/XRP-Ledger-Wallet-Documentation/resources/visuals/xrp-tech-stack-level.png)

#### What does the above photo mean?
**Here's one Translation:**
- There are **applications/services** created 
- These **applications/services** are configured to interact with **Middleware APIs** 
- The **Middleware APIs** are configured to interact with the **Ripple API** (which works with Programming Libraries)
- The **Ripple API** then makes the connections to the **XRP Ledger**, which interacts with the **servers**
- The **servers** are where data is being **sent** and/or **retrieved**



## Suggested High Level Integration Steps:

**To start creating the Native XRP Ledger Wallet, we will need to work at the Apps & Services level.**

![](/XRP-Ledger-Wallet-Documentation/resources/visuals/application-level.png "Model/Class Creation Happens Here")

    
#### A simple wallet object should look like the following:
- Create a [Wallet](/XRP-Ledger-Wallet-Documentation/concepts/what-is-a-wallet.md) **model/class** in your project with the associated properties

![](/XRP-Ledger-Wallet-Documentation/resources/visuals/Software-Wallet-Object.png)

#### However, a wallet consists of other objects (depicted below):
- Therefore, the supporting objects must also be created

![](/XRP-Ledger-Wallet-Documentation/resources/visuals/wallet-payment-updated.png)


####  Once all of our **models/classes** are created, we will need to perform the API Connections to accomplish this **Middleware APIs** Step
    - This step will set-up the endpoints that need to be in place
    - Each endpoint will need to be mapped to a service that corresponds to the XRP Ledger's functionality (i.e. send transactions, receive transactions)
    - The controller will need to pass the necessary headers to the XRP Ledger when trying to successfully connect to each endpoint

![](/XRP-Ledger-Wallet-Documentation/resources/visuals/middleware-api-level.png "Middleware API Connections Happens Here")
**[Please refer to the [XRP Ledger API Documentation](https://xrpl.org/get-started-with-the-rippled-api.html) to
familiarize yourself with [rippled](https://xrpl.org/the-rippled-server.html), **XRP Ledger's core server software**, along
with WebSocket API tools, public servers and more.]**
   
   **[Note: In order to be authorized to connect to the endpoints, a user would first need to create an account in order for a 
    unique token/private key to be generated.]** 

- An intermediary class will need to be created to implement the function logic since that info may be abstracted from the controller
  
  **[Provide a Visual example]**
- these functions should perform the necessary actions required to allow for the interaction between the Wallet and the XRP Ledger.

### Other requirements:
#### Infrastructure
- Create environment specific configurations which includes:
  - port #s
  - server locations/hostnames
  - security connections/protocols, if required here
  - logger files to capture the behavior of the application
- Ensure the Security Protocols are properly enabled  

#### Security 
- the wallet may need a private key field as its primary identifier when interacting with the XRP Ledger, rather than a username/password combination



#### Resources
- Tech Stack Diagram Can be [here](https://xrpl.org/img/ecosystem.svg).


















