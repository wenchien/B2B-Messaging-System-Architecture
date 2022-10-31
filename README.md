![Java Versions][java-version]
![Maven][maven-version]
![Kafka][kafka-version]
![JUnit][junit-version]
![Log4j2][log4j2-version]
![LogStash][logstash-version]
![Kibana][kibana-version]
![ElasticSearch][elasticsearch-version]



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li><a href="#system-diagram">System Diagram</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

The project aims to migrate monolithic B2B messaging system to a new and more modern system that utizilies Spring Boot, Docker, Microservices and Monitoring (logstash and ElasticSearch) that will resolve a lot of the maintenance costs / time that backend developers need to spend.

Do note this is a barebone / prototype / proof of concept. There will be flaws / ideas that haven't been considered / evaluated thoroughly but it's generally better to have something down (something is better than nothing afterall).

By utilizing such design, the frontend (i.e. enterprise portal) can easily be migrated to newer technology (React, AngularJS). It should speed up development time comparing to a direct client-to-microservice communication architecture. 


<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Built With

* ![Java Versions][java-version]
* ![Maven][maven-version]
* ![Kafka][kafka-version]
* ![JUnit][junit-version]
* ![Log4j2][log4j2-version]
* ![LogStash][logstash-version]
* ![Kibana][kibana-version]
* ![ElasticSearch][elasticsearch-version]
* See the ![pom.xml](https://github.com/wenchien/ExcelToPDFForms-Editor/blob/master/pom.xml) for all relevant dependencies

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## System Diagram
<p align="center">
  <img src="https://github.com/wenchien/B2B-Messaging-System-Architecture/blob/master/images/SystemDiagram.png" width="75%">
</p><p align="center">
  <em>Main B2B System</em>
</p>
</br>
</br>

Each sub-module utilizes `chain of responsibility` design pattern. It is done this way to ensure better code readability and scalability. In addition, each sub-module will implement `event validation` to ensure consistencies.

This system aims to solve:
1. Single service / monolithic service deployment -> since we constantly receive messages sent from our trading partners / customers, there's no reason code re-deployment / features changes should cause disturbance in message processing.
2. Features deployment time -> resolves similar to the issue mentioned in #1 thanks to kafka's partitioning feature.
3. 

</br>

### Sub-modules / Microservices:

<p align="center">
  <img src="https://github.com/wenchien/B2B-Messaging-System-Architecture/blob/master/images/Marshalling.png" width="75%">
</p>
<p align="center">
  <em>Improved message marshalling / unmarshalling process</em>
</p>

</br>
</br>

<p align="center">
  <img src="https://github.com/wenchien/B2B-Messaging-System-Architecture/blob/master/images/Fileprocessing.png" width="75%">
</p>
<p align="center">
  <em>Improved file processing (data population from static files)</em>
</p>

</br>
</br>

<p align="center">
  <img src="https://github.com/wenchien/B2B-Messaging-System-Architecture/blob/master/images/DynamicDataSource.png" width="75%">
</p>
<p align="center">
  <em>Improved dynamic data source population (connecting to database...etc.)</em>
</p>

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [ ] Version 1.0.0 release

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- LICENSE -->
## License

MIT License

Copyright 2022 Wen Chien Chang

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[javafx-version]: https://img.shields.io/badge/JavaFX-19--ea%2B8-orange
[java-version]: https://img.shields.io/badge/Java-8%2B-red
[maven-version]: https://img.shields.io/badge/maven-v1.0-blue
[kafka-version]: https://img.shields.io/badge/Kafka-3.1.2-red
[junit-version]: https://img.shields.io/badge/JUnit-4.13.2-green
[log4j2-version]: https://img.shields.io/badge/log4j2-4.13.2-yellowgreen
[logstash-version]: https://img.shields.io/badge/Logstash-8.4-red
[kibana-version]: https://img.shields.io/badge/kibana-v1.0-blue
[elasticsearch-version]: https://img.shields.io/badge/ElasticSearch-0.0-green
