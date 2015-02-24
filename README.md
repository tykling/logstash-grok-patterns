# logstash-grok-patterns
This repository contains my logstash config and grok patterns. It is a work in progress, I am new at this.

- The messages start out by getting their syslog prefix parsed, leaving the rest of the message in the field "syslog_message". 
- If the syslog prefix parsing fails the message will be tagged with "syslog_parsefailure". 
- The messages are then parsed based on the "program" field from syslog using various patterns. 
- Anything left unparsed will have the tag "syslog_message_unparsed".
