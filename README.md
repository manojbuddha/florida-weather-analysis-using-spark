# florida-weather-analysis-using-spark

Installation files link: https://gmuedu-my.sharepoint.com/:u:/g/personal/mbuddha_gmu_edu/EdDW8b3ikvFKuy52VMCtVc4Bj0VmfpFHeesiBgxR5RcOZg?e=NFAPRA
<br>
Dataset link: https://gmuedu-my.sharepoint.com/:f:/g/personal/mbuddha_gmu_edu/Ev0ZQVXopIVKssuMXeJQYTwBNFvDdM_PrV-rOcdjahMGCQ?e=jHIFpr

Steps to install Spark:
1) Create a folder 'BigData'
2) Install jre present in the installation files (The link to the installation files is available at the top).
3) Copy Hadoop folder from installation files and place it in 'BigData' folder.
4) Add the below environment variables in system variables.
      <ul>
      <li>Hadoop<br>
      Variable name: HADOOP_HOME<br>
      Variable value: C:\BigData\Hadoop</li>
      <li>Spark<br>
      Variable name: SPARK_HOME<br>
      Variable value: C:\BigData\Spark</li>
      <li>java<br>
      Variable name: JAVA_HOME<br>
      Variable value: C:\Program Files\Java\jre1.8.0_241</li>
      </ul>
5) Copy tmp file from installation files and place it in the C drive.
6) Install vcredist_x64 from installation files.
7) Open command prompt as administrator, navigate to path 'c:\BigData\Hadoop\bin', and run the command 'winutils.exe cmod 777 c:\tmp\hive'.
8) Unzip required spark version from installation files twice using gzip. And rename the final folder to 'Spark' and place it in BigData folder.
9) Now navigate to 'C:\BigData\Spark\bin', and run the command '<b>spark-shell</b>' to open spark shell and verify the spark installation.
10) The spark managemaent console can be viewed in 'https:localhost//4040'.

Steps to link python to use spark and use pyspark:
1) Install anaconda from the Installation files, the destination folder to install anaconda should be 'C:\BigData\Anaconda'.
2) Navigate to 'c:\Bigdata\Anaconda3\Scripts' in command prompt and run the command 'conda list anaconda$'.
3) Run 'Anaconda prompt' as Administrator, and run the below commands
      <ul>
      <li>conda install -c conda-forge findspark
      <li> jupyter notebook --generate-config
      </ul>
4) Open “jupyter_notebook_config.py” file in “C:\Users\{user_name}\.jupyter” folder.
5) And set c.NotebookApp.notebook_dir = 'C:/BigData/~notebookJupyter'.
6)  Create 'C:/BigData/~notebookJupyter' folder.
7)  Run the below commands to connect pyspark to spark, and verify the connection.
~~~
import findspark
findspark.init()
import pyspark
from pyspark import SparkContext
from pyspark import SQLContext
from pyspark.sql import SparkSession
sc = SparkContext.getOrCreate()
spark = SparkSession.builder.getOrCreate()
~~~
