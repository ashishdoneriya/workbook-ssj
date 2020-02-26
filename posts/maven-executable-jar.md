---
title : "How to create executable jar in maven"
created : "2019-03-31T03:17:00+05:30"
updated : "2019-03-31T03:17:00+05:30"
categories : ["java"]
tags : ["java", "maven"]
summary : "Snippet code to create an executable jar in maven"
---

### Termiologies

```xml
<build>
    <plugins>
      <plugin>
        <artifactId>maven-assembly-plugin</artifactId>
        <configuration>
          <archive>
            <manifest>
              <mainClass>io.github.ashishdoneriya.Test</mainClass>
            </manifest>
          </archive>
          <descriptorRefs>
            <descriptorRef>jar-with-dependencies</descriptorRef>
          </descriptorRefs>
        </configuration>
        <executions>
          <execution>
          
            <!-- this is used for inheritance merges -->
            <id>make-assembly</id>
            
            <!-- bind to the packaging phase --> 
            <phase>package</phase>
            
            <goals>
              <goal>single</goal>
            </goals>
          </execution>
        </executions>
      </plugin>
    </plugins>
  </build>
```