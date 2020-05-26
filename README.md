## Handson on NVIDIA Rapids

This example runs on a DGX-1 and uses the RAPIDS Container taken from NGC.  
cuDF is a GPU DataFrame library for loading, joining, aggregating, filtering, and otherwise manipulating data.


docker run -it -p 29999:29999  --rm -v \`pwd\`:\`pwd\` -w \`pwd\` nvcr.io/nvidia/rapidsai/rapidsai:cuda10.1-runtime-ubuntu18.04


you get can data from https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page


cd data   
wget https://s3.amazonaws.com/nyc-tlc/trip+data/yellow_tripdata_2019-02.csv    
wget https://s3.amazonaws.com/nyc-tlc/trip+data/yellow_tripdata_2019-06.csv   

Start Jupyter Notebook
jupyter notebook --port 29999 --ip 0.0.0.0 --allow-root

![After processing](https://github.com/schoenemeyer/rapids-handson/blob/master/figures/rapids-cudf.PNG)


More Material
https://github.com/rapidsai/cudf


https://developer.download.nvidia.com/video/gputechconf/gtc/2019/presentation/s9797-dask-extensions-and-new-developments-with-rapids.pdf

