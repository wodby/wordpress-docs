# Logs

All services provided with the stack configured to stream their logs to a container output. It's a common practice for docker containers. Those logs are not persistent and available until the next container restart. You can either stream logs in real-time via our dashboard or via CLI. To get logs via CLI copy `Show logs` command from `[Instance] > Stack > [Service]` and execute it on the host server of an instance. Modify `kubectl logs` command flags to your needs.

For more details see [Wodby Documentation: application logs](https://docs.wodby.com/apps/logs.html) 
