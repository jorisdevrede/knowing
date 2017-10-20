## Configure PyCharm for Spark


### Install pyspark package
**Using pip**

Since version 2.2.0 pyspark can be installed using pip

1. Install the pyspark package `pip3 install pyspark`
2. (Re)start PyCharm


**Using PyCharm Project Interpreter**

1. Go to `File > Settings... > Project > Project Interpreter`
2. Add the `py4j` and `pyspark` packages


### Configure Python 3 in PyCharm 

1. In PyCharm edit the run configuration for either Python/_scriptname_ or Defaults/Python
- Select `Run > Edit Configuration...` in the PyCharm menu
- Set the Python Interpreter to Python 3.x
- Add the environment variables `PYSPARK_PYTHON=python3` and `PYSPARK_DRIVER_PYTHON=python3`
