# Docker

## Configuration

### Avoiding interfering networks

If you have Docker networks that interfere with your local networks, you can configure Docker to use another address range by adding the following to `/etc/docker/daemon.json`:

```json
{
 "bip": "172.153.0.1/24",
 "default-address-pools":[
   {"base":"172.154.0.0/16","size":24}
 ]
}
```
