Issue: Application failed to start due to missing PORT environment variable.
Impact: Service was unavailable; application exited during startup.
Root Cause: Application code relied on th PORT environment variable without providing a default fallback value.
Detection: issue was detected when the application crashed during local execution.
Resolution: A default port value (3000) was added in the application code.
Prevention: Ensure all mandatory environment varaibles have safe defaults and validate configuration during application startup.

