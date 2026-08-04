# Docker Networks

## Topics Covered

- What is a Docker Network?
- Why `localhost` doesn't work between containers
- Bridge Network
- Creating a Docker Network
- Running containers on the same network
- Container-to-container communication
- Using container names instead of IP addresses

---

## Key Commands

### Create a Network

```bash
docker network create my-network
```

### List Networks

```bash
docker network ls
```

### Run MongoDB on the Network

```bash
docker run -d --name mongo --network my-network mongo
```

### Run Express on the Network

```bash
docker run -d --name backend --network my-network express-demo
```

---

## Example

Instead of:

```text
mongodb://localhost:27017
```

Use:

```text
mongodb://mongo:27017
```

Here, `mongo` is the container name.

---

