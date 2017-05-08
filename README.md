Pivotal Knowledge Base Guide  <img src="https://logo.clearbit.com/gopivotal.com" display="inline" height="30" />
===========

### Introduction to the KB article

The Knowledge Base (KB) is a customer’s best friend during the “help me help myself” phase of exploring your product. Customers and Pivotal Support Engineers read the KB articles to solve their problems. Keep your feet on customer's shoes when you are writing the KB article.

Your KB article should capture actionable steps to help them solve their problems and not aloof them from the recurring issues. The article should assist them to gather information about the background and should include URLs to Documentation or other resources if they want to learn more about the product.

### KCS

Knowledge Centered Support (KCS) is a method where you solve the problem once and reuse the resolution multiple times.

Read more in [Inside Pivotal KCS Page](http://https://sites.google.com/a/pivotal.io/inside-pivotal/departments/pivotal-support/Knowledge-Centered-Support/knowledge-management).

### Write a KB Article

Anyone at Pivotal can write a Knowledge Base article. If you have information that can help our customers troubleshoot by themselves and resolve their problems, help us capture it by writing a KB. 

Follow the simple steps below to write a KB article in Github. 
1. Search the Knowledge Base and Documentation to ensure what you want to write is not already there. 
2. Check the Product Knowledge Base in detail. For example, take a look at Pivotal Cloud Foundry Knowledge Base if you are writing a PCF article.
3. Navigate to the [KB repo in Github].
4. Choose a template based on the document type.
5. Under "components," choose the right folder based on the ERT product.
6. Create a new ".md" file. You can use the template from step 4.
7. Leave the "ID" blank.
8. Fill out the article following the instructions in the template.
9. Submit a PR to the Knowledge Management Team. Send a message to GSS KM or ping in this Slack channel #gss-platform-kbs to let them know. The KM team will merge to the master and the KB will be updated in the knowledge base.
10. Log into the [Agent Dashboard] using your OKTA credentials.



<!--- Overview
------------------

<!----   [Getting Started](#getting-started)
    - [Criteria for an article](#criteria-for-an-article)
-   [Workflow](#workflow)
    - [Overview](#overview)
    - [Suggest article](#suggest-an-idea-or-article-update)
    - [Create article](#create-article)
    - [Submit article](#submit-article)
    - [Article review](#article-review)    
-   [Roles](#roles)
    - [Contributor](#contributor)
    - [Knowledge Management](#knowledge-management)
    - [Subject Matter Expert (SME)](#subject-matter-expert-sme)
-   [Knowledge Base Topics](#resources)    
-   [Resources](#resources)
    - [Labels](#labels)
    - [Style Guide](#style-guide)
    - [Templates](#templates)
    - [Bookmarks](#bookmarks)
    - [Glossary](#glossary)
    - [Roadmap](#roadmap)

<!--- Getting Started
------------------------------

<!--- ### Criteria for an article

<!--- When coding and testing activities for the story have been completed, and the automated tests for it have all passed, the developer(s) click the Finish button (or possibly their commit message does this via Tracker’s SCM integration.

<!---|Template|Definition|Example|
|---|---|---|
|[Break-fix Guide](https://github.com/pivotal-gss/pcf-kb-process/blob/master/templates/break-fix.md)|Articles concerning any bugs and fixes, providing a solution for an error, falls under the Break-fix category.|[Smoke Test Errand](https://discuss.pivotal.io/hc/en-us/articles/236388567)|
|[Checklist](https://github.com/pivotal-gss/pcf-kb-process/blob/master/templates/checklist.md)|When performing a task that requires certain things to be pre-available, use the Checklist template to specify those requirements.|[GemFire Kernels and JDKs](https://discuss.pivotal.io/hc/en-us/articles/221345988)|
|[Concepts](https://github.com/pivotal-gss/pcf-kb-process/blob/master/templates/concepts.md)|Concepts template applies to any article that is meant for explaining the workings and the theory of a product.|[vSphere IaaS Operations](https://discuss.pivotal.io/hc/en-us/articles/221609547)|
|[How To](https://github.com/pivotal-gss/pcf-kb-process/blob/master/templates/how-to.md)|Choose this template when the article talks about performing a task i.e. "How to" do the task.|[BOSH SSL Certificate](https://discuss.pivotal.io/hc/en-us/articles/115000453368)|
|[Tools](https://github.com/pivotal-gss/pcf-kb-process/blob/master/templates/tools.md)|To introduce any new or updated tool concerning the product or the usage of it.|[Greenplum Backup Time Collector](https://discuss.pivotal.io/hc/en-us/articles/218274158)|
|[Troubleshooting Guide](https://github.com/pivotal-gss/pcf-kb-process/blob/master/templates/troubleshooting-guide.md)|A guide to provide troubleshooting steps.|[CFOPs Support](https://discuss.pivotal.io/hc/en-us/articles/226220147)|

<!---Workflow
------------------------------

<!---<img src="img/workflow.png?" display="inline" />

### Suggest an idea or Article Update
Write stories. The customer, project or product manager (PM), or product owner (PO) adds new feature stories.

- You will only be able to switch to Simplified Workflow if:
- There is only one project being viewed by your board (to check this, look at the board's filter); and
- That project uses a JIRA workflow scheme which only has one workflow for all issue types; and

### Create article
Mock-ups, assets, or other examples may be attached to stories and/or epics. Stories are in the unscheduled state

- Review the Knowledge Base Topics
- Fork the Knowledge Base Topic repository
- Clone your fork
- Making and pushing changes

### Submit article
When creating new articles, please make sure you mark the article as being a draft until it has been approved by another support engineer.  

#### Github
- Making a Pull Request
- There is only one project being viewed by your board (to check this, look at the board's filter);
- That project uses a JIRA workflow scheme which only has one

#### Command Line

They are added to the Icebox, are unestimated, or if they have points to estimate in place of an action button.

    git clone --recursive git@github.com:<username>/gitflow.git
    cd gitflow
    git branch master origin/master
    git flow init -d
    git flow feature start <your feature>

### Article Review

The article would be reviewed by another Subject Matter Expert (SME) to verify the credibility of the content, for instance:

- That project uses a JIRA workflow scheme which only has one workflow for all issue types; and
- Your workflow only uses Post Functions, Validators, and Conditions which are provided by Atlassian (not any which are provided by add-ons);

### Publish Article

 Once an article is reviewed, it will go through a final check by the KM team and then be publsihed. 

 - For publishing the article, the KM team would merge the pull request created with the original fork and save the changes.
 - The article would now be ready to be published.

## Knowledge Base Topics
This might be done in an activity with other team members, such as story mapping, specification workshops

### Pivotal Cloud Foundry

|Repository|Components||
|---|---|---|
|Configuration|Networking, Storage |Knowledge Base|
|[CAPI](https://github.com/pivotal-gss/pcf-capi-kb)|Cloud Controller, CC Bridge, Stager, TPS|Knowledge Base|
|Buildpacks|Java, NodeJS , PHP, Python, Ruby, Static|Knowledge Base|
|[Diego](https://github.com/pivotal-gss/pcf-deigo-kb)|Loggregator, Brain, BBS, Cell, Garden|Knowledge Base|
|Iaas/Platforms|Azure, Google Compute Platform, Openstack, VSphere|Knowledge Base|
|[Pivotal Cloud Foundry](https://github.com/pivotal-gss/pcf-pivotal-cloud-foundry-kb)|Apps Manager, Ops Manager, Push Notifications|Knowledge Base|
|Security|Best Practices, CVEs|Knowledge Base|
|Services|RabbitMQ, Redis, CFOps |Knowledge Base|

### Pivotal Data Suite 

|Section|Components||
|---|---|---|
|Gemfire|Networking, Storage|Knowledge Base|
|Greenplum|Cloud Controller, TPS|Knowledge Base|
|HAWQ|Cloud Controller, TPS|Knowledge Base|


Roles
------------------------------

### Contributor

- You will only be able to switch to Simplified Workflow if:
- There is only one project being viewed by your board (to check this, look at the board's filter); and
- That project uses a JIRA workflow scheme which only has one workflow for all issue types; and

### Knowledge Management

- You will only be able to switch to Simplified Workflow if:
- There is only one project being viewed by your board (to check this, look at the board's filter); and
- That project uses a JIRA workflow scheme which only has one workflow for all issue types; and

### Subject Matter Expert (SME)

- You will only be able to switch to Simplified Workflow if:
- There is only one project being viewed by your board (to check this, look at the board's filter); and
- That project uses a JIRA workflow scheme which only has one workflow for all issue types; and

Resources
------------------------------

- [Style Guide](#overview)
- [Templates](#overview)
- [Labels](#overview)
- [Roadmap](#overview)
- [Glossary](#overview)

Bookmarks
------------------------------
- [Pivotal Cloud Foundry Knowledge Base](https://discuss.pivotal.io/hc/en-us/categories/200072648-Pivotal-CF-Knowledge-Base)
- [Pivotal Data Knowledge Base](https://discuss.pivotal.io/hc/en-us)
- [Pivotal Documentation](https://docs.pivotal.io/)
- [Pivotal Support](https://support.pivotal.io/)
- [Pivotal Network](#overview)

Read [CONTRIBUTING.md](<CONTRIBUTING.md>) for more details on contributing
documentation improvements. 
