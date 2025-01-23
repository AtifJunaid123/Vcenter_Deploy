## change to Desktop Directory
    cd ~/Desktop
## Create Folder  
    sudo mkdir Vcenter
## change to Folder
    cd Vcenter
## Download the Vcenter for Internet   
   wget https://mirror.mahanserver.net/VMware/VCenter/7.0.0/VMware-VCSA-all-7.0.0-16189094.iso
## Deploy Vcenter using this Steps:

1-  Mount the VCSA .ISO you downloaded
   ![How to Mount](Pic/Mount_vcsa7u3.png)

2- Open the folder called “vcsa-ui-installer”
   ![vcsa-ui-installer Folder](Pic/open_ui_installer7u3.png)

3- Choose the correct folder depending on the operating system you’re deploying the VCSA from. Since I am using ubuntu 22.04 to deploy VCSA, I will select “lin64” folder.
   ![lin64 Folder](Pic/os_choice_7u3.png)

4-  open Terminal and Run "installer" file
    ![How to run Exe on Terminal](Pic/installer.png)

5- Choose “Install” and click “next” on the introduction screen.
    ![How to “Install”](Pic/choose_install_7u3.png)

6- Accept the End user license agreement and click next
    ![Accept Agreement”](Pic/agreement.png)

7- Specify target where vCenter server appliance will be deployed. The target can be ESXi host or existing vCenter server. In this demo I will be using a standalone ESXi host. Once you have completed form, click “Next” to continue.
    ![How to add host for vcenter”](Pic/standalone%20ESXi%20host.png)
   **Note: A Certificate Warning might appear. Click “Yes” to continue**

8- Specify the VM settings for the vCenter Server. Click “Next” to continue.
    VM Name - Name of the Virtual Machine
    Set root password - Provide a Password
    Confirm root password - Confirm the root password
    ![VM settings for the vCenter Server”](Pic/Setup-vCenter-Server-VM.png)

9- Select the VCSA deployment size for your enviroment. In this demo I will be using “Small” for deployment size and “Default” for Storage Size. Click “Next” to continue.
     ![Deployment Size”](Pic/vcsa_depoyment_size_7u3.png)

10- Select Datastore to idenifty the storage location for the VCSA. Click “Next” to continue.    
    ![Datastore to idenifty the storage location”](Pic/select_datastore_7u3.png)

11- Configure the network settings of the VCSA. Click “Next” to continue.
        ![Configure the network settings”](Pic/vcsa_network_settings_7u3.png)

    1- Network - Select the port group to be used for the VCSA
    2- IP Version - Select either IPv4 or IPv6
    3- IP assignment - Select either Static or dhcp
    4- FQDN - Provide the fully qualified domain name (FQDN) or IP address of the VCSA. (vcentername.domain.com or x.x.x.x) 
    5- IP Address - Provide the IP address of the VCSA (x.x.x.x)

    6- Subnet Mask or Prefix Length - Provide the Subnet mask or Prefix Length of the VCSA network. (x.x.x.x or xx)
    7- Default Gateway - Provide the Default Gateway (x.x.x.x)
    8- DNS Servers - Provide the DNS server IP address for the VCSA. (x.x.x.x,x.x.x.x)
    9- Common Ports - Leave Defaults unless you need to customize them for your enviroment.

12- Review your configuration and Click “Finish” to initiate stage 1 of deploying the VCSA.
    ![Configure the network settings”](Pic/deploy_ova_7u3.png)

13- After sucessfully completing stage 1 of the VCSA. Click “Continue” to proceed to stage 2.
    ![Sucessfully completing stage”](Pic/stage1_vcsa_7u3.png)

14- Review the introduction screen and Click “Next” to continue.
     ![Stage2 Intro”](Pic/stage2_intro_7u3.png)

15- Configure NTP and SSH configuration for the VCSA. After configuring NTP and SSH, Click “Next” to continue.
    ![Configure NTP and SSH configuration”](Pic/stage2_ntp_ssh_7u3.png)
    1- Time synchronization mode
        Select one of the following:
            1). synchronize time with NTP Server
                Uses a Network Time Protocol server for synchronizing the time. If you select this option, you must enter the names or IP addresses of the NTP servers separated by commas.
            2) synchronize time with the ESXi host
                Enables periodic time synchronization, and VMware Tools sets the time of the guest operating system to be the same as the time of the ESXi host.
    2- SSH Access
        Select one of the following:
            - Disabled
            - Enabled
16- Choose your SSO Configuration and Click “Next” to continue.
     !["Choose your SSO Configuration”](Pic/stage2_sso_7u3.png)

17- Configure CEIP and Click “Next” to continue
    !["Configure CEIP”](Pic/stage2_ceip_7u3.png)

18- Review Ready to complete screen and verify configuration. Click “Finish” to initiate stage 2.
     !["Configure CEIP”](Pic/stage2_complete_7u3.png)

19- After sucesfully completing stage 2, you will be presented with a URL. Click the URL to launch the vSphere Client. You can now close the vCenter Server Installer.
       !["Successfully Completed!”](Pic/stage2_url_7u3.png)

20- Click “Launch vSphere Client (HTML5)”
   !["Launch vSphere Client”](Pic/launch_vsphere_html_7u3.png)

21- Log into vSphere client using administrator@vsphere.local account.
    !["Log into vSphere client”](Pic/vcsa_login_7u3.png)

22- You have succesfully deployed the vCenter Server Appliance!
    !["Succesfully deployed the vCenter Server Appliance”](Pic/done_7u3.png)


   
   
