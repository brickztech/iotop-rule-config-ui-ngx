Configuration UI for IoToP Rule Nodes

## Build steps

1) Switch to iotop/release-3.3 branch
    ```
    git checkout iotop/release-3.3 
    ```
2) Cleanup
    ```
    yarn run cleanup 
    ```
3) Get IoToP UI dependency
    ```
    yarn run get:iotop 
    ```
4) Install dependencies
    ```
    yarn install 
    ```
5) Production build    
    ```
    yarn run build 
    ```
    Resulting JavaScript should be here:
    ```
    ./target/generated-resources/public/static/rulenode-core-config.js
    ```
6) Deploy Rule Nodes UI JavaScript code to ThingsBoard

    Resulting **rulenode-core-config.js**
    should be copied to ```rule-engine/rule-engine-components/src/main/resources/public/static/rulenode/```
    directory of IoToP repository.

7) Run Rule Nodes UI in hot redeploy mode

    ```
    yarn start
    ```
    
    By default, Rule Nodes UI will be available on port 5000 (http://localhost:5000)
