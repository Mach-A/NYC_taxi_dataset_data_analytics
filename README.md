# NYC-Yellow-taxi-dataset
# To solve 5 data analytics problems
# To create 3 ML models and also predict 3 unique challenges

# install and set up Spark -- PySpark
# install and set up Spark -- PySpark


!sudo apt update
!apt-get install openjdk-8-jdk-headless -qq > /dev/null

!wget -q https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz

!tar -xzf spark-3.4.1-bin-hadoop3.tgz


!pip install -q findspark
!pip install -q pyspark py4j

import os
import findspark


os.environ["JAVA_HOME"] = "/usr/lib/jvm/java-8-openjdk-amd64"
os.environ["SPARK_HOME"] = "/content/spark-3.4.1-bin-hadoop3"

# Initialize Spark
findspark.init()

from pyspark.sql import SparkSession

# Start Spark session
spark = SparkSession.builder \
    .appName("NYC Yellow Taxi Data") \
    .getOrCreate()

spark

