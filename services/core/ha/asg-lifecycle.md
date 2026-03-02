![[Pasted image 20260216141203.png]]
- Custom Actions on instances during ASG actions
- .. Instance launch or Instance terminate transitions
- Control the status of actions

Lifecycle hooks enable you to perform custom actions by _pausing_ instances as an Auto Scaling group launches or terminates them. When an instance is paused, it remains in a wait state either until you complete the lifecycle action using the **complete-lifecycle-action** command or the `CompleteLifecycleAction` operation, or until the timeout period ends (one hour by default).