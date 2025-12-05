
🟦 1. What is MVC (Model View Controller)?

MVC stands for Model–View–Controller, which is a famous architectural pattern used to build modern web applications.
The Model contains the application data and business logic, and communicates with the database.
The View is responsible for presenting data to the user through the UI layer using HTML, CSS, and JavaScript.
The Controller handles incoming browser requests, processes user input, and interacts with both Model and View.
MVC helps in separating data, UI, and logic, which makes the application easier to maintain and modify.
Because of this separation, developers can work on different layers at the same time without affecting each other.
MVC also improves testability because each part can be tested individually.
It provides complete control over HTML output, unlike WebForms which restricts customization.
MVC supports clean URL routing, making applications more SEO-friendly.
Overall, MVC creates a structured, organised, and scalable web application architecture.

🟩 2. What are the advantages of MVC?

One major advantage of MVC is Separation of Concerns, meaning UI, business logic, and data are all kept separate.
This separation makes applications easier to maintain, test, and debug.
MVC supports multiple views, so the same data can be displayed in many different formats (mobile, desktop, API, etc.).
It provides full control over HTML, CSS, and JavaScript, allowing responsive and modern UI development.
MVC is lightweight because it does not use ViewState, resulting in faster performance.
It supports Test Driven Development (TDD), as each layer can be tested independently.
Since MVC is built on ASP.NET, developers can still use features like roles, membership, caching, and authorization.
Changes in the UI do not affect higher layers, making UI maintenance easier.
Teams can work parallelly: one on the View, one on the Controller, and one on the Model.
It allows better application scaling, improving project quality and speed of development.

🟧 3. Explain the MVC Application Life Cycle

The MVC application lifecycle has two main phases: creating the request and generating the response.
The first phase begins when a user sends a URL request, and ASP.NET checks the routing table in Global.asax.
The routing system matches the URL to a specific controller and action method.
Next, a RouteData object is created, which stores controller and action names.
Then, a RequestContext object is created, which passes request data to the MVC Handler.
The MVC Handler creates the controller instance using the controller factory.
Once the controller object is ready, its Execute method is called, and the action method runs.
The second phase begins when the action method prepares data and selects the appropriate View.
The View Engine generates HTML from the View and model data.
Finally, the rendered HTML is returned to the browser as the response to the original request.

🟥 4. List out different return types of a Controller Action Method

ASP.NET MVC has nine main return types, each used for a different purpose.
ViewResult is used to return a full HTML view to the browser.
PartialViewResult returns a portion of a view, useful for Ajax or page sections.
RedirectResult redirects the user to another URL, while RedirectToRouteResult redirects to another action.
ContentResult sends plain text or a string response.
JsonResult returns JSON data, commonly used in APIs and AJAX operations.
JavaScriptResult sends JavaScript code to the browser for dynamic operations.
FileResult allows downloading files like PDF, Excel, or images from the server.
EmptyResult returns nothing and is used when no output is needed.
All these return types inherit from ActionResult, making them part of the same hierarchy.

🟪 5. What are Filters in MVC?

Filters allow developers to execute code before or after an action method runs.
They help with cross-cutting concerns like authentication, logging, caching, and handling exceptions.
MVC provides four main filter types: Action Filters, Authorization Filters, Result Filters, and Exception Filters.
Filters make controllers cleaner by separating repeated logic like validation or security.
Authorization filters ensure that only authorized users can access certain actions.
Action filters can modify inputs or outputs before and after action execution.
Result filters run before and after the view is rendered, allowing customization of output.
Exception filters catch errors globally and provide a custom error page.
Filters help improve maintainability and reduce code duplication across controllers.
They also make applications more secure, testable, and efficient.

🟫 6. What are Action Filters in MVC?

Action Filters are attributes applied on controllers or action methods to run custom logic.
They execute before or after an action method runs, allowing developers to plug in reusable logic.
Common action filters include OutputCache, Authorize, and HandleError.
OutputCache improves performance by caching the action’s output for a defined time.
Authorize restricts access to actions based on users or roles.
HandleError catches exceptions and displays a user-friendly error page.
Action Filters reduce repeated code and centralize logic across multiple actions.
They improve application performance and security when used correctly.
Filters can be applied at method level, controller level, or globally.





🔷 6. What is an Action Method in MVC?

(10-line detailed answer)

An Action Method is a public method inside a Controller that handles incoming user requests.
Only public methods can act as action methods; private or protected methods cannot.
When a user accesses a URL, MVC maps it to a specific action method based on routing rules.
Action methods can take parameters, process business logic, and return various ActionResults.
Each action method typically returns a View, JSON, a file, a redirect, or no content at all.
These methods help separate input-control logic from UI and data logic.
Overloading action methods is possible, but parameter binding decides which one executes.
Attributes like [HttpGet], [HttpPost], [Authorize], etc., control how action methods behave.
Action methods should be small, readable, and focused on orchestrating logic—not containing heavy business logic.
Overall, action methods are the entry point for executing any functionality in an MVC controller.

🔷 7. What is Routing in MVC?

(10-line detailed answer)

Routing in MVC is the process of mapping a URL request to a specific controller and action method.
Instead of relying on physical file paths, MVC uses routes to determine how URLs behave.
Routing rules are defined in the RouteConfig.cs file using routes.MapRoute().
The default route format is usually {controller}/{action}/{id}.
When a user enters a URL, the routing engine checks the route table and finds a match.
If matched, it extracts controller name, action method, and optional parameters.
Routing makes URLs clean, user-friendly, and SEO-friendly.
MVC supports both convention-based routing and attribute routing.
Attribute routing allows applying route patterns directly on controllers and actions using [Route("path")].
Overall, routing gives developers full control over URL structure and navigation.

🔷 8. What is the difference between ViewData, ViewBag, and TempData?

(10-line detailed answer)

ViewData is a dictionary used to pass data from controller to view using keys; it requires typecasting.
ViewBag is a dynamic wrapper around ViewData that allows passing data without typecasting.
Both ViewData and ViewBag work only for the current request and are not preserved after redirect.
TempData stores data for one request and survives redirects; it's used for passing messages like success or errors.
TempData uses Session under the hood, so it persists until it is read.
ViewBag and ViewData are best for transferring small UI data like titles or dropdown lists.
TempData is ideal for redirect scenarios such as post-save messages.
All three work as communication mechanisms between controllers and views.
They should not be used for large data storage; models are preferred for this.
Choosing between them depends on whether data should persist after a redirect or not.

🔷 9. What is Razor View Engine?

(10-line detailed answer)

Razor is a lightweight view engine used in ASP.NET MVC to write server-side code inside HTML.
It uses the @ symbol to switch between HTML and C# code seamlessly.
Razor syntax is clean, readable, and minimizes the number of characters required compared to ASPX syntax.
Razor automatically detects whether you're writing HTML or C# without needing special tags.
It prevents script injection attacks by using HTML encoding by default.
Razor files use .cshtml (C#) or .vbhtml (VB) extensions.
It supports layout pages, partial views, and section rendering.
Razor helps in creating dynamic, interactive UI with minimal code.
It improves productivity, readability, and maintainability of view pages.
Razor is the default view engine for MVC and ASP.NET Core MVC.

🔷 10. What are Strongly Typed Views in MVC?

(10-line detailed answer)

A Strongly Typed View is a view that is bound to a specific model class.
It uses @model at the top of the view to define which model the view expects.
This provides compile-time type checking, reducing runtime errors.
IntelliSense support becomes available in the view, improving development speed.
Strongly typed views make the application more structured and maintainable.
It ensures that incorrect property names are caught during compilation.
Useful for edit forms, detail pages, and any screen requiring model data.
Strongly typed views reduce the use of ViewBag and ViewData.

🔷 11. What is a Controller in MVC?

(10-line detailed answer)

A Controller is a C# class in MVC that handles all incoming requests from the browser.
It acts as the middle layer between the View and the Model.
A controller contains action methods, and each action executes specific logic when requested.
Routing decides which controller and action method should run for a given URL.
The controller reads user input, processes it, and then decides which View to display.
It may also call the Model to retrieve or update data.
Controllers help in separating business logic from UI logic.
They improve maintainability by keeping application behavior organized.
Only public methods of a controller can act as action methods.
In summary, the controller is the “brain” of the MVC application that orchestrates the whole flow.

🔷 12. What is an ActionResult?

(10-line detailed answer)

ActionResult is the base class for all return types of action methods in MVC.
It represents the result of an action method call and controls what the user sees next.
Examples include ViewResult, JsonResult, RedirectResult, FileResult, and more.
Using ActionResult allows a controller to return different types of responses.
It helps maintain flexibility while keeping action methods clean and reusable.
ActionResult is part of the System.Web.Mvc namespace and provides polymorphism.
Action methods returning ActionResult can decide at runtime what to return.
You can also create custom ActionResults for special behaviors.
It improves readability and simplifies handling multiple response types.
Thus, ActionResult plays a key role in MVC request–response management.

🔷 13. What is a Partial View? When do you use it?

(10-line detailed answer)

A Partial View is a reusable part of a view that can be rendered inside another view.
It helps break large views into smaller, manageable components.
Commonly used for repeated UI sections like headers, menus, or data cards.
Partial Views improve maintainability and reduce duplicate HTML code.
They are rendered using @Html.Partial() or @Html.RenderPartial().
Partial Views do not have their own layout by default.
They can receive model data like a normal view.
They improve performance when only a portion of the page needs updates.
Good for AJAX-based updates where only small content changes dynamically.
In summary, Partial Views help you write cleaner and modular UI code.

🔷 14. What is a Layout in MVC?

(10-line detailed answer)

A Layout in MVC is like a master page that defines the common structure for your application.
It contains shared UI elements like header, footer, and navigation menu.
Views can reference the layout using @{ Layout = "_Layout.cshtml"; }.
Layouts help avoid duplication of common HTML in every view.
They provide a consistent look and feel across the entire website.
Sections inside layouts allow individual views to override certain areas.
Layouts improve maintainability because changing a shared part only requires editing one file.
They support nested layouts where one layout can inherit another.
Layouts also support rendering dynamic data like username or notifications.
In summary, Layouts bring efficiency and consistency to MVC applications.

🔷 15. What is an HTML Helper? Name some types.

(10-line detailed answer)

HTML Helpers are methods in MVC used to generate HTML UI elements in Razor views.
They help create form controls like textboxes, dropdowns, checkboxes, and links.
Common helpers include Html.TextBox(), Html.Label(), Html.DropDownList(), and Html.ActionLink().
HTML helpers reduce typing and prevent errors by generating standard HTML automatically.
They support strongly typed views using Html.TextBoxFor() and Html.EditorFor().
Helpers make UI code cleaner and more maintainable.
Custom HTML helpers can be created if needed.
They improve readability and take advantage of C# IntelliSense.
HTML helpers ensure server-side validation and model binding integration.
Overall, HTML helpers simplify building dynamic and user-friendly Razor views.

🔷 16. What are Editor Templates and Display Templates?

(10-line detailed answer)

Editor Templates and Display Templates help in generating UI automatically based on model types.
They reduce repetitive HTML code by allowing MVC to auto-render fields using conventions.
Editor Templates are used to create editable form controls and are stored in Views/Shared/EditorTemplates.
Display Templates are used to display read-only data and are stored in Views/Shared/DisplayTemplates.
You can call them using Html.EditorFor() or Html.DisplayFor().
They support custom templates for complex objects like address, product details, or customer information.
MVC automatically selects the correct template based on data type (e.g., date, string, bool).
This creates cleaner and reusable UI code across the application.
Templates improve maintainability because changes to one template update all views.
Overall, templates help in writing less code while delivering consistent UI.

🔷 17. What is Model Binding in MVC?

(10-line detailed answer)

Model Binding is the process by which MVC converts HTTP request data into C# objects.
It extracts form values, query string values, and route parameters and maps them to method parameters.
You do not need to manually parse values from Request—MVC does this automatically.
Model binding works with simple types (string, int) and complex types (classes).
It helps action methods receive structured data directly as model objects.
Binding reduces boilerplate code and improves readability.
DataAnnotation attributes on model properties help validate bound data.
Model binding supports custom binders if you need special conversion logic.
It also handles collection types like lists or arrays.
Overall, model binding simplifies handling user input in MVC applications.

🔷 18. What are Data Annotations in MVC?

(10-line detailed answer)

Data Annotations are attributes used to apply validation rules and UI formatting to model properties.
They help enforce business rules like required fields, max length, and data types.
Examples include [Required], [StringLength], [Range], [EmailAddress], and [RegularExpression].
Using annotations keeps validation close to the model where it belongs.
They enable automatic server-side validation and unobtrusive client-side validation.
Data Annotations improve maintainability because rules are defined in one place.
Views automatically display validation messages using Html.ValidationMessageFor().
Custom validation attributes can also be created when complex rules are needed.
Annotations support display formatting using [Display(Name="")].
They ensure data quality and prevent invalid information from being processed.

🔷 19. What is Validation Summary?

(10-line detailed answer)

Validation Summary is a helper used to display all validation errors on a view at once.
It collects errors from model validation and shows them at the top of the form.
It helps users understand what all went wrong in a single glance.
@Html.ValidationSummary() is used in Razor views to render the summary.
It works with DataAnnotations and client-side validation.
Validation Summary improves usability by avoiding scattered error messages.
Developers can choose to show only model-level errors or include property-level errors too.
It prevents form submission until errors are fixed.
It contributes to better user experience in large forms with many fields.
Overall, Validation Summary ensures error communication is clear and organized.

🔷 20. What is Unobtrusive JavaScript in MVC?

(10-line detailed answer)

Unobtrusive JavaScript means clean separation of JavaScript from HTML.
Instead of writing inline scripts, MVC uses HTML5 attributes to trigger validation and Ajax.
It improves readability by keeping Razor views free from messy script code.
MVC’s client-side validation works using unobtrusive JavaScript conventions.
Scripts like jquery.validate.js and jquery.validate.unobtrusive.js enable this behavior.
HTML elements contain data-* attributes that the framework reads for validation rules.
This makes the UI lightweight and easier to maintain.
Unobtrusive JavaScript helps avoid duplication and script conflicts.
It also improves security by reducing direct script injection risks.
Overall, it makes MVC views cleaner, faster, and more maintainable.  


🔷 21. What are Filters in MVC?

(10-line detailed answer)

Filters allow you to run custom logic before or after an action method executes.
They handle cross-cutting concerns such as logging, authentication, caching, and error handling.
Filters improve maintainability by keeping repetitive logic out of controllers.
MVC includes four main types: Authorization, Action, Result, and Exception filters.
Authorization filters check whether the user is allowed to access the action.
Action filters run before and after the action method executes.
Result filters run before and after the view result is rendered.
Exception filters handle exceptions thrown by the action or view.
Filters can be applied globally, at controller level, or on specific actions.
They help create cleaner, more secure, and more structured MVC applications.

🔷 22. What is an Action Filter?

(10-line detailed answer)

Action Filters are special attributes that run logic before and after an action method.
Common built-in filters include [Authorize], [OutputCache], and [HandleError].
You can also create custom action filters by inheriting from ActionFilterAttribute.
Action filters help add reusable logic like logging, performance tracking, or authentication checks.
They reduce code duplication because you apply them once instead of copying logic into every action.
BeforeAction logic runs before the method executes; AfterAction logic runs afterward.
Action filters are powerful because they can modify input parameters or execution flow.
They support both synchronous and asynchronous methods.
They help enforce business rules and application-wide behaviors.
In summary, Action Filters bring modularity and flexibility to MVC controllers.

🔷 23. What is an Authorization Filter?

(10-line detailed answer)

Authorization filters control whether a user is allowed to access a controller or action.
The most common filter is [Authorize], which restricts access based on roles or users.
If a user is not authorized, the filter prevents the action method from executing.
Authorization filters run before action filters in the request pipeline.
They help secure sensitive parts of an application, such as admin sections.
Custom authorization filters can be created by implementing IAuthorizationFilter.
They can check permissions, tokens, roles, or custom security rules.
If authorization fails, they return an unauthorized or redirect response.
They protect applications by ensuring that only valid users can access resources.
Thus, authorization filters are essential for implementing access control in MVC.

🔷 24. What is a Result Filter?

(10-line detailed answer)

Result Filters run logic before and after the view result is executed.
They allow developers to modify the final output sent to the user.
For example, you can compress output, add headers, or customize response formatting.
Result filters run after the action method has returned its ActionResult.
They are useful for logging view rendering time and performance analysis.
To create a custom result filter, you implement IResultFilter or derive from ActionFilterAttribute.
They do not affect action execution, only the rendering stage.
Result filters also help in managing caching or adding audit logs.
They can be applied globally, to controllers, or to specific actions.
Overall, result filters enhance the final response without touching action logic.

🔷 25. What is an Exception Filter?

(10-line detailed answer)

Exception Filters handle errors thrown by controllers or action methods.
They provide a centralized way to log exceptions or show custom error pages.
The [HandleError] attribute is a common built-in exception filter.
Exception filters run when an unhandled exception occurs during action or result execution.
They help prevent exposing sensitive system information to users.
Custom exception filters can be created by implementing IExceptionFilter.
They can redirect users to friendly error pages or capture exceptions for monitoring tools.
Exception filters improve reliability and stability of MVC applications.
They make exception handling cleaner by reducing try-catch blocks in controllers.
Exception filters are essential for building secure and user-friendly applications.

🔷 26. How can you implement Custom Filters in MVC?

(10-line detailed answer)

Custom filters are created by inheriting from ActionFilterAttribute or implementing filter interfaces.
You override methods like OnActionExecuting(), OnActionExecuted(), OnResultExecuting(), etc.
Custom filters allow you to add logging, validation, performance monitoring, or audit tracking.
They can be applied using attributes on actions or controllers.
You can also register them globally in FilterConfig.cs.
Custom authorization filters are built by implementing IAuthorizationFilter.
Exception filters are built by implementing IExceptionFilter.
Filters provide flexibility because you can reuse them across multiple controllers.
They help remove repetitive code from controllers and actions.
Custom filters improve modularity, readability, and testability of MVC applications.

🔷 27. What is CSRF? How to prevent it in MVC?

(10-line detailed answer)

CSRF (Cross-Site Request Forgery) is an attack where a malicious website tricks a user into performing actions unknowingly.
It targets authenticated sessions and forces users to perform unwanted operations.
In MVC, CSRF protection is implemented using Anti-Forgery Tokens.
The view includes the token using @Html.AntiForgeryToken().
The controller action method must have [ValidateAntiForgeryToken] to validate it.
If the token does not match, MVC blocks the request.
Anti-Forgery tokens ensure that the request comes from the legitimate user and not from a third party.
They protect sensitive actions like form submissions, payments, or data changes.
CSRF prevention is enabled by default in MVC applications.
It is one of the most important security features in web applications.

🔷 28. What is Authentication vs Authorization?

(10-line detailed answer)

Authentication verifies who the user is—like login using username/password.
Authorization verifies what the user is allowed to do, such as access admin pages.
In MVC, authentication happens first, followed by authorization.
Authentication identifies the user; authorization assigns permissions or roles.
MVC supports multiple authentication types: Forms, Windows, JWT, OAuth, etc.
Authorization uses roles or policies to restrict access via [Authorize].
A user can be authenticated but still not authorized for certain pages.
Both are essential for application security.
Authentication ensures identity; authorization ensures access rights.
Together, they protect the application from unauthorized usage.

🔷 29. How does MVC handle Session and Cookies?

(10-line detailed answer)

Session stores user data on the server and persists across multiple requests.
In MVC, session values are set using Session["key"] = value.
Cookies store small pieces of data in the user's browser.
Cookies are created using Response.Cookies["name"].Value = "data".
Session is more secure but uses server memory; cookies are lightweight but less secure.
Session is used for user-specific data like login information or shopping carts.
Cookies are used for preferences, tracking, or "Remember Me" functionality.
MVC supports TempData, which internally uses Session for short-lived data.
Both Session and Cookies help maintain state in stateless HTTP.
The choice between them depends on security, size, and persistence requirements.

🔷 30. What is AntiForgeryToken in MVC?

@Html.AntiForgeryToken() generates a hidden token to protect forms from CSRF attacks.
This token is unique for each user and each request.
When the form is submitted, MVC verifies this token using [ValidateAntiForgeryToken].
If the token is missing or invalid, the request is rejected.
Anti-forgery tokens ensure that the request is coming from a trusted source.
They protect sensitive operations like login, data updates, and financial transactions.
MVC automatically maintains security by validating these tokens.
They are easy to implement and highly effective in security.
Anti-forgery tokens work with both Ajax and normal form submissions.
In summary, they provide robust CSRF protection for MVC applications.


🔷 31. What is Attribute Routing? How is it enabled?

(10-line detailed answer)

Attribute Routing allows you to define routes directly on controller actions using attributes.
Instead of defining all routes in RouteConfig, you place [Route("path")] above actions.
It improves readability because the route definition stays close to the controller action.
Attribute routing supports complex URL patterns, optional parameters, and constraints.
It is enabled by adding routes.MapMvcAttributeRoutes(); in RouteConfig.cs.
You can define routes like [Route("product/details/{id}")].
It works well for RESTful URLs and APIs because routes become predictable.
Attribute routing can override conventional routing rules.
It allows route grouping using [RoutePrefix] on the controller.
Overall, attribute routing gives precise control over how URLs map to actions.

🔷 32. What is Convention-Based Routing?

(10-line detailed answer)

Convention-based routing means defining routes in a centralized configuration file (RouteConfig.cs).
The default route looks like: {controller}/{action}/{id}.
MVC uses this pattern to automatically match incoming URLs to controllers and actions.
It avoids defining individual routes for each action manually.
Convention routing is easy to maintain for small and medium applications.
However, for complex URL patterns, attribute routing becomes easier.
Convention routing also supports default values and optional parameters.
Routes must be added in order because MVC uses the first matching rule.
You can define custom routes to override the default pattern.
It is the traditional routing method used since MVC 1.0.

🔷 33. What are Areas in MVC?

(10-line detailed answer)

Areas allow you to divide a large MVC application into multiple sections or modules.
Each Area contains its own Controllers, Views, and Routes.
Common Areas include Admin, User, Billing, Reports, etc.
They help organize large projects by grouping related functionality.
Each Area has its own AreaRegistration.cs file to define routes.
Areas prevent naming conflicts by isolating controllers with the same name.
They also enhance maintainability and allow multiple teams to work independently.
Views in Areas have their own folder structure like /Areas/Admin/Views/.
Routing automatically identifies the area during request processing.
Overall, Areas help in modularizing and scaling big enterprise MVC applications.

🔷 34. How to register a route in MVC?

(10-line detailed answer)

Routes are registered in the RouteConfig.cs file inside the App_Start folder.
The most common method is routes.MapRoute(name, url, defaults).
Example:

routes.MapRoute(
    name: "Default",
    url: "{controller}/{action}/{id}",
    defaults: new { controller = "Home", action = "Index", id = UrlParameter.Optional }
);


Route registration happens during application start in Global.asax.
MVC checks routes in the order they are registered.
Custom routes must be placed before the default route.
Route registration helps define how URLs behave and what actions they map to.
It is essential for controlling navigation and URL structure.

🔷 35. What is RouteConfig file?

(10-line detailed answer)

RouteConfig.cs is the file where all convention-based routes are defined.
It lives in the App_Start folder of an MVC application.
The method RegisterRoutes(RouteCollection routes) contains routes.MapRoute() calls.
The file is executed at application startup using Global.asax.
It configures how URLs map to controllers and actions.
You can define default routes, custom routes, optional parameters, and constraints.
Attribute routing can also be enabled inside this file.
The order of routes in RouteConfig controls routing behavior.
It is essential for building clean, SEO-friendly URLs.

They make the view code more readable by avoiding dynamic objects.
In summary, strongly typed views ensure safer and cleaner UI coding.
🔷 36. What is Bundling in MVC?

(10-line detailed answer)

Bundling is an MVC feature that combines multiple CSS or JavaScript files into a single bundle.
This reduces the number of HTTP requests sent by the client browser.
Bundling improves page performance and loading speed, especially for large applications.
You can create bundles in BundleConfig.cs using ScriptBundle or StyleBundle.
Example:

bundles.Add(new ScriptBundle("~/bundles/js").Include("~/Scripts/file1.js", "~/Scripts/file2.js"));


MVC automatically handles bundle versioning and caching.
Bundles can be minified to further reduce file size.
During development, files remain separate for easy debugging.
Overall, bundling is a powerful optimization technique in ASP.NET MVC.

🔷 37. What is Minification?

(10-line detailed answer)

Minification removes unnecessary characters from CSS and JavaScript files.
This includes removing spaces, comments, tabs, and extra line breaks.
Minified files load faster because their size is much smaller.
Minification happens automatically when bundling is enabled in MVC.
It reduces bandwidth usage and improves page responsiveness.
Example: script.js becomes script.min.js with compressed content.
Browsers receive optimized files for production use.
In development mode, MVC does not minify files to allow easier debugging.
Minification also decreases page rendering time.
Together with bundling, it greatly enhances application performance.

🔷 38. Difference between RouteConfig and BundleConfig?

(10-line detailed answer)

RouteConfig manages how URLs map to controllers and actions in the MVC application.
It defines URL patterns, default routes, custom routes, and route constraints.
RouteConfig is responsible for the request navigation flow.
BundleConfig, on the other hand, manages script and style optimization.
It bundles and minifies CSS and JS files to improve performance.
BundleConfig does not control navigation; it controls front-end asset loading.
RouteConfig is executed to match routes, while BundleConfig is executed to load static assets.
Both files are placed under the App_Start folder.
One deals with server-side routing; the other deals with client-side optimization.
Together they help in building fast, structured MVC applications.

🔷 39. What is Url.Action() used for?

(10-line detailed answer)

Url.Action() generates a URL for a specific controller action.
It helps in creating dynamic links that automatically follow routing rules.
Example: Url.Action("Details", "Product", new { id = 5 }).
It is often used in redirects, script calls, and AJAX requests.
Url.Action() ensures URLs are created using the correct route patterns.
It avoids hardcoding URLs, making the code cleaner and safer.
If routes change, Url.Action() automatically updates the generated URL.
It supports passing parameters to action methods.
Commonly used inside Razor views and scripts.
Overall, it helps in building flexible and route-friendly navigation.

🔷 40. What is Html.ActionLink()?

(10-line detailed answer)

Html.ActionLink() is an HTML helper that generates an anchor (<a>) tag.
It creates a clickable link that points to a specific action method.
Example:

@Html.ActionLink("View Product", "Details", "Product", new { id = 5 }, null)


It ensures the link is built according to routing rules.
Avoids writing raw <a href=""> links manually.
Helps prevent broken links if route patterns change.
Supports passing parameters and HTML attributes.
Commonly used in menus, navigation bars, and lists.
It simplifies linking between pages in MVC applications. 


🔷 41. What is Dependency Injection (DI) in MVC?

(10-line detailed answer)

Dependency Injection is a design pattern that helps remove tight coupling between classes.
Instead of a class creating its own dependencies, they are injected from outside.
This makes the code more flexible, testable, and easier to maintain.
In MVC, DI is commonly used to inject services, repositories, and DbContext into controllers.
It improves unit testing because fake or mock objects can be injected easily.
ASP.NET MVC supports DI through third-party containers like Unity, Autofac, Ninject, etc.
You configure these containers to resolve dependencies automatically.
ASP.NET Core MVC has DI built-in, and services can be added using AddScoped, AddTransient, or AddSingleton.
DI helps in following SOLID principles, especially the Dependency Inversion Principle.
Overall, DI simplifies object creation, improves structure, and makes applications more scalable.

🔷 42. What are View Components (in MVC Core)?

(10-line detailed answer)

View Components are reusable UI building blocks similar to Partial Views but more powerful.
They allow executing server-side logic and returning HTML output.
View Components do not use controllers; instead, they contain their own class and view.
They are ideal for components like menus, dashboards, sidebars, and notifications.
A View Component consists of a class (ending with ViewComponent) and a view file.
They are invoked using @Component.Invoke("Name") or @await Component.InvokeAsync("Name").
They support passing parameters and retrieving data from services or databases.
Unlike Partial Views, they follow a full MVC mini-pattern internally.
They improve separation of concerns by moving UI logic out of large views.
View Components help create modular, maintainable, and testable UIs in MVC Core.

🔷 43. What is TempData? When do you use it?

(10-line detailed answer)

TempData is used to store data that is needed only for one request, especially after a redirect.
It uses Session internally to store key-value pairs.
Common use cases include success messages, error messages, or confirmation messages after POST.
Example: TempData["Message"] = "Record Added Successfully";.
TempData persists only until it is read, after which it is removed automatically.
It is ideal for Post/Redirect/Get (PRG) patterns.
TempData works across multiple controllers because it uses session storage.
Unlike ViewBag and ViewData, TempData survives redirects.
It should not be used for long-term data because it is cleared quickly.
TempData helps in short-lived data sharing between actions.

🔷 44. What is the difference between Server-side and Client-side Validation?

(10-line detailed answer)

Server-side validation happens on the server after the form is submitted.
It is more secure because validation rules run on the server where users cannot tamper with them.
However, it requires a round-trip to the server, making it slower for the user.
Client-side validation happens in the browser before sending data to the server.
It uses JavaScript and is faster, giving instant feedback to users.
MVC supports client-side validation using jQuery Validation and Unobtrusive JavaScript.
Both validation types are often used together for best security and user experience.
Data Annotations trigger both client-side and server-side validations automatically.
Client-side validation improves usability; server-side validation ensures strong security.
Using both ensures safe and user-friendly form handling.

🔷 45. What is Scaffolding in MVC?

(10-line detailed answer)

Scaffolding is an automatic code-generation feature in MVC.
It quickly creates controllers, views, and CRUD operations based on your model.
This saves a lot of development time for standard database-driven screens.
You can scaffold a controller with actions and views using Visual Studio tools.
MVC generates standard Create, Read, Update, and Delete views automatically.
It is extremely useful in the initial phase of the project or rapid prototyping.
Scaffolding reduces repetitive manual coding and avoids common mistakes.
You can customize the generated code later as per business requirements.
Scaffolding integrates with Entity Framework for database operations.
Overall, it speeds up development and ensures consistent code structure.


🔷 46. What are Action Selectors (HttpGet, HttpPost) in MVC?

(10-line detailed answer)

Action selectors are attributes that control which action method executes based on the HTTP request type.
[HttpGet] handles GET requests where data is requested from the server.
[HttpPost] handles POST requests where data is submitted to the server.
You can also use [HttpPut], [HttpDelete], and [HttpPatch] in Web APIs.
Action selectors help create method overloading for the same action name.
Example: One "Create" method for GET to show form, another for POST to submit form.
They improve clarity by clearly separating data retrieval and submission logic.
Action selectors also enhance security by restricting how actions can be called.
Without them, MVC may confuse which action should run.
Overall, action selectors help build well-structured and secure controller actions.

🔷 47. What is the difference between RedirectToAction() and RedirectToRoute()?

(10-line detailed answer)

RedirectToAction() redirects to a specific action method and controller.
It is commonly used to redirect after form submissions or CRUD operations.
Its parameters are controller name, action name, and route values.
RedirectToRoute() redirects based on route configuration rather than controller/action.
You specify the route name instead of action and controller.
RedirectToAction() is simpler when redirecting inside the same controller or known action.
RedirectToRoute() is more flexible when custom routing rules exist.
Both return a RedirectToRouteResult.
Both send a new HTTP request, meaning no data persists unless stored in TempData.
In summary: use RedirectToAction for controllers/actions and RedirectToRoute for route names.

🔷 48. What is JSON Binding in MVC?

(10-line detailed answer)

JSON binding allows MVC to convert JSON data from client-side into C# objects automatically.
It is commonly used with AJAX calls, JavaScript fetch API, or jQuery.
The JSON data must match the property names of the model for successful binding.
Model binding converts JSON into complex objects like lists or nested classes.
The controller action receives the data as parameters or model objects.
Anti-forgery validation may be required for secure JSON POST requests.
MVC supports JSON responses using JsonResult or return Json(data).
In ASP.NET Core, FromBody attribute helps bind JSON to action parameters.
JSON binding improves performance by avoiding full-page posts.
It is essential for building modern, dynamic, and interactive MVC applications.

🔷 49. How do you upload files in MVC?

(10-line detailed answer)

File uploads in MVC use HttpPostedFileBase (MVC 5) or IFormFile (MVC Core).
The form must include enctype="multipart/form-data".
The controller receives uploaded files through method parameters.
You can save the file using SaveAs() in MVC 5 or using file streams in Core.
Validation should include checking file size, type, and security.
Files can be saved in local folders, cloud storage, or databases.
Multiple file uploads are also supported using collections.
Error handling is important to avoid security issues.
MVC Core also supports asynchronous file upload APIs.
File uploading is a common requirement for profile images, documents, or attachments.

🔷 50. What is the Repository Pattern? Why is it used in MVC?

(10-line detailed answer)

The Repository Pattern separates data access logic from business logic.
It provides a clean abstraction over database operations.
Controllers interact with repositories instead of directly calling Entity Framework.
This makes the code more testable because repositories can be mocked.
It follows the Single Responsibility Principle from SOLID.
Repositories contain methods like Add, Update, Delete, and GetAll.
They help reduce duplicate data access code across controllers.
Using repositories improves maintainability and flexibility.
Changes to the database layer do not affect controllers.
Overall, the Repository Pattern improves code quality, structure, and scalability in MVC.
