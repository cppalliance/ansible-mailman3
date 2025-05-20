
## Upgrade

To upgrade packages, first discover the latest pip package version in another container venv.  

```
pip3 install mailman
pip3 install mailman-web
pip3 list

pip3 install mailman-hyperkitty
pip3 install importlib-resources
pip3 list
```

Place the latest versions into ansible's defaults/main.md.



