# generator-ng2component
**An angular 2 component/service generator (based on new namespace '@angular/core') that can generate templates for all kinds of angular2 projects.**    

**VERSION 1.1.0**   
current features:    
    1. create a component with full standard structure (check example tree below);   
    2. create a service with full standard structure;    
    3. auto declare component in your current app.module.ts file; (there is a plan for improving to declaring in specific module)    
    4. you decide if you want to use index.ts file    

>**Steps: ( Assuming you have installed node.js [tested against node v6.9.1])**

1. install yeoman (you may need 'sudo' for permission)
    > npm install -g yo
    
2. install this tool
    > globally (may need sudo to install globally): npm install -g generator-ng2component   
    
    > or just to local project: npm install --save-dev generator-ng2component
    
3. run via yeoman
    > yo ng2component
    
4. follow the command line instructions, and your component will be populated in designated directory.
    > it will prompt questions based on your **1st choice**:

    - **what do u wanna generate?**  
        you can generate either component or service or both! default only component
        - **component name?**  
            default: show-message  
            (notice: generator will declare this component for u only if u have src/app/app.module.ts)
        - **resides position?**  
            default under: your_project_root/src/app/, enter '.' will generate in current folder    
        - **style sheet?**  
            choose from scss, css, less  
        - **service name?**  
            default: device  
        - **service resides position?**  
            default under: your_project_root/src/app/shared/services/    
        - **import service into new component?**  
            default: no
        - **omit index.ts?**  
            default: false. it will generate index.ts for each of your cmp/service

    > normally, it will generate following (example) structure under your project/src/app:

    ```
    project-root/
    ├── src/
    │   └── app/
    │       ├── show-message/
    │       │    ├── show-message.component.ts
    │       │    ├── show-message.component.spec.ts
    │       │    ├── show-message.component.scss[less][css]
    │       │    ├── show-message.component.html
    │       │    └── index.ts
    │       └── shared/
    │            └── device/
    │                ├── device.service.ts
    │                ├── device.service.spec.ts
    │                ├── device.ts
    │                └── index.ts
    ```

Find more generators on yeoman: http://yeoman.io/generators/

> TODO (some thoughts):  

1. add 'generate e2e test' option
    * where do u want to generate
    
You're welcome to contribute (open issues, PRs)!
Also, if you think this tool is helpful, please watch/star/fork me on github/npmjs and let more people know it!

## developing logs
> Check current version: npm view generator-ng2component version  
> Check newest version: npm outdated generator-ng2component  
> Update your local version: npm install generator-ng2component
> big changes happened on following versions. Feel free to use older version if you think current version contains issues.

**02/28/2017 v1.1.0** generator can declare component automatically for your app.module.ts now  
**02/22/2017 v1.0.9** capable to omit generating index.ts now  
**11/12/2016 v1.0.6** generator is capable to import service automatically into component now  
**11/09/2016 v1.0.3** now you have stable service generator  
**11/8/2016 v0.0.11** fixed ts linting warnings  
**11/07/2016 v0.0.7** added global colors/fonts ref to scss  
**11/01/2016 v0.0.5** first stable version, can only generate component