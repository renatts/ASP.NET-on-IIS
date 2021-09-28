## Microsoft Machine Bonus Application (IIS)
### Part I
1. Create a new project in `Visual Studio 19`
2. In the `Create a new project` window, choose `C#` from the Language list.
3. Choose `Windows` from the Platform list, and `Web` from the project types list.
4. Choose the `ASP.NET Core Web App` template, and then choose `Next`.
5. In the `Configure your new project` window, type or enter Project name in the `Project name` box. Then, choose `Next`.
6. In the `Additional information` window, verify that `.NET 5` appears in the top drop-down menu.
7. Uncheck the `Configure for HTTPS` checkbox.
8. Right-click on your project and choose `Manage NuGet Packages`.
9. Search for `Newtonsoft.Json` and install it for your project.
10. Check your `.csproj` file (`Newtonsoft.Json` package has been added).
11. Right-click on your `solution` and choose `Restore Nuget Packages`.
12. `Rebuild` your solution.
13. Right-click on your project and choose `Publish`.
14. In publish window choose `Folder`.
15. In Location choose the folder location and then choose `Finish`.
16. In publish window press the `Publish` button.
17. Some publishing files were created at `[Your project]/bin/Release/net5.0/publish`.
18. Check your project is running.

### Part II
1. Search for `Remote Desktop Connection` on your computer.
2. Insert the `IP` address of your remote server.
3. Insert your `username` and `password`.
4. Choose `Local Resources` and then press on `More...`.
5. Click on `+` near the `Drives` option.
6. Choose your drive (the drive that includes your `ASP.NET` project) and then press `OK`.
7. Go back to `General` and press `Connect`.
8. Add `IIS Manager` to your `Windows` server.
9. Create new application pool by right-clicking `Application Pools`.
10. For `.NET 5` choose `No Managed` and `Integrated`.
11. Create new website by right-clicking `Sites`.
12. Give your site a name, press `SELECT` and choose the application pool that you created at step 9.
13. On physical path insert: `C:/inetpub/wwwroot`.
14. In `wwwroot` directory press `Make New Folder` and create a folder for your website.
15. In `Binding` insert the port for your website (for example: 5100) and press `OK`.
16. Right-click on your website and press `Explore`.
17. Copy your `publish` folder (`PART I`) to the folder you created at step 14.
18. Your website has been created so `refresh` it and browse on `http://localhost:[your port]`.
19. There is an `ERROR` (500.29).
20. Download `ASP.NET Core Hosting Bundle` and install it on your windows server machine
    (`https://dotnet.microsoft.com/download/dotnet/thank-you/runtime-aspnetcore-5.0.10-windows-hosting-bundle-installer`).
22. `Refresh` your website and press `Browse*:[your port](http)`.
23. It finally works!
