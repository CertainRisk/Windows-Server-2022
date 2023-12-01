# Windows Server 2022 Administration
Using Windows Server 2022 for Administration

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/fa137044-93bb-4b3d-898e-f89ae6ebc921)

Changing the Computer Name to something less arbitrary, and more fun.

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/bf927957-4685-4673-b445-d7ff734cb77a)


- Checking out the IP information and disabling IPv6 for now. 
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/c1d04da7-6add-4795-9df2-8305b5726839)

# Simple Volume Creation

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/ccda7a8c-a2a3-44c7-b72c-cf7e72fdc067)

Right clicking the unallocated space to enter the Simple Volume Wizard. I will make this smaller than the default since I am messing around and learning!
- I will stick the the NTFS file system as that's the one I am most familiar with. 

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/24a33789-2d8d-4dcd-972e-5f8277c5dd26)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/524a9aed-faec-4c59-807d-443408a051f7)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/b686016a-0ea5-407c-a5db-939578c0d1f6)

## Extending and Shrinking Volumes 

I'm going to add another 50,000 in order to extend the volume.

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/790fed03-7871-4175-a8ec-71e51f62ad90)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/4e7cc38c-4b78-464b-950b-91b0e36bd999)

Time to shrink it! I'm going to shrink it to 80,000 MB.

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/514044ef-bcc2-480a-870b-bef6b79c6acf)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/4863ab92-9289-4c73-b8fa-cb645947198d)

## Converting Disks - From basic to dynamic 

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/6e9a5f75-fcd2-4afd-bd86-584cc74ac0d3)

- **Spanned disks:** Take space from more than one physical disk to create the appearance of a single, larger volume for the user.

- **Striped volumes:** Store data in stripes across two or more disks with the aim of providing faster access to your data compared to simple or spanned volumes.
  - This implies designating an equal amount of space on two or more volumes because the data will be striped across all of the disks. This method ensures better read performance.

- **Mirrored volumes:** Duplicate the data on two disks, dividing it equally between each disk. For example, if it indicates the use of 40,000 MB of storage, only 20,000 MBs can be utilized due to the setup of mirrored volumes for fault tolerance.

- **RAID-5 Volumes:** Store data in stripes across three or more disks. The greater the number of disks in RAID-5, the greater the performance benefits. In an example of three disks, all would be 20,000 MB each but one would be a recovery block. Each stripe will put the recovery block on a different of the three disks. This allows for read performance benefits and you can have a disk space utilization benefit better than mirroring. 


Enabling Remote Desktop on the Server:

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/027ce084-09a9-47a1-9d96-fc83ce37d752)

Rebooting so that the name change to the computer takes effect.


Going into Manage > Add Roles and Features, I will be sticking with the Role-based or feature-based installation. 

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/9e5ec65c-1ed0-40c6-b02b-e695c9b1fde3)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/bbbb90e6-3612-4460-b9f4-9d7d989fe604)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/33a1ce30-b487-42c2-8a4d-23f09bb450e5)


# Installing Active Directory:
- Active Directory Domain Services only for now.

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/9f344cbe-c23b-4db5-9ca7-6e302384fe53)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/ad433761-65b8-40df-964e-446225d66b7c)


After it finished installing, I am going to promote this server to a Domain controller. Then I will setup a whole new forest. 

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/5178b7bb-474d-4393-b996-961edb734a5b)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/b542e677-3c20-4c61-8bc6-60afd9fd3a5d)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/5d924e8b-f7e7-4c1a-a356-3bf625860db5)

DNS is not yet installed so I will be skipping this option till AD can handle that. Then I will continue on till the installation is finished!

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/83485159-4a69-492e-bcc2-380749910ba3)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/17e6e0df-1611-4c8d-9065-3b7adee1bc4f)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/6c6fce9b-6569-427a-81e2-7f38864ad9fb)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/1ebfbe7a-3200-4cc7-91d2-5f25138e2380)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/29928037-c407-45ce-a43d-4da1ce54c26a)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/371287f2-23f4-406f-9db5-42675b5b2958)

Success!
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/b97bf2ec-8f8e-45d3-b591-2f6f50db3703)

## Tools > DNS > DNS Manager
- Looking through to see that everything was installed correctly and it was. 

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/4d2dac85-0c65-4a5a-abe5-bb1c6d05882d)


## Tools > Active Directory Users and Computers

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/161dedc8-1ab5-471e-aee2-5836e318c0ee)


## Installing an additonal domain controller for fault tolerance and redundancy. 
- Promoting the DC2 to a domain controller.
  
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/f172e5b6-1462-4fad-907e-4ea4f0460f1c)












