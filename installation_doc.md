**To install IIS on the windows server:**

Open server manager: (Windows → search “Server Manager”)



1. Click on Manage


<img width="960" alt="click on manage" src="https://user-images.githubusercontent.com/56874272/201602505-97bb2c5c-c442-4836-98d7-5cda78c962a0.png">




2. Select Add Roles and Features

<img width="960" alt="2022-10-01 (2)" src="https://user-images.githubusercontent.com/56874272/201602733-5bf6717d-783c-4377-b44e-a8a330eeb655.png">


3. Click Next

<img width="960" alt="2022-10-01 (3)" src="https://user-images.githubusercontent.com/56874272/201602865-e6906f67-f310-4c1b-8e6b-a7107a372d5e.png">



4. Select “Role-Based or feature-based installation” and click Next

<img width="960" alt="2022-10-01 (4)" src="https://user-images.githubusercontent.com/56874272/201602940-170461bb-2d68-482e-8497-1b2217660566.png">



5. Select the server and proceed.

<img width="960" alt="2022-10-01 (5)" src="https://user-images.githubusercontent.com/56874272/201603105-76117fe2-ed69-4ff0-8c8b-c1f6f8bf4335.png">


6. Select “Web Server (IIS)” in server roles and proceed further.

<img width="960" alt="2022-10-01 (8)" src="https://user-images.githubusercontent.com/56874272/201603341-65f93ef9-3973-4e2b-86c5-6c93a11d922d.png">


7. Click on “Add Features”

<img width="960" alt="2022-10-01 (9)" src="https://user-images.githubusercontent.com/56874272/201603476-6771f296-02b2-4584-bb48-45c7c094c183.png">

8. In Features select “IIS Hostable Web Core”

<img width="960" alt="2022-10-01 (7)" src="https://user-images.githubusercontent.com/56874272/201603601-ae263e51-5a1e-4453-9370-b13afc41cf8c.png">

9. Click on Next

<img width="960" alt="2022-10-01 (11)" src="https://user-images.githubusercontent.com/56874272/201603798-4a3e4fa9-31c5-467b-9df9-5d1900bfa631.png">


10. Click on Install.

<img width="960" alt="2022-10-01 (12)" src="https://user-images.githubusercontent.com/56874272/201603849-0ec6eda5-60de-4ebc-9fcd-0b137d15e885.png">


11. After Installation is complete click “Close”.

<img width="960" alt="2022-10-01 (13)" src="https://user-images.githubusercontent.com/56874272/201603942-c4b84c8f-b778-4ecb-b3f8-e7c24b0b243b.png">


12. Open Powershell as administrator and run the following command 

<img width="960" alt="2022-10-01 (27)" src="https://user-images.githubusercontent.com/56874272/201604060-9f465f1a-fbcc-4cfb-a405-3d014cbd7af7.png">

13. After following all these steps visit the public DNS or public IP address

<img width="960" alt="2022-10-01 (29)" src="https://user-images.githubusercontent.com/56874272/201604109-7bb32d49-9e74-4a18-b979-871ed5d563a1.png">


IIS is installed successfully on the windows server.

**To install Dot net core hosting and runtime and the SDK:**

Download and install the following packages:



1. ASP NET CORE 6 SDK: \
[https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/sdk-6.0.402-windows-x64-installer](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/sdk-6.0.402-windows-x64-installer)
2. ASP NET CORE 6 Hosting Bundler

    [https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-aspnetcore-6.0.10-windows-hosting-bundle-installer](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-aspnetcore-6.0.10-windows-hosting-bundle-installer)


Once the installation is complete open windows PowerShell and enter the following command:

“dotnet --version”

The output should show a version not an error message. If there’s any error please retry the installation carefully.

Time to set up SQL server in the instance.

Download the SQL server & SSMS from the given links:



1. SQL Server

[https://www.microsoft.com/en-in/sql-server/sql-server-downloads](https://www.microsoft.com/en-in/sql-server/sql-server-downloads)



2. SSMS

[https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16)

Download and install the following software on the server.

To create DB:

Run the following query to create  Main DB:

```sql

create database Main_DB;

use Main_DB;

create table dbo.Courses(Id int unique not null identity(1,1), COURSE_ID varchar(20) unique, COURSE_TITLE varchar(225));

create table dbo.Learners(Id int unique not null identity(1,1), LEARNER_ID varchar(20) unique, LEARNER_EMAIL varchar(225));

create table dbo.CourseHistory(

Id int unique not null identity(1,1), 

LEARNER_ID varchar(20),

COURSE_TITLE varchar(225),

LEARNER_EMAIL varchar(225),

DURATION_HOURS int,

EVL_STATUS varchar(50),

SCORE int,

foreign key(LEARNER_ID) references dbo.Learners(LEARNER_ID),

);

	

--Run the above command.

--To create dummy Data for testing:

insert into dbo.Courses values

('1', 'ASP.NET CORE Basics'),

('2','React Basics'),

('3','React Native Esentials'),

('4','Rails Starter'),

('5','Javascript from zero to hero'),

('6','Professional communication ethics'),

('7','How to be more professional')

insert into dbo.Learners values('1', 'abc@test.com'),('2', 'test@test.com'),('3', 'rishabh@ssingularity.co.in'),('4', 'admin@deloitte.com'),('5', 'ceo@quodeck.com')

```

**Once the installation of dotnet, SQL server & creation of the database is done and successfully verified Install AWS CLI on the instance to run AWS commands on the server itself**



1. Open Windows Powershell as administrator and enter the following command:
```powershell
msiexec.exe /i https://awscli.amazonaws.com/AWSCLIV2.msi
```

2. To verify the installation enter “aws --version” in the PowerShell window.

You can visit the link given below for more information.

[https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

After the successful installation of AWS CLI, we need to configure the AWS account on the instance.

Before following this step you would need to get the AWS IAM user Access Key ID & Secret Access Key beforehand.



1. Open Windows PowerShell as administrator.
2. Enter the following command:
```powershell
aws configure
```
3. AWS Access Key ID will be prompted, enter your IAM Access Key ID and press ENTER.
4. AWS Secret Access Key will be prompted, enter your IAM Secret Access Key and press ENTER.
5. For the rest of the options just press ENTER.

    Here’s an example of how aws credentials will be asked.

![image](https://user-images.githubusercontent.com/56874272/201606256-602819ae-a05a-4c69-8a63-994c98eb45e8.png)


After this, we are done with the setup and configurations.

The next steps are to encrypt and store the secrets in a keys.json file.

**The following secrets shall be encrypted:**

* Main_Db
* DEP_STRING
* public_key
* private_key
* api_key_rsa
* api_key
1. Main_Db - You will need to run a query in SSMS and get the MAIN DB Connection string.
2. DEP_STRING - You will be given the following DEP string from the DEP team.
3. public_key, private_key, api_key_rsa, api_key - You will be given these by mail.

To get the Main DB connection string use the following query in ssms: 

```sql
 use <PUT_YOUR_DATABASE_NAME_HERE>;


    select


        'Data Source=' + @@servername +


        '; Initial Catalog=' + db_name() +


        case type_desc


            when 'WINDOWS_LOGIN'


                then '; Trusted_Connection=true'


            else


                ';User Id=' + suser_name() + '; Password=<<YourPassword>>'


        end


        as ConnectionString


    from sys.server_principals


    where name = suser_name()
```

After you get all the plaintext secrets use the aws kms tool to encrypt all the secrets and store them in the keys.json file.

Command to encrypt:

```powershell
aws kms encrypt --cli-binary-format raw-in-base64-out --key-id "<KEY_ID>" --plaintext "<SECRET_TO_ENCRYPT>"
```

SECRET_TO_ENCRYPT - Plain secrets needed to be encrypted.

KEY_ID - Key id present in the aws arn key.

For e.g. arn:aws:kms:eu-west-1:123456789:key/11111111-0000-0000-0000-000000000000 is the arn key

Now “1111111-0000-0000-0000-000000000000” is the key id.

You can refer to the following document for more information.

[https://github.com/Flavien/SecretConfiguration](https://github.com/Flavien/SecretConfiguration)

Store the encrypted secrets in the keys.json file now.

After this, you need to store the arn key in the secrets.json file.

Store the arn as follows:
```
{

	“aws_key_id”: “<PUT_YOUR_ARN_HERE>”

}
```

Deploy the project in the server:

Download the middleware APIs archive file from the GitHub repository.

You can download it from here:

[https://github.com/ssingularitytech/deloitte_middleware_api/archive/refs/heads/master.zip](https://github.com/ssingularitytech/deloitte_middleware_api/archive/refs/heads/master.zip)

Unzip the archive and paste the unzipped folder into the windows server instance.

Copy keys.json & secrets.json files into the root directory of the project where the .csproj file exists.

Copy the path of the root directory ( where the .csproj file exists).

Open Windows PowerShell and go to the directory using the copied location.

For e.g.

```powershell
cd C://<The correct location you’ve copied>
```

Paste the following command:

```powershell
dotnet publish --configuration Release
```

You’ll get the result as given below.

<img width="960" alt="2022-10-01 (40)" src="https://user-images.githubusercontent.com/56874272/201608907-1d896f03-97e5-43c1-b194-ef4dab9e2499.png">


Now copy the whole project directory and paste it into the following location:

```
C:\\inetpub\\wwwroot\
```

For e.g.

<img width="960" alt="2022-10-01 (43)" src="https://user-images.githubusercontent.com/56874272/201608964-657472e1-3cee-4689-9313-5c61b7284d41.png">


Press the Windows key + R and type inetmgr to open IIS management tools.

Follow the given Images as follows:

<img width="960" alt="2022-10-01 (44)" src="https://user-images.githubusercontent.com/56874272/201609160-7244354a-e261-4892-8f3e-9a2e74d3cae6.png">
<img width="960" alt="2022-10-01 (45)" src="https://user-images.githubusercontent.com/56874272/201609343-dac4bdab-50c5-4717-bffa-dafb02f73dac.png">
<img width="960" alt="2022-10-01 (46)" src="https://user-images.githubusercontent.com/56874272/201609347-5cdddc16-419b-482f-9bb4-52497a5899f4.png">
<img width="960" alt="2022-10-01 (47)" src="https://user-images.githubusercontent.com/56874272/201609325-d4ea4124-531b-40b7-bbc7-885400ad8294.png">
<img width="960" alt="2022-10-01 (48)" src="https://user-images.githubusercontent.com/56874272/201609335-c8a60921-586b-4f52-8ae2-16ff6a5cdecb.png">
<img width="960" alt="2022-10-01 (49)" src="https://user-images.githubusercontent.com/56874272/201609340-919d78ad-35e6-4641-b68f-d869776138ff.png">


Click on Browse Website (http) and see if there are any errors.
