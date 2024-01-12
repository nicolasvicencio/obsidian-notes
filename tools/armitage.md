#gui 
## Solution

**Step 1:** Open the lab link to access the Kali GUI instance

**Step 2:** Identify the target IP address

Before we get started, you will need to obtain the IP address of **Victim Machine 1** within the lab environment.

This lab will provide you with the target IP addresses of both **Victim Machine 1** and **Victim Machine 2** in a leafpad window when you first access the lab as shown in the following screenshot.

![1](https://assets.ine.com/content/ptp/AlexisAhmed/VOD-4377/LAB-3868/1.png)

**Note:** Your target IP address will be different, so make sure to substitute the IP shown in the commands below with the one in your lab.

**Step 3:** Port scanning & enumeration with Armitage

Before starting up Armitage, you will need to start the **postgresql** database service, this can be done by running the following command:

**Command:**

```
service postgresql start
```

We can start up Armitage by running the following command:

**Command:**

```
armitage
```

After starting up Armitage, you will be prompted to connect to the MSF database as shown in the following screenshot.

![2](https://assets.ine.com/content/ptp/AlexisAhmed/VOD-4377/LAB-3868/2.png)

After connecting to the MSF database, Armitage will open up as shown in the following screenshot.

![3](https://assets.ine.com/content/ptp/AlexisAhmed/VOD-4377/LAB-3868/3.png)

We can get started by adding the IP address of **Victim Machine 1**, this can be done clicking on **Hosts** on the toolbar and on **Add Hosts** in the sub-menu as shown in the following screenshot.

![4](https://assets.ine.com/content/ptp/AlexisAhmed/VOD-4377/LAB-3868/4.png)

You will then be prompted to add the IP address of the target system as shown in the following screenshot.

![5](https://assets.ine.com/content/ptp/AlexisAhmed/VOD-4377/LAB-3868/5.png)

After adding the IP address of **Victim Machine 1**, the system will be added to the top panel as shown in the following screenshot.

![6](https://assets.ine.com/content/ptp/AlexisAhmed/VOD-4377/LAB-3868/6.png)

We can perform a port scan on the target system by right-clicking on the system and clicking on **Scan** as shown in the following screenshot.

![7](https://assets.ine.com/content/ptp/AlexisAhmed/VOD-4377/LAB-3868/7.png)

This will begin the port scan on the target system, after which the results will be displayed in the bottom output pane as shown in the following screenshot.

![8](https://assets.ine.com/content/ptp/AlexisAhmed/VOD-4377/LAB-3868/8.png)

We can also perform an Nmap port scan on the target system by clicking on the **hosts** menu in the toolbar and the **Nmap Scan** option in the submenu as shown in the following screenshot.

![9](https://assets.ine.com/content/ptp/AlexisAhmed/VOD-4377/LAB-3868/9.png)

You will then be prompted to add the IP address of the target system as shown in the following screenshot.

![10](https://assets.ine.com/content/ptp/AlexisAhmed/VOD-4377/LAB-3868/10.png)

This will begin the Nmap port scan, after which, the results will be displayed in the output pane at the bottom as shown in the following screenshot.

![11](https://assets.ine.com/content/ptp/AlexisAhmed/VOD-4377/LAB-3868/11.png)

You can now view the open ports and services running on the target system by right-clicking on the system and clicking on **services** as shown in the following screenshot.

![12](https://assets.ine.com/content/ptp/AlexisAhmed/VOD-4377/LAB-3868/12.png)

As shown in the following screenshot, this will display the list of open ports and services discovered during the port scan.

![13](https://assets.ine.com/content/ptp/AlexisAhmed/VOD-4377/LAB-3868/13.png)

## Conclusion

In this lab, we explored the process of performing port scanning and enumeration with Armitage.