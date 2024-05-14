# TechZone Deployer Support Runbook and FAQ

## What is in this document?

This runbook is a resource for IBM Technology Zone users who are using reservations utilizing the TechZone Deployer asset to deploy IBM software, or those who want more information about what the TechZone Deployer does and where to find support or further documentation.

## What is the TechZone Deployer?

The IBM TechZone Deployer is a complementary system that works together to enable technical sellers to build and deploy IBM software quickly and easily. The goal of the TechZone Deployer is to enable Technical sellers to use the same automation technology in both TechZone and customer infrastructure.

The TechZone Deployer consists of deployment automation based on OpenShift Pipelines to package IBM Software, a catalog of available automation leveraging backstage.io, and a set of provisioning tools that enable the deployment of this automation in TechZone and customer infrastructure. If you are interested in learning more about the TechZone Deployer then see our documentation site at https://pages.github.ibm.com/skol/itz-deployer-docs/

When creating a reservation that leverages the TechZone Deployer it will create a cluster that has OpenShift Data Foundation, Red Hat OpenShift Pipelines, Red Hat OpenShift Gitops, External Secretes Operator, and the IBM Technology Zone Deployer already installed. It may also already have started a pipeline that is installing an IBM product, if that was defined in the reservation.

# FAQs and Common Errors

### My pipeline failed to complete with \***\*\_\_\*\*** error.

If the cluster for the reservation is successfuly provisioned but there is an error in the pipeline, record the error from the failing task, then try restarting the pipeline.

Steps to restart the pipeline with the same parameters it had when it failed:

1. Log into the cluster and from the OpenShift console select the "Pipelines" section from the left side menu.![pipeline section](Images/techzone-deployer-pipeline-section.png)

2. Click the inner "Pipelines" section and you should be able to see the pipeline that failed.![pipeline inner section](Images/techzone-deployer-pipeline-inner-section.png)

   Note: If you don't see any pipelines you may be in the wrong project and should change the Project: \<projname\> at the top of the screen to "All Projects"

3. Click on the three dots on the right side of the screen of the failed pipeline and select "Rerun"![pipeline section](Images/techzone-deployer-rerun-pipeline.png)

### I'm having a problem that re-running the pipeline didn't fix.

The TechZone Deployer is one piece of the reservation deployment process, and it will save you time if you contact the right people for the problem you are experiencing.

If you are having problems with the cluster in general (reservation failed to be created, storage not working correctly, nodes are not to the correct specifications, ect.), create a support case.

If there is a problem with the Pipeline that was deploying the IBM product defined by the reservation, then create a support case and be sure to include the name of the pipeline as well as any errors you can see. Information for creating a support case can be found in the ["Help" section of the IBM Technology Zone on the right side](https://techzone.ibm.com/help).

If you are having problems installing demos or running scripts from people outside of the IBM Technology Zone, then reach out to the owners of those demos or scripts. We can't help everyone debug every issue from custom resources, but if there is something wrong with the way our automation configured the IBM product it depends on, the owners of the demo/script will be the best able to work with us to fix it.

## TechZone Deployer SMEs

[David Stacy](mailto:david.stacy@ibm.com), [Cong Nguyen](mailto:cong.nguyen@au1.ibm.com), [Craig Cooper](mailto:craig.cooper@ibm.com), [David Massey](mailto:david.massey@ibm.com)
