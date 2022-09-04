# Cloud Computing Foundations
[Cloud Computing Foundation](https://www.coursera.org/learn/cloud-computing-foundations-duke) by Duke University

## Week II
> talent is one aspect, but it's not the most important aspect of an effective team

> If there is no goal, it's really hard to have an effective team

Ideas of what it takes to be effective in terms of a team
1. Clear, Elevating Goal
2. Results-Driven Structure
3. Competent Team Members
4. Unified Commitment (Is everyone on the same page)
5. Collaborative Climate
6. Standards of Excellence 
7. External Support and Recognition
8. Principled Leadership

### Effective Technical Project Management
Learning Objectives
1. Identify primary factors that influence the success of a technical project
2. Cultivating positive team dynamics through transparent and timely communication

Key principles 
* **Quarterly schedule** that identifies week by week what it is that you'll build.
* **Weekly Demo**: _If you can't demo each week you probably not going to hit your deadline_
* The code is **always in a deployable state**.
* **Automated testing**: **If it is not automated, it is broken**
* Tickets sweet spot: 4 hours to 3 days time window
* Avoid the hero, _who jumps in and save the day_ (hero-drived development)
* Kaizen, from Japanese Automobile Industry: Continuous Improvement

Anti-patterns 
1. Hero-Driven development
2. Crisis-Driven development
3. HiPPO-Diven development (Highest-paid person's opinion, e.g CEO. Investor, ...) 
4. Heavy SCRUM: Mimic what appears to be succesful. 
5. Faith in people vs. Faith in process.


> Hope is not a strategy

### Reference 
* [Teamwork: What Must Go Right/What Can Go Wrong (SAGE Series in Interpersonal Communication)](https://www.amazon.com/Teamwork-Right-Wrong-Interpersonal-Communication/dp/0803932901) by Carl Larson (Author), Frank M J LaFasto (Author)


## Week III

### AWS Cloud
Tests:
* Functional
* Integration
* Load

> Linting: Catches bugs before they happen. 

Python Virtual Env:
* Isolates Python to a directory
* Best practice


GitHub Actions
* Continuous Integration: Form of automated testing.
* SaaS based continuous integration server

Sample onboarding scripts and resources 
* https://github.com/noahgift/multi-cloud-onboard

CI: 
* The software is always in a known state
* Saves time

### Azure Cloud
* Unit tests: low level. 
* Integration tests: verify that different modules or services worked well together. 
* Functional tests: Are verifying that the business requirements of an application say a web service returns the right status code. 
* End to end testing: Is a way of mimicking users and how they use the software 
* Acceptance testing: A formalized way of verifying that let's say a payroll application sends out the payments. 
* Performance testing or load testing: Is going to test how the app will perform under load. 
* Basic sanity testing: It verifies that if you also do some exploratory data analysis that you can ensure that things are working properly. 

> How much testing: Just enough to solve the problem. 

Testing Strategy:
* Just right: Not too much, neither too litle. Just enough for knowing what we do works. 
* Judgment: Do you suspect something may be wrong, write the test.
* Save time: The most common mistake developers think of. Do not debug the same code again.
* Automation: 

It is called "Kaizen":
> [Kaizen](https://en.wikipedia.org/wiki/Kaizen) is a concept referring to business activities that continuously improve all functions and involve all employees from the CEO to the assembly line workers. Kaizen also applies to processes, such as purchasing and logistics, that cross organizational boundaries into the supply chain. 

#### Azure resources and futher reading/videos
* https://paiml.com/docs/home/books/cloud-computing-for-data/chapter01-getting-started/#microsoft-azure
* [Azure Cloud Shell - Introduction](https://www.youtube.com/watch?v=rXXtJpcVems)
* [Azure Integration - Scaffold](https://www.youtube.com/watch?v=0IAcF4cfGmI)


### Scaffold Python Project 
For use with Cloud9, Azure and GCP
* https://github.com/skounis/cdf-scaffold


### Google Cloud 
#### Google Cloud resources and futher reading/videos
* https://paiml.com/docs/home/books/cloud-computing-for-data/chapter01-getting-started/#gcp-google-cloud-platform

#### Create a virtual env
```bash
which virtualenv
virtualenv ~/.cdf-scaffold
source .cdf-scaffold/bin/activate
ssh-keygen -t rsa
```

#### Continuous Delivery
> The code is always in a deployable state both in term the application software and the infrastructure. 

#### Build Servers
Some examples:
* GitHub Actions
* Jenkings
* AWS Code Build (Cloud native)

Jobs targeting the code:
* Lint the code
* Test the code
* Deploy the code/application

##### Infrastructure as Code (IaC)
Update or create an environment. It will be mapped to the source control (eg `staging`, `test` or `production` branches). We have ENVs for reach branch. 
Some examples:
* Terraform
* Cloud Formation

#### Continuous Delivery - A real example
* Repo: https://github.com/skounis/cdf-gcp-flask-ml-deploy

Setup
```bash
virtualenv ~./.cdf-gcp-flask-ml-deploy
source ~./.cdf-gcp-flask-ml-deploy/bin/activate
make install
```

Run localy (Cloud ENV):
```bash
python main.py
```

Google Cloud Deploy
```bash
gcloud app deploy
```

#### Cloud Build
1. Create a triger (region europe-west1)
    - https://console.cloud.google.com/cloud-build/triggers;region=europe-west1?project=cdf-cloud-data-cd
2. Configure settings
    - https://console.cloud.google.com/cloud-build/settings/service-account?project=cdf-cloud-data-cd
3. Settings
    - Enable "App Engine": You can do deploys for me
    - Enable "Service Accounts": Do this on my behalf.
4. Make a commit to `master`
