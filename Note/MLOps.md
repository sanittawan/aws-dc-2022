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
