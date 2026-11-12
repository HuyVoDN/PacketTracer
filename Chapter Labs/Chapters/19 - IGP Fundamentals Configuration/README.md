Notes:

- Default static route means gateway of last resort
    - (config)# ip route 0.0.0.0 0.0.0.0 <next_hop_address>

- Injecting default route to all routers within RIP
    - (config)# router rip
    - (config)# default-information originate

- Check for EIGRP adjacent neighbors within a router
    - Router_Name# show ip eigrp neighbors