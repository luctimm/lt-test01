#!/bin/bash
if [ "$1" == "stop" ]; then
sh /opt/atlassian/instances/jira506-BUILD-CLASS/bin/shutdown.sh
elif [ "$1" == "start" ]; then
sh /opt/atlassian/instances/jira506-BUILD-CLASS/bin/startup.sh
elif [ "$1" == "server" ]; then
vi /opt/atlassian/instances/jira506-BUILD-CLASS/conf/server.xml
elif [ "$1" == "logs" ]; then
tail -f /opt/atlassian/home/jira506-BUILD-CLASS/log/*
elif [ "$1" == "catlogs" ]; then
tail -f /opt/atlassian/instances/jira506-BUILD-CLASS/logs/*
elif [ "$1" == "jap" ]; then
vi /opt/atlassian/instances/jira506-BUILD-CLASS/atlassian-jira/WEB-INF/classes/jira-application.properties
elif [ "$1" == "jcp" ]; then
vi /opt/atlassian/home/jira506-BUILD-CLASS/jira-config.properties
elif [ "$1" == "setenv" ]; then
vi /opt/atlassian/instances/jira506-BUILD-CLASS/bin/setenv.sh
elif [ "$1" == "status" ]; then
MYPID=$(ps faux | grep java | awk '/jira510/ { print $2 }')
if [ "$MYPID" == "" ]; then
echo ""
echo "jira506-BUILD-CLASS is not running."
echo ""
else
echo ""
echo "jira506-BUILD-CLASS is running, PID is $MYPID."
echo ""
fi
else
echo ""
echo "Usage: $1 (start|stop|status|logs|catlogs|server|setenv|jap|jcp). "
echo ""
echo "where:"
echo "jap == jira-application.properties "
echo "jcp == jira-config.properties "
echo "server == server.xml "
echo ""
fi
exit 0
