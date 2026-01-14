1) Build the image (recreates the same environment)
docker build -t rust-python .

2) Run the container with the repo mounted

Windows PowerShell

docker run --rm -it -v "${PWD}:/work" -w /work rust-python bash


macOS/Linux

docker run --rm -it -v "$(pwd):/work" -w /work rust-python bash

3) Verify tools inside the container
which python
python --version
pip --version
cargo --version


for ml devs 
once ur done with devvelopment make sure u run 
pip freeze 
and copy tht output to requirments.txt 