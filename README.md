<h3>Docker Containers - Rapid Prototyping Env</h3>
Contains the following Hortonworks tech stack (within Docker containers):
<br>
<br>&bull; Apache Spark & Apache Zeppelin
<br>&bull; Apache NiFi
<br>&bull; Apache Kafka
<br>&bull; Apache HBase & Apache Phoenix
<br>&bull; Apache Storm
<br>&bull; Apache Solr
<br>
<br>
<br>Docker cleanup:
<br>docker system prune
<br>docker volume prune
<br>docker volume rm $(docker volume ls -qf dangling=true)
<br>
