1. Deployment Resource
Purpose: Manages a set of replicas of a pod, ensuring that the specified number of pods are running at any given time.

apiVersion: Specifies the API version used to create the Deployment.
kind: Defines the type of resource; in this case, a Deployment.
metadata.name: Names the Deployment.
spec.replicas: Sets the desired number of pod replicas.
spec.selector.matchLabels: Labels used to select the pods managed by this Deployment.
spec.template.metadata.labels: Labels applied to the pods.
spec.template.spec.containers: Defines the container(s) within the pod, including the image and port settings.

2. ReplicaSet Resource
Purpose: Ensures that a specified number of pod replicas are running at any time. Usually managed by a Deployment.

apiVersion: Specifies the API version used to create the ReplicaSet.
kind: Defines the type of resource; in this case, a ReplicaSet.
metadata.name: Names the ReplicaSet.
spec.replicas: Sets the desired number of pod replicas.
spec.selector.matchLabels: Labels used to select the pods managed by this ReplicaSet.
spec.template.metadata.labels: Labels applied to the pods.
spec.template.spec.containers: Defines the container(s) within the pod, including the image and port settings.

3. DaemonSet Resource
Purpose: Ensures that a copy of a pod runs on all (or some) nodes in the cluster. Ideal for system-level services or monitoring agents.

apiVersion: Specifies the API version used to create the DaemonSet.
kind: Defines the type of resource; in this case, a DaemonSet.
metadata.name: Names the DaemonSet.
spec.selector.matchLabels: Labels used to select the pods managed by this DaemonSet.
spec.template.metadata.labels: Labels applied to the pods.
spec.template.spec.containers: Defines the container(s) within the pod, including the image and port settings.

4. Job Resource
Purpose: Creates one or more pods and ensures that a specified number of them successfully terminate. Useful for batch processing.

apiVersion: Specifies the API version used to create the Job.
kind: Defines the type of resource; in this case, a Job.
metadata.name: Names the Job.
spec.template.spec.containers: Defines the container(s) within the pod, including the image and command to run.
spec.template.spec.restartPolicy: Policy to restart the pod; set to OnFailure to only restart on failure.

5. CronJob Resource
Purpose: Creates Jobs on a time-based schedule. Similar to Unix cron jobs.

apiVersion: Specifies the API version used to create the CronJob.
kind: Defines the type of resource; in this case, a CronJob.
metadata.name: Names the CronJob.
spec.schedule: Cron schedule for running the Job.
spec.jobTemplate.spec.template.spec.containers: Defines the container(s) within the pod, including the image and command to run.
spec.jobTemplate.spec.template.spec.restartPolicy: Policy to restart the pod; set to OnFailure to only restart on failure.

6. StatefulSet Resource
Purpose: Manages stateful applications by providing stable network identities and persistent storage.

apiVersion: Specifies the API version used to create the StatefulSet.
kind: Defines the type of resource; in this case, a StatefulSet.
metadata.name: Names the StatefulSet.
spec.serviceName: The name of the headless service that controls the StatefulSet.
spec.replicas: Number of pod replicas.
spec.selector.matchLabels: Labels used to select the pods managed by this StatefulSet.
spec.template.metadata.labels: Labels applied to the pods.
spec.template.spec.containers: Defines the container(s) within the pod, including the image and port settings.
spec.volumeClaimTemplates: Defines storage volumes for each pod, including access modes and storage size.