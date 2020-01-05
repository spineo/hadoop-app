# hadoop-app

In this example I will be setting up an [Apache Hadoop](https://hadoop.apache.org/) Multi-node Cluster on [AWS](https://aws.amazon.com/) and processing a set of input text files using the Hadoop Streaming API and Python Mapper/Reducers. The simple application will perform the same task we saw in my [Spark App](https://github.com/spineo/spark-app) but instead use the Hadoop framework to output the alphabet letter counts.

The setup involves a main node and two data nodes and use Hadoop v2.10.0 available from one of the mirros at https://hadoop.apache.org/releases.html

## Launch the Instances

For this example, I will click on _Launch Instance_ and select an Amazon Linux t2.micro 64-bit (x86) configuration (Free tier eligible). For now I will not perform additional configurations of the instances, add storage, or attach any security group(s) but I will add a tag (under the _Add Tags_ section) with a key _Name_ for each of the three instances and values _HadoopMainNode_, _HadoopDataNode1_, and _HadoopDataNode2_ respectively. As I launch each instance I will be using a pre-existing key pair (i.e., certificate).
