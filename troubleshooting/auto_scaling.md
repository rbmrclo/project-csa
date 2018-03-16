# Auto Scaling Troubleshooting

##### An Auto Scaled instance continue to start and stop (or create/terminate) in short intervals

- The scale-up and scale-down thresholds may be too close to each other. Either
  raise the scale-up threshold or lower the scale-down threshold.

##### Auto Scaling does not occur even though scaling policies are configured correctly

- The "max" number of instances set in the auto scaling group may have been reached.
