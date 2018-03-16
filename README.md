# 🚀 nomirror

🌰 Sponsered by _fandogh_   - 💛 Maitained by [pi0](https://github.com/pi0) 

## Docker APT repository

Add apt repository:

```bash
sudo add-apt-repository "deb [arch=amd64] https://docker-download.nomirror.ml/linux/ubuntu/ $(lsb_release -cs) stable"
```
    
Install gpg key:

```bash
curl -fsSL https://docker-download.nomirror.ml/linux/ubuntu/gpg | sudo apt-key add -
```

## JCenter

```diff
--jcenter()
++jcenter { url "https://jcenter.nomirror.ml" }
```

## Docker Proxy

Supports docker centeral registry and K8S!

### For ubuntu >= 16.04 (with systemctl)

Create conf directory:

```bash
mkdir /etc/systemd/system/docker.service.d
```

Create `/etc/systemd/system/docker.service.d/proxy.conf`:

```inf
[Service]
Environment="HTTP_PROXY=http://proxy.nomirror.ml:60606"
Environment="HTTPS_PROXY=http://proxy.nomirror.ml:60606"
Environment="NO_PROXY=localhost,127.0.0.1,localaddress,.localdomain.com"
```

Reload docker:

```bash
systemctl daemon-reload
systemctl restart docker
```

### For ubuntu 14.0.4

Append this lines to `/etc/default/docker`:

```inf
export HTTP_PROXY=http://proxy.nomirror.ml:60606
export HTTPS_PROXY=http://proxy.nomirror.ml:60606
export NO_PROXY=localhost,127.0.0.1,localaddress,.localdomain.com
```

Reload service:

```bash
sudo service docker restart
```
