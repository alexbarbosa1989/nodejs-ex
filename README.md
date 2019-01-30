nodejs-ex demo. Just for academical purposes

This directory contains a Jenkinsfile which can be used to build nodejs-ex using an OpenShift build pipeline.

To do this, run:

# create the nodejs example as usual

> oc new-app https://github.com/sclorg/nodejs-ex.git

# now create the pipeline build controller from the openshift/pipeline subdirectory

> oc new-app https://github.com/alexbarbosa1989/nodejs-ex.git --context-dir=openshift/pipeline --name nodejs-ex-pipeline
 

(Last step creates a jenkins builconfing and deploy an ephemeral jenkins pod inside the project)
