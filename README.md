# DapperCRUD
CRUD Operations in ASP.NET MVC 5 using Dapper and Stored Procedure

Stored Procedures in the SQL Server
- AddNewEmpDetails
- GetEmployees
- UpdateEmpDetails
- DeleteEmpById

<br>



</br>

1. AddNewEmpDetails

USE [test]
GO
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE procedure [dbo].[AddNewEmpDetails]
(
@Name varchar (50),
@City varchar (50),
@Address varchar (50),
@EmpId int
)
as
begin
Insert into Employee values(@Name,@City,@Address)
End
;

<br>

</br>

2. GetEmployees

USE [test]
GO
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE Procedure [dbo].[GetEmployees]    
as    
begin    
   select Id as Empid,Name,City,Address from Employee  
End
;

<br>

</br>

3. UpdateEmpDetails

USE [test]
GO
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE procedure [dbo].[UpdateEmpDetails]  
(  
   @EmpId int,  
   @Name varchar (50),  
   @City varchar (50),  
   @Address varchar (50)  
)  
as  
begin  
   Update Employee  
   set Name=@Name,  
   City=@City,  
   Address=@Address  
   where Id=@EmpId  
End
;

<br>

</br>

4. DeleteEmpById

USE [test]
GO
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE procedure [dbo].[DeleteEmpById]  
(  
   @EmpId int  
)  
as  
begin  
   Delete from Employee where Id=@EmpId  
End
;
