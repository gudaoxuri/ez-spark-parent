EZ Spark Parent
===
### EZ Spark 构建框架，可使用Scala编写Spark程序基础包。

## How to Use

### Step1 引用

    <dependency>
        <groupId>com.ecfront</groupId>
        <artifactId>ez-spark-parent</artifactId>
        <version>0.1.1</version>
    </dependency>
    
    此pom已包含了spark core，如果要用spark sql等功能需要在项目pom.xml中自行引入，如
    
     <dependency>
        <groupId>org.apache.spark</groupId>
        <artifactId>spark-streaming_2.10</artifactId>
        <version>${spark.version}</version>
        <scope>${spark.scope}</scope>
     </dependency>

### Step2 复写两个属性

    <mainClass>你的启动类</mainClass>
    <spark.scope>provided 或者 compile，前则是默认值，用于打包发布，如果本地调试的话必须改成compile</spark.scope>
    
### Step3 打包发布
    
    mvn assembly:assembly

### Check out sources
`git clone https://github.com/gudaoxuri/ez-spark-parent.git`

### License

Under version 2.0 of the [Apache License][].

[Apache License]: http://www.apache.org/licenses/LICENSE-2.0

