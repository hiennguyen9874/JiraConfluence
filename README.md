# Jira Confluence

## Usage

### Docker build & up

- `docker compose build`
- `docker compose up -d`

### Jira

- Visit jira: [localhost:18009/](http://localhost:18009/), select language and choose manual configuration
    <div align="center">
        <a href="docs/jira_language.png">
            <img src="docs/jira_language.png" width="75%"/>
        </a>
    </div>
- Configure stand-alone databases
    <div align="center">
        <a href="docs/jira_create_db.png">
            <img src="docs/jira_create_db.png" width="75%"/>
        </a>
    </div>

- Set up application properties
    <div align="center">
        <a href="docs/jira_setup_application.png">
            <img src="docs/jira_setup_application.png" width="75%"/>
        </a>
    </div>
- Cracking
  - Copy `Server ID` from web

  - `docker compose exec -w /opt/atlassian/jira/ jira java -jar atlassian-agent.jar -d -m test@test.com -n BAT -p jira -o http://<IP>:18009 -s <Server ID>`

    <div align="center">
        <a href="docs/jira_generate_licenses.png">
            <img src="docs/jira_generate_licenses.png" width="75%"/>
        </a>
    </div>

    <div align="center">
        <a href="docs/jira_paste_licenses.png">
            <img src="docs/jira_paste_licenses.png" width="75%"/>
        </a>
    </div>
- Configure stand-alone databases
    <div align="center">
        <a href="docs/confluence_create_db.png">
            <img src="docs/confluence_create_db.png" width="75%"/>
        </a>
    </div>
- Setup admin account
    <div align="center">
        <a href="docs/jira_setup_admin_account.png">
            <img src="docs/jira_setup_admin_account.png" width="75%"/>
        </a>
    </div>

### Confluence

- Visit jira: [localhost:18010](http://localhost:18010), pick an app
    <div align="center">
        <a href="docs/confluence_pick_app.png">
            <img src="docs/confluence_pick_app.png" width="75%"/>
        </a>
    </div>

- Cracking
  - Copy `Server ID` from web

  - `docker compose exec -w /opt/atlassian/confluence/ confluence java -jar atlassian-agent.jar -d -m test@test.com -n BAT -p conf -o http://<IP>:18010 -s <COPY FROM WEB>`

    <div align="center">
        <a href="docs/confluence_generate_licenses.png">
            <img src="docs/confluence_generate_licenses.png" width="75%"/>
        </a>
    </div>

    <div align="center">
        <a href="docs/confluence_paste_licenses.png">
            <img src="docs/confluence_paste_licenses.png" width="75%"/>
        </a>
    </div>

## TODO

- Bitbucket
- Prefix

## Acknowledgments

- [gitee.com/pengzhile/atlassian-agent](https://gitee.com/pengzhile/atlassian-agent)
- [programmer.group/docker-installs-jira-and-confluence-cracked-version.html](https://programmer.group/docker-installs-jira-and-confluence-cracked-version.html)
