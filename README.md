#CPU usage script:
This script shows the percentage of CPU usage in real-time.
#!/bin/bash
while true; do
  usage=$(top -bn1 | grep "Cpu(s)" | awk '{print $2 + $4}')
  echo "CPU usage: $usage%"
  sleep 1
done

