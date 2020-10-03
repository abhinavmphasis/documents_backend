Media queries
hamburger menu
code with harry after 1:48 hrs
flex-direction
smooth scroll
bootstrap
I.shekhar26@gmail.com
talent next asp .net procedure
0-------------------------core-------------
difference between map and mapget 
map will handle all the request and mapget will handle only the input request

kesteral server
there are two methods in the startup file -- configure() and configureservices()
the later one is used to define the dependencies which we are going to use in our application

the configure method is used to define the http service middleware
https://www.youtube.com/watch?v=gxu1fsHGvMo&list=PLaFzfwmPR7_LTXu0Vz9Zz_Y0OMMC7ArHZ&index=12&ab_channel=WebGentle

if the name of the view is equal to the name of the action method,
return (view model  obj)

if the name of the view is not equal to the name of the action method 
return (view name, view model object)

ViewEngine is a piece of code which is used to render server side code, works with views, set/get the path for the default view location, razor is a view engine, write a c# logics on 
view page. everything starts with @

@expression
@DateTime.Now
@Yourc#variable

Static files
All static files must be placed inside the wwwroot folder
Its also known as the content root folder
It must be present at the root level

In order to use the static files we need to use the middleware in the startup.cs file

app.UseStaticFiles(new StaticFileOptions() {

                FileProvider = new PhysicalFileProvider(Path.Combine(Directory.GetCurrentDirectory() + "MyStaticFiles")),
                RequestPath = "/MyStaticFiles"
            }) ;

Libman.json

Razor files engine compiles only two times- it compiles when we build our solution and when we publish our solution
Install a new package to the solution
Microsoft.AspNetCore.Mvc.Razor.RuntimeCompilation

make some changes in the startup file - add in the 
        public void ConfigureServices(IServiceCollection services)


services.AddRazorePages().AddRazorRuntimeCompilation();

there is a 	condition in which this needs to run as it impacts the performance of the application
so that is only the development environment
--------------------------------------------------------------------------------
Layout:- RenderBody() method is used inside the layout file to provide space for the other view

we can have only one RenderBody() method inside the one layout file 		

Benifits:
less code
centralized code for the static files
No duplicate code
Easy to update
Good architecture
-----
Adding navigation bar

we will use bootstrap
-------------------------------------------
Display Model list data on the view in Asp.Net Core
@model-- when we are getting the data in the model and we need to display it on the view
----------------------------------
Render Section

RenderSection is a space with the a specific name and is used in the _Layout file
It tells the application that some other code is coming here

Section
Section is used on views
create a section we use @section directive
Each section has a unique name and we will write inside the section block that will replace the RenderSection defined in _Layout file with the same name

Situation

Header
CSS
Body
js
RenderSection
Footer

there is section which can be placed anywhere in the cshtml file and then is rendered in the layout page of the application and is placed inside the @render("section",. required: false)
and is placed at the suitable position of the UI
---------------------------------------------------------------
View start is the view which gets triggered before the view file

view imports-- common directives in this are 
@addTagHelpers
@removeTagHelpers
@tagHelperPrefix
@using
@model
@inherits
@inject
the main purpose of the view imports is to have all the directives imported at the common location
			