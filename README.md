nodejs-ex demo. Just for academical purposes

This directory contains a Jenkinsfile which can be used to build nodejs-ex using an OpenShift build pipeline.

To do this, run:

# create the nodejs example as usual
[source,bash]
----
oc new-app https://github.com/sclorg/nodejs-ex.git
----

# now create the pipeline build controller from the openshift/pipeline subdirectory
[source,bash]
----
oc new-app https://github.com/alexbarbosa1989/nodejs-ex.git --context-dir=openshift/pipeline --name nodejs-ex-pipeline
---- 

== This step creates an ephemeral jenkins builconfing and deploy a jenkins pod inside the project
