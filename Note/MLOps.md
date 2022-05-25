## MLOps
Speakers: Shelby Eigenbrode (Principal AI/ML solutions architect), Bobby Lindsey (senior ML/AI architect)

### MLOps
- the intersection between ML, DevOps, and data engineering
- focus of the talk is technology
- focus on SageMaker service
- ML pipelines are important to reduce redundancy, adjusting data sources which lead to manual update of source code, introduce quality gates

### challenges in MLOps pipeline
- lack of data strategy
- gap between model building and model deployment
- skill sets across persona (building, production are not the same group of people)
- many pipelines involved like data, model building, deployment

### Tools 
- SageMaker pipelines, Amazon MWAA, AWS step functions
- main tool is SageMaker

### SageMaker Pipelines Components
Components include
- 1st component: SageMaker Pipelines = SDK, can be looked up in a studio. used in model development and operations. = building largely
- 2nd component: SageMaker model registry 
- SageMaker Projects basically is a template that encapsulates Pipelines and registry
- templates should be created by people with DevOps background, architect. Consumers are data scientists

### Demo
- using SageMaker studio
- demo "Projects" > create project already populated by many pre-built templates
- some customers don't use SageMaker end to end, so there are many options for the templates
- looks like most people use Jenkins, Github (source code), Gitlab
- can start with pre-built templates and modify it
- there is also AWS service catalogue with project templates
- you get 2 repos (model build and model deploy)
- cloning means cloning to your studio environment
- basically, you can view a dag in the studio for the steps in the pipeline
- also has explainability, bias report, and metrics were you have to go to manually approve a model
- using the pipeline is really helpful in tracing data lineage to understand how the model was trained and the data involved, versioning 
