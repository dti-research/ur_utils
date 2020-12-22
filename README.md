# UR Utilities
Python utility functions for SSH into the Universal Robot Controller

# Example usage

```
robot_ip=192.168.1.100
robot_port=29999
robot_username=root

# HACK: Kill URControl process
python3 utils/ur_kill_urcontrol.py --robot-ip $robot_ip \
                                   --username $robot_username
python3 utils/ur_reboot.py --robot-ip $robot_ip \
                           --username $robot_username
python3 utils/ur_send_string_command.py -ip $robot_ip \
                                        -p $robot_port \
                                        -c "setUserRole locked"
```

For more string commands see Dashboard server interface documentation for [CB-series](https://s3-eu-west-1.amazonaws.com/ur-support-site/15690/Dashboard_Server_CB-Series.pdf) and [e-series](https://s3-eu-west-1.amazonaws.com/ur-support-site/42728/Dashboard_Server_e-Series.pdf).
