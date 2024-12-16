
# Creating Areas in ASP.NET Core MVC

Areas in ASP.NET Core MVC allow you to partition your application into smaller functional groupings (e.g., Admin, User). This helps in organizing large applications and managing separate sections for different purposes.

## Steps to Create Areas Using New Scaffolded Item

### 1. Add a New Area
1. **Right-click on the project** in **Solution Explorer**.
2. Select **Add** > **New Scaffolded Item**.
3. In the **Add Scaffold** dialog, select **MVC Area** and click **Add**.
4. Enter the name of the area (e.g., `Admin` or `User`) and click **Add**.

   This automatically creates the following folder structure for the specified area:
   ```
   Areas
   ├── Admin (or User)
       ├── Controllers
       ├── Views
       └── Models
   ```


### 2. Configure Routing for Areas
Make sure your routing configuration includes support for areas. Update the `Program.cs` file as follows:
```csharp
app.UseEndpoints(endpoints =>
{
    endpoints.MapControllerRoute(
        name: "areas",
        pattern: "{area:exists}/{controller=Home}/{action=Index}/{id?}");
    endpoints.MapDefaultControllerRoute();
});
```

copy the MapControllerRoute() from `ScaffoldingReadMe.txt` file to `Program.cs` file:
```csharp
app.MapControllerRoute(
    name: "areas",
    pattern: "{area:exists}/{controller=Home}/{action=Index}/{id?}"
);
```


### 3. Add Controllers and Views for Each Area
1. Inside the `Controllers` folder of the newly created area, **add a new controller**:
   - Right-click on the `Controllers` folder > **Add** > **Controller**.
   - Select **MVC Controller - Empty**.
   - Name the controller (e.g., `HomeController`) and click **Add**.
   - Add the `[Area]` attribute to the controller to specify its area:
     ```csharp
     [Area("Admin")]
     public class HomeController : Controller
     {
         public IActionResult Index()
         {
             return View();
         }
     }
     ```

2. **Add Views for the Controller**:
   - Add view file `Index.cshtml` in controller specific View folder.


### 4. Link Between Areas
To navigate between areas, use the `asp-area`, `asp-controller`, and `asp-action` attributes in your Razor views.

- **In Admin Area**:
  ```html
  <a asp-area="User" asp-controller="Home" asp-action="Index">Go to User Home</a>
  ```

- **In User Area**:
  ```html
  <a asp-area="Admin" asp-controller="Home" asp-action="Index">Go to Admin Home</a>
  ```


### 5. Adding Multiple Areas
Repeat the above steps to create additional areas, such as `User` or `Support`. Ensure each area has its own set of controllers, views, and routes.


### Summary
- The **New Scaffolded Item** option simplifies the creation of the **Areas** folder structure.
- Each area is isolated and contains its own controllers, views, and models.
- Use `asp-area` in Razor views for seamless navigation between areas.
