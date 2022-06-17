https://gitee.com/pengzhile/atlassian-agent
https://programmer.group/docker-installs-jira-and-confluence-cracked-version.html

## Jira

- `docker compose exec -w /opt/atlassian/jira/ jira java -jar atlassian-agent.jar -d -m test@test.com -n BAT -p jira -o http://<IP>:18009 -s <COPY FROM WEB>`

## Confluence

- `docker compose exec -w /opt/atlassian/confluence/ confluence java -jar atlassian-agent.jar -d -m test@test.com -n BAT -p conf -o http://<IP>:18010 -s <COPY FROM WEB>`

# TODO

- Bitbucket
- Prefix
