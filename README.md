1. Deployment Resource
Purpose: Manages a set of replicas of a pod, ensuring that the specified number of pods are running at any given time.

2. ReplicaSet Resource
Purpose: Ensures that a specified number of pod replicas are running at any time. Usually managed by a Deployment.

3. DaemonSet Resource
Purpose: Ensures that a copy of a pod runs on all (or some) nodes in the cluster. Ideal for system-level services or monitoring agents.

4. Job Resource
Purpose: Creates one or more pods and ensures that a specified number of them successfully terminate. Useful for batch processing.

5. CronJob Resource
Purpose: Creates Jobs on a time-based schedule. Similar to Unix cron jobs.

6. StatefulSet Resource
Purpose: Manages stateful applications by providing stable network identities and persistent storage.
