1) Build the image (recreates the same environment)
docker build -t rust-python .

2) run 
python com_window_code/comencment_marco_polo_code.py

3) Run the container with the repo mounted
Windows PowerShell
docker run --rm -p 8080:80 -p 8081:81 -p 8082:82 -it -v "${PWD}:/work" -w /work rust-python bash


macOS/Linux
docker run --rm -p 8080:80 -p 8081:81 -p 8082:82 -it -v "$(pwd):/work" -w /work rust-python bash



4) Verify tools inside the container

which python
python --version
pip --version
cargo --version


for ml devs 
once ur done with devvelopment make sure u run 
pip freeze 
and copy tht output to requirments.txt 