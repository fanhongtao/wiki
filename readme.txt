
1. Copy directory 'Catalina' to Tomcat's $CATALINA_HOME/conf
    If thie wiki directory is not in E:/Git, change 'E:/Git/wiki' in the XML files to the real path.

2. Modify $CATALINA_HOME/conf/server.xml, add ' URIEncoding="UTF-8"' to element '<Connector port="8080"'.
    For example, change 
        <Connector port="8080"
                       maxThreads="150" minSpareThreads="25" maxSpareThreads="75"
                       enableLookups="false" redirectPort="8443" acceptCount="100"
                       debug="0" connectionTimeout="20000" 
                       disableUploadTimeout="true"/>

    to
        <Connector port="8080"
                    maxThreads="150" minSpareThreads="25" maxSpareThreads="75"
                    enableLookups="false" redirectPort="8443" acceptCount="100"
                    debug="0" connectionTimeout="20000" 
                    disableUploadTimeout="true" 
                    URIEncoding="UTF-8"/>

3. Modify cfg/template.properties, 
	var.wikiurl
	var.wikipath
    to the actual URL and path.

4. Start tomcat.


