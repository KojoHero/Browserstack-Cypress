# Browserstack-Cypress Integration

**After creating your cypress project, below is how to integrate browserstack into it**

1. Install the BrowserStack CLI
    `npm install -g browserstack-cypress-cli`

2. Create and configure the browserstack.json. Run the command below
    `browserstack-cypress init`

    -You should see similar configuration in the created file-
    ```
        {
            "auth": {
                "username": "testaccount_23su9Z",
                "access_key": "9ZxPSqMuRFdheHYZ28Wx"
            },
            "browsers": [{
                "browser": "chrome",
                "os": "Windows 10",
                "versions": ["latest", "latest - 1"]
                },
                {
                "browser": "firefox",
                "os": "OS X Mojave",
                "versions": ["latest", "latest - 1"]
                },
                {
                "browser": "edge",
                "os": "OS X Catalina",
                "versions": ["latest"]
                }
            ],
            "run_settings": {
                "cypress_config_file": "./cypress.config.js",
                "cypress_version": "12.3",
                "npm_dependencies": {
                "npm-package-you-need-to-run-tests-1": "^1.2.1",
                "npm-package-you-need-to-run-tests-2": "^7.1.6-beta.13"
                },
                "project_name": "Cypress Kitchen Sink Example",
                "build_name": "Build no: 1",
                "parallels": 5,
                "exclude": ["some-folder/test.js", "static/*.pdf"]
            }
        }
    ```

3. Add your browserstack username and access key to the browserstack.json file

4. Add the cypress version to the browserstack.json 
   ```
   {
    ...
    "run_settings": {
        ...
        "cypress_version": "12.latest",
        ...
        }
    ...
   }
   ```

