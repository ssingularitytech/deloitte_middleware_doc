**To install IIS on the windows server:**

Open server manager: (Windows → search “Server Manager”)



1. Click on Manage



<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")




2. Select Add Roles and Features



<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image2.png "image_tooltip")




3. Click Next



<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image3.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image3.png "image_tooltip")




4. Select “Role-Based or feature-based installation” and click Next



<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image4.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image4.png "image_tooltip")




5. Select the server and proceed.



<p id="gdcalert5" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image5.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert6">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image5.png "image_tooltip")




6. Select “Web Server (IIS)” in server roles and proceed further.



<p id="gdcalert6" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image6.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert7">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image6.png "image_tooltip")




7. Click on “Add Features”



<p id="gdcalert7" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image7.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert8">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image7.png "image_tooltip")




8. In Features select “IIS Hostable Web Core”



<p id="gdcalert8" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image8.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert9">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image8.png "image_tooltip")




9. Click on Next



<p id="gdcalert9" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image9.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert10">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image9.png "image_tooltip")




10. Click on Install.



<p id="gdcalert10" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image10.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert11">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image10.png "image_tooltip")




11. After Installation is complete click “Close”.



<p id="gdcalert11" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image11.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert12">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image11.png "image_tooltip")




12. Open Powershell as administrator and run the following command 

“Install-WindowsFeature -name Web-Server -IncludeManagementTools”



<p id="gdcalert12" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image12.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert13">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image12.png "image_tooltip")




13. After following all these steps visit the public DNS or public IP address



<p id="gdcalert13" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image13.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert14">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image13.png "image_tooltip")


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

create database Main_DB;

use Main_DB;

create table dbo.Courses(Id int unique not null identity(1,1), COURSE_ID varchar(20) unique, COURSE_TITLE varchar(225));

create table dbo.Learners(Id int unique not null identity(1,1), LEARNER_ID varchar(20) unique, LEARNER_EMAIL varchar(225) unique);

create table dbo.CourseHistory(

Id int unique not null identity(1,1), 

COURSE_ID varchar(20), 

LEARNER_ID varchar(20),

COURSE_TITLE varchar(225),

LEARNER_EMAIL varchar(225),

HOURS_SPENT int,

STATUS varchar(50),

SCORE int,

foreign key(LEARNER_ID) references dbo.Learners(LEARNER_ID),

foreign key(COURSE_ID) references dbo.Courses(COURSE_ID),

);

	

Run the above command.

To create dummy Data for testing:

insert into dbo.Courses values

('1', 'ASP.NET CORE Basics'),

('2','React Basics'),

('3','React Native Esentials'),

('4','Rails Starter'),

('5','Javascript from zero to hero'),

('6','Professional communication ethics'),

('7','How to be more professional')

insert into dbo.Learners values('1', 'abc@test.com'),('2', 'test@test.com'),('3', 'rishabh@ssingularity.co.in'),('4', 'admin@deloitte.com'),('5', 'ceo@quodeck.com')

**Once the installation of dotnet, SQL server & creation of the database is done and successfully verified Install AWS CLI on the instance to run AWS commands on the server itself**



1. Open Windows Powershell as administrator and enter the following command:

            “msiexec.exe /i https://awscli.amazonaws.com/AWSCLIV2.msi”

2. To verify the installation enter “aws --version” in the PowerShell window.

You can visit the link given below for more information.

[https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

After the successful installation of AWS CLI, we need to configure the AWS account on the instance.

Before following this step you would need to get the AWS IAM user Access Key ID & Secret Access Key beforehand.



1. Open Windows PowerShell as administrator.
2. Enter the following command: “aws configure”.
3. AWS Access Key ID will be prompted, enter your IAM Access Key ID and press ENTER.
4. AWS Secret Access Key will be prompted, enter your IAM Secret Access Key and press ENTER.
5. For the rest of the options just press ENTER.

    Here’s an example of how aws credentials will be asked.


    

<p id="gdcalert14" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image14.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert15">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image14.png "image_tooltip")



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

After you get all the plaintext secrets use the aws kms tool to encrypt all the secrets and store them in the keys.json file.

Command to encrypt:

aws kms encrypt --cli-binary-format raw-in-base64-out --key-id "<KEY_ID>" --plaintext "<SECRET_TO_ENCRYPT>"

SECRET_TO_ENCRYPT - Plain secrets needed to be encrypted.

KEY_ID - Key id present in the aws arn key.

For e.g. arn:aws:kms:eu-west-1:123456789:key/11111111-0000-0000-0000-000000000000 is the arn key

Now “1111111-0000-0000-0000-000000000000” is the key id.

You can refer to the following document for more information.

[https://github.com/Flavien/SecretConfiguration](https://github.com/Flavien/SecretConfiguration)

Store the encrypted secrets in the keys.json file now.

After this, you need to store the arn key in the secrets.json file.

Store the arn as follows:

{

	“aws_key_id”: “<PUT_YOUR_ARN_HERE>”

}

Deploy the project in the server:

Download the middleware APIs archive file from the GitHub repository.

You can download it from here:

[https://github.com/ssingularitytech/deloitte_middleware_api/archive/refs/heads/master.zip](https://github.com/ssingularitytech/deloitte_middleware_api/archive/refs/heads/master.zip)

Unzip the archive and paste the unzipped folder into the windows server instance.

Copy keys.json & secrets.json files into the root directory of the project where the .csproj file exists.

Copy the path of the root directory ( where the .csproj file exists).

Open Windows PowerShell and go to the directory using the copied location.

For e.g.

cd “C://<The correct location you’ve copied>”

Paste the following command:

dotnet publish --configuration Release

You’ll get the result as given below.

<p id="gdcalert15" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image15.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert16">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image15.png "image_tooltip")


Now copy the whole project directory and paste it into the following location:

C:\\inetpub\\wwwroot\

For e.g.



<p id="gdcalert16" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image16.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert17">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image16.png "image_tooltip")


Press the Windows key + R and type inetmgr to open IIS management tools.

Follow the given Images as follows:



<p id="gdcalert17" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image17.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert18">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image17.png "image_tooltip")




<p id="gdcalert18" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image18.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert19">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image18.png "image_tooltip")




<p id="gdcalert19" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image19.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert20">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image19.png "image_tooltip")




<p id="gdcalert20" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image20.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert21">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image20.png "image_tooltip")




<p id="gdcalert21" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image21.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert22">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image21.png "image_tooltip")




<p id="gdcalert22" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image22.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert23">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image22.png "image_tooltip")


Click on Browse Website (http) and see if there are any errors.
