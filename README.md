
1. Create conda environment:

```
  conda create -n pysep
  conda activate pysep
``` 
  


2. Download and install PySEP:

```
  git clone https://github.com/adjtomo/pysep.git
  cd pysep
  conda env update --file environment.yml
  cd ..
``` 

**_NOTE:_** 
  The above installation works for most purposes, but see 
  [PySEP docs](https://pysep.readthedocs.io/en/latest/) the most detailed and 
  up-to-date installation instructions.  
  


3. Download PySEP configuration files:

```
  git clone --branch pysep_example https://github.com/rmodrak/mtbench.git pysep_example
``` 
  



4. Download waveforms from IRIS data sources using PySEP:

```
  cd pysep_example
  pysep -c pysep_config.yaml
``` 



5. After the waveform downloads finish, SAC files and corresponding 
   MTUQ "weight files" will be present in `2006-10-09T013528_NORTH_KOREA/`.

   These waveforms can then be used with `mtuq_script.py` to reproduce the 
   results in `mtuq_output/`.

   To run the MTUQ script, it is necessary to switch to a new virtual
   environment in which MTUQ installed. See 
   [MTUQ docs](https://uafgeotools.github.io/mtuq/install/index.html)
   for installation instructions.

