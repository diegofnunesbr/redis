# Redis

### Instalar o Redis no Kubernetes:

- `git clone git@github.com:diegofnunesbr/redis.git`
- `cd redis`
- `helm install --create-namespace redis -n redis .`

### Configurar o Redis no arquivo hosts do Windows:

- `sudo tee -a /mnt/c/Windows/System32/drivers/etc/hosts <<< "$(ifconfig eth0 | grep 'inet ' | awk '{print $2}') redis.local"`

### Remover o Redis no Kubernetes:

- `helm uninstall redis -n redis`
