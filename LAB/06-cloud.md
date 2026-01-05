# 1. container
- if you explicitly remove a container using the docker rm command, the container's file system will be deleted.
| **Feature**         | **Option 1 (run)**                | **Option 2 (start)**              | **Option 3 (exec)**             |
|---------------------|-----------------------------------|-----------------------------------|---------------------------------|
| **Action**          | Create & Start                    | Resume                            | Enter/Execute                   |
| **Container State** | Doesn't exist yet.                | Exists, but is Stopped.           | Exists and is Running.          |
| **Data/Changes**    | Starts fresh (New).               | Keeps changes from last time.     | Interacts with live data.       |
| **Analogy**         | Buying a brand new car.           | Turning the key in a car you already own. | Jumping into a car that is already driving. |

```shell
docker images
docker byuld -t NAME

docker ps -a
docker start NAME
docker exec -it NAME cmd

```

# 2. Hyper-V