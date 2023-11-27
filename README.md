# Windows Server 2022 Administration
Using Windows Server 2022 for Administration

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/fa137044-93bb-4b3d-898e-f89ae6ebc921)

Changing the Computer Name to something less arbitrary, and more fun.

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/bf927957-4685-4673-b445-d7ff734cb77a)


- Checking out the IP information and disabling IPv6 for now. 
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/c1d04da7-6add-4795-9df2-8305b5726839)

Enabling Remote Desktop on the Server:

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/027ce084-09a9-47a1-9d96-fc83ce37d752)

Rebooting so that the name change to the computer takes effect.


Going into Manage > Add Roles and Features, I will be sticking with the Role-based or feature-based installation. 

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/9e5ec65c-1ed0-40c6-b02b-e695c9b1fde3)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/bbbb90e6-3612-4460-b9f4-9d7d989fe604)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/17a1748e-06ba-467f-93a1-b1636ae9d341)

# Installing Active Directory:
- Active Directory Domain Services only for now.

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/9f344cbe-c23b-4db5-9ca7-6e302384fe53)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/ad433761-65b8-40df-964e-446225d66b7c)


After it finished installing, I am going to promote this server to a Domain controller. Then I will setup a whole new forest. 

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/5178b7bb-474d-4393-b996-961edb734a5b)
![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/95e645cc-664f-4bce-acaa-dc2285cb4dd5)
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

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/fb63a65a-e3bb-4025-861f-6325a067c29f)

## Tools > Active Directory Users and Computers

![image](https://github.com/CertainRisk/Windows-Server-2022/assets/141761181/5f9cf47b-cbf6-4118-8aff-66e675426760)















