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
