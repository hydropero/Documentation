#### [Return to main Index page](https://github.com/hydropero/Terminology)

# AWS Networking Concepts


| Term     | Description |
| ----------- | ----------- |
|  **Main Routing Table**   | Default routing table that comes with your VPC (Controls routing for all subnets that are not explicitly associated with another route table)     |
|  **Custom Route Table**   | A *custom* route table you create for your VPC |
| **Destination** | A range/block of IP addresses where you want traffic to flow |
| **Target** | A gateway/network interface or connection through which to send the destination traffic? |
| **Route Table Association** | A route table association - the association between a route table and a:<ul><li>Subnet</li><li>Internet Gateway</li><li>Virtual Private Gateway</li>
</ul> **Subnet Route Table** | A route table that's associated with a subnet |
| **Local Route** | A default route for communication within the VPC |
| **Propagation** | if a vpg (virtual private gate) is attached to your VPC + route propagation is enabled - VPN connection routes are automatically added to your subnet route tables (no work required on your end) |

