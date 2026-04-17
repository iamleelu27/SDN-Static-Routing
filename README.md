Description

This project demonstrates static routing in a Software Defined Network using Mininet and a Ryu controller. The controller installs predefined flow rules in switches, ensuring packets follow a fixed path instead of dynamic learning.

Objective

To implement static routing by manually defining forwarding behavior through controller-installed OpenFlow rules.

Topology

h1 --- s1 --- s2 --- s3 --- h2

Features
Controller–switch interaction using OpenFlow
Static flow rule installation
Deterministic packet forwarding
No dynamic learning behavior
How to Run
Step 1: Start Ryu Controller

ryu-manager static_routing_controller.py

Step 2: Start Mininet

sudo mn --topo linear,3 --controller remote

Test Scenario
Allowed Communication

h1 ping h2

Result: Successful communication following predefined path.

Expected Output
Packets are forwarded only along the defined path
No flooding or dynamic routing occurs
Flow rules are installed by the controller
Validation
Communication remains consistent across multiple runs
Routing path does not change dynamically
Conclusion

Static routing was successfully implemented using controller-installed flow rules, ensuring predictable and controlled network behavior.
