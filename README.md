## Jira

- `docker compose exec -w /opt/atlassian/jira/ jira java -jar atlassian-agent.jar -d -m test@test.com -n BAT -p jira -o http://localhost:18009 -s B2W9-9PIH-TZDH-709F`

## Confluence

- `docker compose exec -w /opt/atlassian/confluence/ confluence java -jar atlassian-agent.jar -d -m test@test.com -n BAT -p conf -o http://localhost:18010 -s BY55-WEQX-BCI0-GCRF`
