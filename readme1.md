# Cloud Computing Experiments

## Experiment 1: Installing VirtualBox or VMware with Different OS Flavours

### Aim
To install VirtualBox or VMware Workstation with different Linux or Windows OS on top of Windows 7 or 8.

### Procedure
#### Install VirtualBox:
1. Download and install the VirtualBox executable.
2. Follow the installation wizard until completion.

#### Import OpenNebula Sandbox:
1. Open VirtualBox, select **File > Import Appliance**, and import `OpenNebula-Sandbox-5.0.ova`.
2. Configure USB settings to USB 1.1 in the VM settings.
3. Start the VM and log in as root (password: `opennebula`).

#### Create Virtual Machines in OpenNebula:
1. Access `http://localhost:9869` in a browser.
2. Log in as `oneadmin` (password: `opennebula`).
3. Navigate to **Instances > VMs**, and create new virtual machines with specified configurations.

### Applications
Cloud computing enables scalability and efficient resource utilization, benefiting platforms like Amazon, LinkedIn, and Facebook.

### Result
Virtual machines were successfully created and managed in the virtualized environment.

---

## Experiment 2: Running C Programs in a Virtual Machine

### Aim
To install a C compiler and execute simple C programs in a virtualized environment.

### Procedure
#### Import and Start the VM:
1. Import `ubuntu_gt6.ova` in VirtualBox.
2. Start the VM and log in (username: `dinesh`, password: `99425`).

#### Write and Compile a C Program:
1. Open the terminal, navigate to `/opt/axis2/axis2-1.7.3/bin`, and create a new C file using `gedit`.
2. Write a program, compile it with `gcc filename.c`, and run using `./a.out`.

### Applications
This environment allows for seamless execution of C programs, aiding in software development and testing.

### Result
C programs were successfully written, compiled, and executed.

---

## Experiment 3: Creating Web Applications with Google App Engine

### Aim
To install Google App Engine (GAE), create a Hello World application, and deploy it.

### Procedure
#### Setup:
1. Install Google Plugin for Eclipse and configure the GAE SDK.

#### Develop Application:
1. Create a new web application project in Eclipse.
2. Edit the auto-generated `appengine-web.xml` file with your application ID.

#### Test Locally and Deploy:
1. Run the application locally using Eclipse.
2. Deploy the application via the GAE deploy button, making it accessible at `http://<app-id>.appspot.com`.

### Applications
GAE simplifies web application development with scalability and deployment efficiency.

### Result
The Hello World application was successfully created and deployed.

---

## Experiment 4: CloudSim Simulation and Custom Scheduling Algorithm

### Aim
To simulate a cloud scenario using CloudSim and implement a custom scheduling algorithm.

### Procedure
#### Setup CloudSim:
1. Download and integrate CloudSim into Eclipse.
2. Initialize the library and create required entities like data centers, brokers, and virtual machines.

#### Custom Scheduling Algorithm:
1. Define and integrate the scheduling algorithm into the simulation.
2. Submit the tasks (cloudlets) and run the simulation.

### Applications
Simulating cloud scenarios helps evaluate scheduling algorithms for resource optimization.

### Result
The simulation successfully executed a custom scheduling algorithm.

---

## Experiment 5: Using GAE Launcher for Web Applications

### Aim
To use the GAE Launcher to develop and deploy web applications.

### Procedure
#### Setup Environment:
1. Install GAE Launcher and create a new application project.

#### Deploy Application:
1. Test the application locally and deploy to GAE with a registered application ID.

### Applications
GAE Launcher streamlines the development and deployment of scalable web applications.

### Result
Web applications were successfully created and deployed using GAE Launcher.

---

## Experiment 6: Installing HDFS and Executing File Management Commands

### Aim
To install the Hadoop Distributed File System (HDFS) and execute file management commands to manage distributed data.

### Procedure
#### Install Hadoop:
1. Download Hadoop binaries and extract them into a directory (`/usr/local/hadoop`).
2. Configure `core-site.xml`, `hdfs-site.xml`, and `mapred-site.xml` for single-node operation.
3. Format the Hadoop filesystem with `hadoop namenode -format`.

#### Start HDFS:
1. Start the Hadoop Distributed File System with `start-dfs.sh`.

#### Execute File Management Commands:
1. Use commands like `hdfs dfs -put <local_file> <hdfs_directory>` to upload files.
2. View files in HDFS with `hdfs dfs -ls <directory>`.
3. Retrieve files with `hdfs dfs -get <hdfs_file> <local_directory>`.

### Applications
HDFS supports scalable and distributed storage for big data applications, essential for platforms like Yahoo and Facebook.

### Result
HDFS was successfully installed, and file management commands were executed.

---

## Experiment 7: Configuring MapReduce and Executing WordCount Program

### Aim
To configure Hadoop MapReduce and execute a sample WordCount program.

### Procedure
#### Setup MapReduce:
1. Ensure Hadoop is correctly installed and configured.
2. Configure `mapred-site.xml` for running the MapReduce framework.

#### Run WordCount Program:
1. Place an input text file into HDFS using `hdfs dfs -put`.
2. Execute the WordCount program with the command:
   ```
   hadoop jar hadoop-mapreduce-examples.jar wordcount <input_dir> <output_dir>
   ```

#### Check Results:
1. Use `hdfs dfs -cat <output_dir>/part-r-00000` to view the output.

### Applications
MapReduce simplifies parallel data processing, aiding in large-scale data analytics tasks like log analysis and indexing.

### Result
The WordCount program executed successfully, processing input data and generating word frequency counts.

---

## Experiment 8: Using Eucalyptus for Private Cloud Implementation

### Aim
To install and configure Eucalyptus for creating and managing a private cloud environment.

### Procedure
#### Install Eucalyptus:
1. Install Eucalyptus packages on a CentOS or Ubuntu system.
2. Configure Eucalyptus components like Cloud Controller (CLC), Walrus, Cluster Controller (CC), and Node Controller (NC).

#### Setup Networking:
1. Configure networking with managed mode for the private cloud.

#### Create Cloud Users and Instances:
1. Use Eucalyptus commands to create user accounts and allocate resources.
2. Launch instances with `euca-run-instances` command.

#### Manage Instances:
1. Use commands like `euca-describe-instances` to monitor instances and `euca-terminate-instances` to stop them.

### Applications
Eucalyptus facilitates private cloud implementation, enabling organizations to manage resources securely and efficiently.

### Result
Eucalyptus was successfully configured, and a private cloud environment was implemented and tested.
