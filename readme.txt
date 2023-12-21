-------------------------------------------------

			# ELK-STUDY #

-------------------------------------------------

https://www.elastic.co/kr/
https://www.elastic.co/guide/index.html
https://www.elastic.co/guide/kr/index.html

-------------------------------------------------

-ELK Stack?
https://www.elastic.co/kr/what-is/elk-stack

-Elasticsearch?
https://www.elastic.co/kr/what-is/elasticsearch

-------------------------------------------------

-elastic-stack
https://www.elastic.co/kr/elastic-stack

-elasticsearch
https://www.elastic.co/kr/elasticsearch/

	-Elasticsearch Reference
	https://www.elastic.co/guide/en/elasticsearch/reference/current/index.html?baymax=KR-ES-getting-started&elektra=landing-page
	https://victorydntmd.tistory.com/category/OpenSource/Elasticsearch
	
-logstash
https://www.elastic.co/kr/logstash
	
-beats
https://www.elastic.co/kr/beats

-kibana
https://www.elastic.co/kr/kibana

-------------------------------------------------

-GrokConstructor
http://grokconstructor.appspot.com/
http://grokconstructor.appspot.com/do/match?example=2

-------------------------------------------------

-example

-reference
https://www.inflearn.com/course/elk-%EC%8A%A4%ED%83%9D-%EB%8D%B0%EC%9D%B4%ED%84%B0-%EB%B6%84%EC%84%9D/#curriculum
https://soyoung-new-challenge.tistory.com/56
https://kimseunghyun76.tistory.com/category/DB%26NoSQL/Elasticsearch%2CELK


-Pre-step
	node instll
	java instll or set JAVA_HOME=C:\dev\elk-study\elasticsearch-7.8.0\jdk
	
-Download
	https://www.elastic.co/kr/downloads/elasticsearch
	https://www.elastic.co/kr/downloads/logstash
	https://www.elastic.co/kr/downloads/beats
	https://www.elastic.co/kr/downloads/beats/filebeat		
	https://www.elastic.co/kr/downloads/kibana

-Install 
 Install Path : C:\dev\elk-study 
	C:\dev\elk-study\elasticsearch-7.8.0
	C:\dev\elk-study\logstash-7.8.0		
	C:\dev\elk-study\filebeat-7.8.0	
	C:\dev\elk-study\kibana-7.8.0

-Run  
-elasticsearch (default jvm elasticsearch-7.8.0\jdk) 		
	cmd  : C:\dev\elk-study\elasticsearch-7.8.0\bin\elasticsearch.bat
	
	http://localhost:9200/	
	
	*search index
	 http://localhost:9200/_cat/indices?v&pretty	

-logstash
	cmd  : set JAVA_HOME=C:\dev\elk-study\elasticsearch-7.8.0\jdk
		   C:\dev\elk-study\logstash-7.8.0\bin\logstash.bat -f C:\dev\elk-study\logstash-7.8.0\config\logstash.conf
	
	*plugin update (init install)
		C:\dev\elk-study\logstash-7.8.0\bin\logstash-plugin update logstash-input-beats
		C:\dev\elk-study\logstash-7.8.0\bin\logstash-plugin update logstash-filter-useragent
		C:\dev\elk-study\logstash-7.8.0\bin\logstash-plugin update logstash-filter-geoip
				
	*modify - logstash.conf 
		
-filebeat
	cmd  : C:\dev\elk-study\filebeat-7.8.0\filebeat.exe -c C:\dev\elk-study\filebeat-7.8.0\filebeat.yml -e -v
	
	*modify - filebeat.yml
				  			  				
	*access.log <- http://grokconstructor.appspot.com/do/match?example=2
		10.121.123.104 - - [01/Nov/2012:21:01:04 +0100] "GET /cluster HTTP/1.1" 200 1272
		10.121.123.104 - - [01/Nov/2012:21:01:17 +0100] "GET /cpc/auth.do?loginsetup=true&targetPage=%2Fcpc%2F HTTP/1.1" 302 466
		10.121.123.104 - - [01/Nov/2012:21:01:18 +0100] "GET /cpc?loginsetup=true&targetPage=%252Fcpc%252F HTTP/1.1" 302 -
		10.121.123.104 - - [01/Nov/2012:21:01:18 +0100] "GET /cpc/auth.do?loginsetup=true&targetPage=%25252Fcpc%25252F&loginsetup=true HTTP/1.1" 302 494
	 
-kibana
	cmd  : C:\dev\elk-study\kibana-7.8.0\bin\kibana.bat
	
	http://127.0.0.1:5601/



