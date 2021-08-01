# Difference between Docker and VM

**Docker** and **Virtual Machine** are **not** the same. The key differences are given as follows

| **Virtual Machine \(VM\)** | **Docker** |
| :---: | :---: |
| Contains one/many applications | Shares kernel with other containers |
| Necessary libraries/binaries | Contains app and all its dependencies |
| Entire guest OS interacts with the apps | Not tied - only needs Docker machine on host, runs as isolated processes in user space on host OS |

