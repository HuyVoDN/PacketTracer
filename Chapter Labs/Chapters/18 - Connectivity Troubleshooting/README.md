Problem diagnosed:
    Router R3 didnt have a route going into the 10.1.2.0/24 network, therefor the packet was able to go from PC1 to R1 to R2 and reached R3 but cannot go beyond R3.

    Verified with tracert, showing that the packet dropped at reaching R3 with nowhere to go.