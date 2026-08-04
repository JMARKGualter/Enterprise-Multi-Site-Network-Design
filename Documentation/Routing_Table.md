# Routing Table

## HQ Router

| Destination Network | Next Hop | Purpose |
|---------------------|----------|---------|
| 0.0.0.0/0 | 10.0.12.2 | Default route to ISP |
| 200.1.1.0/24 | 10.0.12.2 | Internet Network |
| 192.168.110.0/24 | 10.0.13.2 | Batangas IT |
| 192.168.120.0/24 | 10.0.13.2 | Batangas HR |
| 192.168.130.0/24 | 10.0.13.2 | Batangas Finance |
| 192.168.140.0/24 | 10.0.13.2 | Batangas Sales |
| 192.168.210.0/24 | 10.0.14.2 | Cebu IT |
| 192.168.220.0/24 | 10.0.14.2 | Cebu HR |
| 192.168.230.0/24 | 10.0.14.2 | Cebu Finance |
| 192.168.240.0/24 | 10.0.14.2 | Cebu Sales |




## Batangas Router

| Destination Network | Next Hop | Purpose |
|---------------------|----------|---------|
| 0.0.0.0/0 | 10.0.13.1 | Default route to HQ |



## Cebu Router

| Destination Network | Next Hop | Purpose |
|---------------------|----------|---------|
| 192.168.0.0/16 | 10.0.14.1 | Reach HQ, Batangas, and Servers |




## ISP Router

| Destination Network | Next Hop | Purpose |
|---------------------|----------|---------|
| 192.168.0.0/16 | 10.0.12.1 | Route all enterprise private networks to HQ |