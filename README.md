## Experiment 1: Install VirtualBox / VMware Workstation with Different Flavours of Linux or Windows OS on Top of Windows 7 or 8

### Aim
To install VirtualBox / VMware Workstation with different flavours of Linux or Windows OS on top of Windows 7 or 8.

### Steps
1. **Install VirtualBox:**
   - Download the VirtualBox installer (exe file).
   - Double-click the downloaded exe file and click **Next**.
   - Click **Next** again.
   - Click **Next** once more.
   - Click **Yes** to allow changes.
   - Click **Install** to begin the installation.
   - Once the installation is complete, the VirtualBox icon will appear on the desktop.

2. **Import OpenNebula Sandbox:**
   - Open VirtualBox.
   - Go to **File** → **Import Appliance**.
   - Browse and select the `OpenNebula-Sandbox-5.0.ova` file.
   - Go to **Settings**, select **USB**, and choose **USB 1.1**.
   - Start the OpenNebula virtual machine.
   - Login with the username: `root` and password: `opennebula`.

3. **Create Virtual Machine Using OpenNebula:**
   - Open a browser and navigate to `localhost:9869`.
   - Login using the credentials: `username: oneadmin`, `password: opennebula`.
   - Click on **Instances**, then select **VMs**.
   - Follow these steps to create a virtual machine:
     - Expand the `+` symbol.
     - Select **User**: `oneadmin`.
     - Enter the VM name, number of instances, and CPU configuration.
     - Click **Create**.
     - Repeat steps for creating additional VMs.

### Applications
Cloud computing has various applications in today’s network world. Many search engines and social websites, such as Amazon, Hotmail, Facebook, and LinkedIn, use cloud computing. The advantages of cloud computing, in terms of scalability, include:
- Reduced risk
- Low-cost testing
- Ability to segment the customer base
- Auto-scaling based on application load

### Result
The procedure to install and run virtual machines with different configurations was successfully completed.


## Experiment 2: Install a C Compiler in the Virtual Machine Created Using VirtualBox and Execute Simple Programs

### Aim
To install a C compiler in the virtual machine created using VirtualBox and execute simple programs.

### Steps

1. **Import the .OVA File:**
   - Open VirtualBox.
   - Go to **File** → **Import Appliance**.
   - Browse and select the `ubuntu_gt6.ova` file.
   - Go to **Settings**, select **USB**, and choose **USB 1.1**.
   - Start the `ubuntu_gt6` virtual machine.
   - Login using the credentials: `username: dinesh`, `password: 99425`.

2. **Run a C Program:**
   - Open the terminal in the virtual machine.
   - Type `cd /opt/axis2/axis2-1.7.3/bin` and press **Enter**.
   - Type `gedit hello.c` to create a new C program file.
   - Write your C program in the `hello.c` file.
   - Compile the program using `gcc hello.c`.
   - Run the compiled program with `./a.out` to see the output.
   
   - Alternatively, to create and run another C program:
     - Type `cd /opt/axis2/axis2-1.7.3/bin` and press **Enter**.
     - Type `gedit first.c` to create the program file.
     - Write your C program.
     - Compile using `gcc first.c` and run it with `./a.out` to display the output.

### Applications
This setup is useful for running C programs in a grid environment, allowing for easy execution and testing.

### Result
The simple C programs were executed successfully in the virtual machine.

## Experiment 3: Install Google App Engine. Create Hello World App and Other Simple Web Applications Using Python/Java

### Aim
To install Google App Engine, create a Hello World app, and other simple web applications using Python/Java.

### Steps

1. **Install Google Plugin for Eclipse:**
   - Follow the guide to install the **Google Plugin for Eclipse**. 
   - If you install the **Google App Engine Java SDK** together with the plugin, proceed to step 2.
   - Otherwise, download the **Google App Engine Java SDK** and extract it.

2. **Create New Web Application Project:**
   - In Eclipse, click on the **Google** icon in the toolbar and select **New Web Application Project**.
   - Deselect the **Google Web Toolkit** option.
   - Link your GAE Java SDK by clicking the **configure SDK** link.
   - Click **Finish**. The Google Plugin for Eclipse will automatically generate a sample project.

3. **Hello World:**
   - Review the generated project directory. The directory structure is as follows:
     ```
     HelloWorld/
     ├── src/
     │   └── ... Java source code ...
     ├── META-INF/
     │   └── ... other configuration ...
     ├── war/
     │   └── ... JSPs, images, data files ...
     ├── WEB-INF/
     │   └── ... app configuration ...
     ├── lib/
     │   └── ... JARs for libraries ...
     └── classes/
         └── ... compiled classes ...
     ```
   - The project will also contain a file named `appengine-web.xml` which is required for Google App Engine to run and deploy the application.
   - The content of the `appengine-web.xml` file:
     ```xml
     <?xml version="1.0" encoding="utf-8"?>
     <appengine-web-app xmlns="http://appengine.google.com/ns/1.0">
       <application></application>
       <version>1</version>
       <!-- Configure java.util.logging -->
       <system-properties>
         <property name="java.util.logging.config.file" value="WEB-INF/logging.properties"/>
       </system-properties>
     </appengine-web-app>
     ```

4. **Run the Application Locally:**
   - Right-click on the project and select **Run as > Web Application**.
   - In the Eclipse console, you will see:
     ```
     INFO: The server is running at http://localhost:8888/
     INFO: The admin console is running at http://localhost:8888/_ah/admin
     ```
   - Access the URL `http://localhost:8888/` to see the output, and the Hello World servlet at `http://localhost:8888/helloworld`.

5. **Deploy to Google App Engine:**
   - Register an account on [Google App Engine](https://appengine.google.com/) and create an application ID.
   - In the `appengine-web.xml` file, update the `<application>` tag with your created application ID:
     ```xml
     <?xml version="1.0" encoding="utf-8"?>
     <appengine-web-app xmlns="http://appengine.google.com/ns/1.0">
       <application>mkyong123</application>
       <version>1</version>
       <!-- Configure java.util.logging -->
       <system-properties>
         <property name="java.util.logging.config.file" value="WEB-INF/logging.properties"/>
       </system-properties>
     </appengine-web-app>
     ```
   - To deploy, click the **GAE deploy** button in the toolbar.
   - Sign in with your Google account and click the **Deploy** button.
   - Once deployed, the Hello World web application will be available at the URL:
     ```
     http://mkyong123.appspot.com/
     ```

### Result
The simple web application was created and successfully deployed to Google App Engine.

## Experiment 4: Simulate a Cloud Scenario Using CloudSim and Run a Scheduling Algorithm That is Not Present in CloudSim

### Aim
To simulate a cloud scenario using CloudSim and run a scheduling algorithm that is not present in CloudSim.

### Steps

#### How to Use CloudSim in Eclipse:
CloudSim is written in Java. Basic Java programming knowledge and an understanding of cloud computing concepts are required to use CloudSim. It is a library and does not need to be installed separately. You can unpack the downloaded package into any directory, add it to the Java classpath, and it is ready to be used.

Follow these steps to use CloudSim in Eclipse:

1. **Download CloudSim Installable Files:**
   - Download CloudSim from [CloudSim Downloads](https://code.google.com/p/cloudsim/downloads/list) and unzip the files.

2. **Open Eclipse:**
   - Launch Eclipse IDE.

3. **Create a New Java Project:**
   - Go to `File -> New -> Java Project` to create a new project.

4. **Import CloudSim Project into the New Java Project:**
   - Import the unpacked CloudSim project into your newly created Java project.

5. **Initialize CloudSim:**
   - The first step is to initialize the CloudSim library with the following code:
     ```java
     CloudSim.init(num_user, calendar, trace_flag);
     ```

6. **Create Data Centers:**
   - Data centers are the resource providers in CloudSim. To create a data center, you need to define the `DatacenterCharacteristics` object that stores properties such as architecture, OS, machines, allocation policy, and price. Example:
     ```java
     Datacenter datacenter9883 = new Datacenter(name, characteristics, new VmAllocationPolicySimple(hostList), s);
     ```

7. **Create a Broker:**
   - Create a broker using the `createBroker()` method:
     ```java
     DatacenterBroker broker = createBroker();
     ```

8. **Create a Virtual Machine:**
   - Create a virtual machine with specific parameters such as ID, MIPS, number of CPUs, RAM, bandwidth, storage, and cloudlet scheduler:
     ```java
     Vm vm = new Vm(vmid, brokerId, mips, pesNumber, ram, bw, size, vmm, new CloudletSchedulerTimeShared());
     ```

9. **Submit the VM List to the Broker:**
   - Submit the list of VMs to the broker:
     ```java
     broker.submitVmList(vmlist);
     ```

10. **Create a Cloudlet:**
    - Define a cloudlet with parameters like length, file size, output size, and utilization model:
      ```java
      Cloudlet cloudlet = new Cloudlet(id, length, pesNumber, fileSize, outputSize, utilizationModel, utilizationMode);
      ```

11. **Submit the Cloudlet List to the Broker:**
    - Submit the list of cloudlets to the broker:
      ```java
      broker.submitCloudletList(cloudletList);
      ```

#### Sample Output from the Existing Example:

### Result
The simulation was successfully executed with CloudSim. The scheduling algorithm was run, and the cloud scenario was simulated as expected.

## Experiment 5: Use GAE Launcher to Launch Web Applications

### Aim
To use the GAE (Google App Engine) Launcher to create and launch web applications.

### Steps

1. **Creating Your First Application:**
   - Create a folder for your Google App Engine applications, for example:
     `C:\Documents and Settings\csev\Desktop\apps`.
   - Inside this folder, create a sub-folder named `ae--01--trivial`, for example:
     `C:\Documents and Settings\csev\Desktop\apps\ae--01--trivial`.

2. **Writing the `app.yaml` File:**
   - Using a text editor like [JEdit](http://www.jedit.org), create a file named `app.yaml` in the `ae--01--trivial` folder.
   - Add the following content to the file:
     ```yaml
     application: ae-01-trivial
     version: 1
     runtime: python 
     api_version: 1
     handlers:
     - url: /.*
       script: index.py
     ```
   - **Note:** Type these lines manually to avoid formatting issues.

3. **Writing the `index.py` File:**
   - Create a file named `index.py` in the same `ae--01--trivial` folder.
   - Add the following Python code:
     ```python
     print 'Content-Type: text/plain'
     print ' '
     print 'Hello there Chuck'
     ```

4. **Starting the Application:**
   - Open the **Google App Engine Launcher**.
   - Use the `File → Add Existing Application` command and navigate to the `ae--01--trivial` folder.
   - Select the application, and use the launcher to control the application (start/stop).

5. **Dealing with Errors:**
   - Errors in the `app.yaml` file:
     - The application will not start, and the launcher will display a yellow icon.
     - View the log for details, such as indentation errors.
   - Errors in the `index.py` file:
     - A Python traceback error will appear in your browser.
     - Fix the file and refresh the browser; no need to restart the server.

6. **Shutting Down the Server:**
   - To stop the application, select it in the launcher and press the **Stop** button.

### Result
Thus, a Google App Engine web application was successfully created and launched.


## Experiment 6: File Transfer Between Virtual Machines

### Aim
To transfer files from one virtual machine (VM) to another.

### Steps
1. Enable shared clipboard and drag-and-drop (set to bidirectional) in VM settings.
2. Install Guest Additions on both virtual machines.
3. Set up shared folders between the two virtual machines.
4. Ensure the receiving VM has an active SSH server for file transfer.
5. Mount file systems via NFS or SSHFS, or use Samba for shared directories.
6. Migrate VMs using OpenNebula as detailed below.

### Procedure
1. **Using Shared Clipboard and Drag-and-Drop:**
   - Enable shared clipboard and drag-and-drop (set to bidirectional) in VM settings.
   - Install Guest Additions on both virtual machines.
   - Copy from the guest OS, paste on the host OS, and then paste from the host OS to the second guest OS.

2. **Using Shared Folders:**
   - Set up shared folders between the two virtual machines using Guest Additions.
   - Files placed in the shared folder from either machine are visible on the other.

3. **Using SSH for File Transfer:**
   - Ensure the receiving VM has an active SSH server (install with `sudo apt-get install openssh-server` on Linux).
   - Use `scp` or similar tools from the sending VM to transfer files.

4. **Using NFS or SSHFS for File Sharing:**
   - Mount part of the file system of one VM on another via NFS or SSHFS, or use Samba for shared file directories.

5. **VM Migration in OpenNebula:**
   - Open a browser and navigate to `localhost:9869`.
   - Login using the credentials: `username: oneadmin`, `password: opennebula`.
   - Follow these steps to migrate VMs:
     - Go to **Infrastructure** → **Clusters**, and select the cluster.
     - Under **Host**, select the hosts, **Vnets**, and **Datastores**, and then configure.
     - To add a new host, click the `+` symbol, name the host, and click **Create**.
     - Go to **Instances** → **VMs**, select the VM to migrate, and click the 8th icon for the dropdown.
     - Select **Migrate**, choose the target host, and click **Migrate**.

### Applications
- Easily transfer files between virtual machines or migrate VMs between hosts.

### Result
The file transfer between VMs and VM migration were successfully completed.

# Experiment 7: Procedure to Launch Virtual Machine Using TryStack

## Aim
To launch a virtual machine using TryStack, an OpenStack demo platform.

## Steps

### Step 1: Create Network
1. Go to **Network → Networks → Create Network**.
2. Enter a **Network Name** (e.g., `internal`) and click **Next**.
3. Set **Network Address** (e.g., `192.168.1.0/24`), **IP Version** as IPv4, and click **Next**.
4. Add **DNS Name Servers** as `8.8.8.8` and click **Create**.

### Step 2: Create Instance
1. Navigate to **Compute → Instances → Launch Instance**.
2. Fill in **Instance Name** (e.g., `Ubuntu 1`), select **Flavor** (e.g., `m1.medium`), and choose **Boot from Image** (e.g., `Ubuntu 14.04`).
3. Import a **Key Pair** (use `~/.ssh/id_rsa.pub` for the public key).
4. Select the created **Network** (e.g., `internal`) and click **Launch**.

### Step 3: Create Router
1. Go to **Network → Routers → Create Router**. Name it (e.g., `router1`).
2. Set the **Gateway** to `external` and add the subnet (`internal`) as an interface.
3. View the topology under **Network → Network Topology**.

### Step 4: Assign Floating IP
1. In **Compute → Instances**, click **More → Associate Floating IP** for an instance.
2. Allocate and associate a floating IP from the `external` pool.

### Step 5: Configure Security
1. Go to **Compute → Access & Security → Security Groups → Manage Rules**.
2. Add rules to allow:
   - ICMP (Ping),
   - HTTP (Port 80),
   - SSH (Port 22).

### Step 6: Connect to Instance
1. Use the floating IP to SSH into the instance (e.g., `ssh ubuntu@<floating-ip>`).

## Result
A virtual machine was successfully launched using TryStack.

## Experiment 8: Install Hadoop Single Node Cluster and Run Simple Applications Like WordCount

### Aim
To install Hadoop single node cluster and run simple applications like WordCount.

### Steps

1. **Install Java:**
   - Download the Java 8 package and save it in your home directory.
   - Extract the Java tar file using the command:
     ```
     tar -xvf jdk-8u101-linux-i586.tar.gz
     ```

2. **Install Hadoop:**
   - Download the Hadoop 2.7.3 package using the command:
     ```
     wget https://archive.apache.org/dist/hadoop/core/hadoop-2.7.3/hadoop2.7.3.tar.gz
     ```
   - Extract the Hadoop tar file:
     ```
     tar -xvf hadoop-2.7.3.tar.gz
     ```

3. **Set Environment Variables:**
   - Add the Hadoop and Java paths in the `.bashrc` file:
     ```
     vi .bashrc
     ```
   - Save and close the file.
   - Apply the changes to the current terminal:
     ```
     source .bashrc
     ```
   - Verify the installation by checking the Java and Hadoop versions:
     ```
     java -version
     hadoop version
     ```

4. **Edit Hadoop Configuration Files:**
   - Navigate to the Hadoop configuration directory:
     ```
     cd hadoop-2.7.3/etc/hadoop/
     ls
     ```
   - **Edit core-site.xml** to configure the NameNode:
     ```
     vi core-site.xml
     ```
   - **Edit hdfs-site.xml** to configure the HDFS daemons:
     ```
     vi hdfs-site.xml
     ```
   - **Edit mapred-site.xml** to configure MapReduce:
     - If the file does not exist, create it:
       ```
       cp mapred-site.xml.template mapred-site.xml
       vi mapred-site.xml
       ```
   - **Edit yarn-site.xml** to configure ResourceManager and NodeManager:
     ```
     vi yarn-site.xml
     ```
   - **Edit hadoop-env.sh** to add the Java path:
     ```
     vi hadoop-env.sh
     ```

5. **Format the NameNode:**
   - Format the HDFS via the NameNode:
     ```
     cd hadoop-2.7.3
     bin/hadoop namenode -format
     ```

6. **Start Hadoop Daemons:**
   - Navigate to the `sbin` directory and start all daemons:
     ```
     cd hadoop-2.7.3/sbin
     ./start-all.sh
     ```
   - Alternatively, start the services individually:
     - Start NameNode:
       ```
       ./hadoop-daemon.sh start namenode
       ```
     - Start DataNode:
       ```
       ./hadoop-daemon.sh start datanode
       ```
     - Start ResourceManager:
       ```
       ./yarn-daemon.sh start resourcemanager
       ```
     - Start NodeManager:
       ```
       ./yarn-daemon.sh start nodemanager
       ```
     - Start JobHistoryServer:
       ```
       ./mr-jobhistory-daemon.sh start historyserver
       ```

7. **Check the Daemons:**
   - Verify that all Hadoop services are running:
     ```
     jps
     ```

8. **Access the NameNode Interface:**
   - Open your browser and go to:
     ```
     localhost:50070/dfshealth.html
     ```

### Applications
Hadoop can be used for various big data applications such as distributed storage, processing, and running MapReduce jobs like WordCount. It is widely used in industries requiring large-scale data processing.

### Result
The Hadoop single node cluster was installed successfully, and simple applications, such as WordCount, were executed without issues.
