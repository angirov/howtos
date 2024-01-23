1. Situation: you want to install pip packages locally (`sudo pip` is really bad practice and sometimes also impossible)
2. Install or find installed python binary of appropriate version. [-> How to install python as non-root](https://askubuntu.com/questions/566324/how-to-install-python-as-a-user)
3. Run venv through this binary. E.g. in my env miniconda has python-11 which is okay for me: `/homes/<USER>/miniconda3/bin/python3.11 -m venv myvenv`
4. Activate the virtual env: `source myvenv/bin/activate`
5. In the virtual env dir (e.g. `myvenv`) you find file `pyvenv.cfg`
6. Thre set `include-system-site-packages = true`
7. Now you can `pip install --user -r requirements.txt`
