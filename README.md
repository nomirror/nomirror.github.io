# 🌩 nomirror mirrors!

> Sponsered by Fandogh. Maitained by [pi0](https://github.com/pi0) 💚


## Docker apt repository

Add apt repository:

```bash
sudo add-apt-repository "deb [arch=amd64] https://docker-download.nomirror.ml/linux/ubuntu/ $(lsb_release -cs) stable"
```
    
Install gpg key:

```bash
curl -fsSL https://docker-download.nomirror.ml/linux/ubuntu/gpg | sudo apt-key add -
```
