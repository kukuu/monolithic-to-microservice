# Monolithic to microservice

Note any changes should not change the user experience. Just the architecture.

1. https://github.com/kukuu/AGILITY/blob/master/SOA-and-MicroServices.md 

2. https://github.com/kukuu/AGILITY/blob/master/difference-between-monolithic-and-microservices-architecture-1.png

## Strategy:

1. Define Business context

2. Security

3. Technology

4. Architecture

5. Configuration Management

6. Monitoring

7. Aggregating logs

8. Deployment

9. Documentation

## Implementation

1. In the conversion we use a dispatcher proxy to the monolithic (legacy system) to capture requests and direct it to the micro-service

ii. Use Apache config file to do re-write rule for the new  urls (end points) - Apache's re-write engine switched on. Each URL with a string in it will be re-written.


## Technology


A. Nodejs, NGINX, Containers

B. SCALA


1. Apache 

2. Container -  Make changes and see propagate through from 40 to 2 secs

3. Architecture: Contract betweeen

```
service => model => client

```
4. Other microservices uses the client (thin) and do not have to create any more underlining http requests. 

5. Other microservices will import the client

6. Each microservice can supply more than one client in different technologies (JAVA, SCALA, JS[Node JS]). You simply import the appropriate client

7. Create micro-service according to REST  Specification.

i. JSON as exchange format and

ii HTTP protocol

## Best Practices

### TOGAF

The Open Group Architecture Framework (TOGAF) is an enterprise architecture methodology that offers a high-level framework for enterprise software development. 


TOGAF helps organize the development process through a systematic approach aimed at reducing errors, maintaining timelines, staying on budget and aligning IT with business units to produce quality results.

Like other IT management frameworks, TOGAF helps businesses align IT goals with overall business goals, while helping to organize cross-departmental IT efforts. TOGAF helps businesses define and organize requirements before a project starts, keeping the process moving quickly with few errors.


The Open Group states that TOGAF is intended to:

Ensure everyone speaks the same language
Avoid lock-in to proprietary solutions by standardizing on open methods for enterprise architecture
Save time and money, and utilize resources more effectively
Achieve demonstrable ROI.

Different elements of TOGAF are:

BADT:

There are four architectural domains in TOGAF 9.1 that offer specializations for businesses.

i. Business architecture: includes information on business strategy, governance, organization and how to adapt any existing processes within the organization.

ii. Applications architecture: a blueprint for structuring and deploying application systems and in accordance with business goals, other organizational frameworks and all core business processes.


iii. Data architecture: defining the organization’s data storage, management and maintenance, including logical and physical data models.

iv. Technical architecture: also called technology architecture; it describes all necessary hardware, software and IT infrastructure involved in developing and deploying business applications.

### OWASP

The OWASP Top 10 list consists of the 10 most seen application vulnerabilities:

Injection.

Broken Authentication.

Broken Access control.

Sensitive data exposure.

XML External Entities (XXE)

Security misconfigurations.

Cross Site Scripting (XSS)

Insecure Deserialization.


### HTTP2 

Concurrent downloads streamlined within a single TCP connection

Enable browsers to fetch crucial assets of a web page first

Optimize and improve HTTP header compression

And integrating a feature known as 'Server Push' that allows the server to deliver crucial data before the browser asks for it.
