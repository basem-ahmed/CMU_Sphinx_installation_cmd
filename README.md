# CMU_Sphinx_installation_cmd
CMU Sphinx installation cmd
# CMU sphinx Installation steps
## sphinxbase
```
git clone https://github.com/cmusphinx/sphinxbase.git
./autogen.sh
make 
sudo make install
```

# add sphinx libs to system libs 
```sudo nano /etc/ld.so.conf```

add new line /usr/local/lib
```
sudo ldconfig
ldconfig -p | grep local
```

# pocketsphinx
```
git clone https://github.com/cmusphinx/pocketsphinx.git
cd pocketsphinx
./autogen.sh
make 
sudo make install


```

# sphinxtrain
```
git clone https://github.com/cmusphinx/sphinxtrain.git
./autogen.sh
make 
sudo make install
```

## cmuclmtk
```
svn checkout svn://svn.code.sf.net/p/cmusphinx/code/trunk/cmuclmtk cmuclmtk-code
./autogen.sh
make 
sudo make install
```

## force alignment
'''
svn checkout svn://svn.code.sf.net/p/cmusphinx/code/trunk/sphinx3

./autogen.sh

make 

ln -s /home/motaz/myspeech/cmusphinx-svn-source/trunk/sphinx3/src/programs/sphinx3_align /usr/local/libexec/sphinxtrain/sphinx3_align
