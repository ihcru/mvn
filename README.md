# mvn

## LFS
```sh
curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | sudo bash
sudo apt-get install git-lfs
```

## Install artifact
```sh
mvn install:install-file \
 -DgroupId=com.example \
 -DartifactId=example \
 -Dversion=0.1 \
 -Dpackaging=jar \
 -Dfile=target/example-0.1.jar \
 -DlocalRepositoryPath=../mvn

mvn install:install-file \
 -DgroupId=com.example \
 -DartifactId=example \
 -Dversion=0.1 \
 -Dpackaging=jar \
 -Dfile=target/example-0.1-sources.jar \
 -DlocalRepositoryPath=../mvn \
 -Dclassifier=sources
```

## Use repository
```xml
<repositories>
    <repository>
        <id>ihcru</id>
        <name>ihcru</name>
        <url>https://github.com/ihcru/mvn/raw/master/</url>
    </repository>
</repositories>
```
## Use dependency

### diadocsdk-java
https://github.com/ihcru/diadocsdk-java
```xml
<dependencies>
  <dependency>
    <groupId>ru.kontur.diadoc</groupId>
    <artifactId>diadocsdk</artifactId>
    <version>1.42.0</version>
  </dependency>
</dependencies>
```

