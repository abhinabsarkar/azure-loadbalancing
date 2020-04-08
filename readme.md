# Azure Load Balancing options

| Features | Azure Front Door Service | Traffic Manager | Application Gateway | Azure Load Balancer |
| :------ | :------:                 | :------:        | :------:            | :------:            |
| Region    |   Global  | Global    |   Regional    |   Regional |
| OSI Layer |   Layer 7 |   Layer 4 |     Layer 7 |   Layer 4 |
| Traffic type |    HTTP(S) |   non -HTTP(S)    |    HTTP(S) |   non -HTTP(S)    |
| SSL Offloading |  Yes |   No  |   Yes | No    |

[**Front Door**](https://docs.microsoft.com/en-us/azure/frontdoor/front-door-overview) is an application delivery network that provides global load balancing and site acceleration service for web applications. It offers Layer 7 capabilities for your application like SSL offload, path-based routing, fast failover, caching, etc. to improve performance and high-availability of your applications.

[**Traffic Manager**](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-overview) is a DNS-based traffic load balancer that enables you to distribute traffic optimally to services across global Azure regions, while providing high availability and responsiveness. Because Traffic Manager is a DNS-based load-balancing service, it load balances only at the domain level. For that reason, it can't fail over as quickly as Front Door, because of common challenges around DNS caching and systems not honoring DNS TTLs.

[**Application Gateway**](https://docs.microsoft.com/en-us/azure/application-gateway/overview) provides application delivery controller (ADC) as a service, offering various Layer 7 load-balancing capabilities. Use it to optimize web farm productivity by offloading CPU-intensive SSL termination to the gateway.

[**Azure Load Balancer**](https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview) is a high-performance, low-latency Layer 4 load-balancing service (inbound and outbound) for all UDP and TCP protocols. It is built to handle millions of requests per second while ensuring your solution is highly available. Azure Load Balancer is zone-redundant, ensuring high availability across Availability Zones.

## Decision tree for load balancing in Azure

![Alt text](/images/load-balancing-decision-tree.jpg)