# High Level Plan for the Developer Guide

## Scope
This document serves as a **suggested** high level plan for developing a **Native XRP Ledger Wallet**.

## Audience
- Developers
- Infrastructure Engineers

## Tools Required:
The tools required for setting up the developer workstation are <span style="color:red;">**COMING SOON**</span>

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
### Step 1: Start at the Apps & Services Level
To start creating the Native XRP Ledger Wallet, we will need to work at the Apps & Services level.

![](/XRP-Ledger-Wallet-Documentation/resources/visuals/application-level.png "Model/Class Creation Happens Here")


#### A wallet object should look like the following:
- Create a [Wallet](/XRP-Ledger-Wallet-Documentation/concepts/what-is-a-wallet.md) **model/class** in your project with the associated properties

![](/XRP-Ledger-Wallet-Documentation/resources/visuals/Software-Wallet-Object.png)

#### However, a wallet consists of other objects and methods (depicted below):
- The supporting objects and method functionality must also be created


![](/XRP-Ledger-Wallet-Documentation/resources/visuals/wallet-payment-updated.png)



### Step 2: Transition to the **Middleware APIs** Level
- Once all of our **models/classes** are created, we will need to perform the API Connections to accomplish this **Middleware APIs** Step


![](/XRP-Ledger-Wallet-Documentation/resources/visuals/middleware-api-level.png "Middleware API Connections Happens Here")

#### Important Notes:
- Each endpoint will need to be mapped to a service that corresponds to the Ripple API (i.e. send transactions, receive transactions) - which connects to the XRP Ledger
- The controller will need to pass the necessary headers to the XRP Ledger when trying to successfully connect to each endpoint of the Ripple API, so the right response can be returned
- This step will set up the endpoints that need to be in place

#### Sample Code:

```java
     import org.springframework.web.bind.annotation.GetMapping;
     import org.springframework.web.bind.annotation.RequestParam;
     import org.springframework.web.bind.annotation.RestController;

      @RestController
      @RequestMapping(/XRPWallet)
      public class XRPLedgerWallet {
	   
      //Controller
      public XRPLedgerWallet(@RequestParams...){
         //Include attributes/objects required for the wallet
      }
  
      @RequestMapping(/createAccount)
	       public void createAccount(@RequestParams...){
          /* - this method should provide the formatted payload that the Ripple API recognizes
             - once the payload is passed in the Ripple API will connect to the server and return the 
             corresponding response to this endpoint.
          */
  	}


      @RequestMapping(/createEscrow)
	       public void createEscrow(@RequestParams...){
          /* - this method should provide the formatted payload that the Ripple API recognizes
             - once the payload is passed in the Ripple API will connect to the server and return the 
             corresponding response to this endpoint.
          */
  	}

      @RequestMapping(/send)
      public void sendTransactions(@RequestParams...){
      /* - this method should provide the formatted payload that the Ripple API recognizes
      - once the payload is passed in the Ripple API will connect to the server and return the
      corresponding response to this endpoint.
      */
      }
  
      @RequestMapping(/receive)
      public void receiveTransactions(@RequestParams...){
      /* - this method should provide the formatted payload that the Ripple API recognizes
      - once the payload is passed in the Ripple API will connect to the server and return the
      corresponding response to this endpoint.
      */
      }
  }       
```



### Additional requirements:
#### Infrastructure
**[Please refer to the [XRP Ledger API Documentation](https://xrpl.org/get-started-with-the-rippled-api.html) to
familiarize yourself with [rippled](https://xrpl.org/the-rippled-server.html), **XRP Ledger's core server software**, along
with WebSocket API tools, public servers and more.]**

- Create environment specific configurations which includes:
  - port #s
  - server locations/hostnames
  - security connections/protocols, if required here
  - logger files to capture the behavior of the application
- Ensure the Security Protocols are properly enabled
  - 
#### Security
- the wallet may need a private key field as its primary identifier when interacting with the XRP Ledger, rather than a username/password combination
  **[Note: In order to be authorized to connect to the endpoints, a user would first need to create an account in order for a
  unique token/private key to be generated.]**



#### Resources
- Tech Stack Diagram Can be [here](https://xrpl.org/img/ecosystem.svg).
- Click [here](https://spring.io/guides/gs/rest-service/) for guidance on creating a RESTful Web Service in **Java**.
- Curious about any of the following? Click [here](https://xrpl.org/get-started-with-the-rippled-api.html).
  - sample payload
  - sample response
  - makeup of the objects that a wallet holds


















