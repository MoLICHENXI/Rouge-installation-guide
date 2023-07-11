# Rouge-installation-guide
Install Rouge Package which used for summarization generation task

1、git clone https://github.com/MoLICHENXI/Rouge-installation-guide.git  
  
2、进入Linux服务器(Go into Linux)  
cd ROUGE-1.5.5/  
chmod 777 *.pl    ###给pl文件可执行权限  
cd data/  
rm WordNet-2.0.exc.db  
cd WordNet-2.0-Exceptions/  
sudo chmod 777 buildExeptionDB.pl  
./buildExeptionDB.pl . exc WordNet-2.0.exc.db         ###注意给.pl文件可执行权限  
cd ..  
ln -s WordNet-2.0-Exceptions/WordNet-2.0.exc.db WordNet-2.0.exc.db  
  
3、下载pyrouge(Download pyrouge)  
注意不要从pip安装，会出现问题，在shell中输入以下命令安装。（notice:Do not use pip command to install pyrouge or you will get an error.Please enter the command under this to install!!!）   
cd pyrouge  
pip install -e .   
pyrouge_set_rouge_path </absolute/path/to/ROUGE-1.5.5/directory>（这一步是ROUGE1.5.5路径）  
python -m pyrouge.test  
  
如果最后一步执行成功则成功安装！！(if the last command successfully run, then it has been successfully installed!!!)  
