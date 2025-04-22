<p align="center">
<img src="https://github.com/user-attachments/assets/72eee999-d4eb-4442-8957-31e4502bc391" 
</p>



# 🛠️ osTicket: Prerequisites and Installation

> In this lab, I installed the open-source helpdesk platform osTicket on a Windows 10 virtual machine. I handled web server setup, PHP configuration, MySQL installation, and all required dependencies to get the system running smoothly on IIS.

---

## ⚙️ Stack & Services Used
| Component         | Version        | Purpose                              |
|------------------|----------------|--------------------------------------|
| Windows 10        | Host OS         | VM Environment                       |
| IIS               | w/ CGI Enabled | Web server for hosting osTicket      |
| PHP               | v7.3.8         | Required for osTicket scripting      |
| MySQL             | v5.5.62        | Backend database for ticket storage  |
| osTicket          | v1.15.8        | Helpdesk/ticketing system            |
| PHP Manager       | 1.5.0          | Integration with IIS                 |
| VC++ Redist       | x86            | Dependency for PHP                   |
| Rewrite Module    | (64-bit)       | Enables URL routing for osTicket     |

---

## 🧩 Step-by-Step Breakdown

🔹 **Environment Setup**
- Deployed Windows 10 VM and connected via RDP
- Created “osTicket-Installation-Files” folder and extracted resources

🔹 **IIS & PHP Configuration**
- Enabled CGI support in IIS
- Installed PHP Manager and Rewrite Module
- Created `C:\PHP` directory and extracted PHP binaries
- Registered `php-cgi.exe` in IIS via PHP Manager

🔹 **MySQL Database Setup**
- Installed MySQL 5.5 with root user: `root/root`
- Verified installation and access via configuration wizard

🔹 **osTicket Deployment**
- Unzipped osTicket to `C:\inetpub\wwwroot\`
- Renamed upload folder to `osTicket`
- Reloaded IIS and accessed setup through browser (localhost)

---

## 📸 Screenshots *(Add your visual proof here)*  
> PHP in IIS Manager, folder structure, osTicket setup page, MySQL config wizard, etc.


https://github.com/user-attachments/assets/1e43033a-6a1a-4508-ba35-255519d8ed22

<p align="center">
  <img src="https://github.com/user-attachments/assets/46410c93-4b58-4f21-8d93-fce53267cb1a" width="850"/>
</p>

<img src="https://github.com/user-attachments/assets/33caf0a5-7099-4cf6-8470-a0f85af09640" width="500" height="450"/>
<img src="https://github.com/user-attachments/assets/9fdb430c-532a-445a-8eed-a48d2cfcd548" width="500" height="450"/>


---

## 💡 Lessons Learned
✅ A successful deployment requires precise dependency versions (especially PHP)  
✅ IIS must be configured with proper extensions and routing modules  
✅ Testing each component individually (PHP, MySQL, IIS) avoids setup issues later  
✅ Understanding the backend stack builds confidence when deploying real-world platforms  

---


