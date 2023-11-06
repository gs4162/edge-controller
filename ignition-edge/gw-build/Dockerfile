# Use the Inductive Automation Ignition base image with a specific version
FROM inductiveautomation/ignition:8.1.33

# Update packages and install Git (Uncomment if Git is needed)
#RUN apt-get update && apt-get install -y git
# Switch to root to change file ownership and permissions
USER root


# Copy your modules
COPY *.modl /usr/local/bin/ignition/user-lib/modules/
# Adjust the ownership to the ignition user and group
RUN chown -R 2003:2003 /usr/local/bin/ignition/user-lib/modules/
# Adjust permissions if necessary, 775 for directories and 664 for files is a common setting
RUN find /usr/local/bin/ignition/user-lib/modules/ -type d -exec chmod 775 {} \;
RUN find /usr/local/bin/ignition/user-lib/modules/ -type f -exec chmod 664 {} \;


# Copy the MariaDB JDBC driver into the Ignition drivers folder
COPY *.jar /usr/local/bin/ignition/user-lib/jdbc/
# Adjust the ownership for JDBC drivers
RUN chown -R 2003:2003 /usr/local/bin/ignition/user-lib/jdbc/
# Adjust permissions if necessary, 775 for directories and 664 for files is a common setting
RUN find /usr/local/bin/ignition/user-lib/jdbc/ -type d -exec chmod 775 {} \;
RUN find /usr/local/bin/ignition/user-lib/jdbc/ -type f -exec chmod 664 {} \;

# docker build -t mhm-edge-gateway-standard .
# docker build -t mhm-edge-gateway-edge .

