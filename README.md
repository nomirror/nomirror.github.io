# 🚀 nomirror

> A mirror service that works!

🌰 Sponsered by _fandogh_    
💛 Maitained by [pi0](https://github.com/pi0) 

# 🌩 Mirrors

## Docker apt repository

1️⃣ Add apt repository:

```bash
sudo add-apt-repository "deb [arch=amd64] https://docker-download.nomirror.ml/linux/ubuntu/ $(lsb_release -cs) stable"
```
    
2️⃣ Install gpg key:

```bash
curl -fsSL https://docker-download.nomirror.ml/linux/ubuntu/gpg | sudo apt-key add -
```
