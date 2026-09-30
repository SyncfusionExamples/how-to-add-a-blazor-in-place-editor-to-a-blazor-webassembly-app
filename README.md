# How to Add a Blazor In-Place Editor to a Blazor WebAssembly App

## Overview

This sample demonstrates how to integrate the Syncfusion [Blazor In-Place Editor](https://www.syncfusion.com/blazor-components/blazor-in-place-editor) into a Blazor WebAssembly application. The project shows how users can edit values directly within the page without navigating to separate forms, creating a more streamlined editing experience.

The sample illustrates different editor configurations, including text-based editing, date selection, and value selection scenarios. It also demonstrates editor behavior customization, editing modes, action handling, and UI styling adjustments that are commonly required in real-world applications.

## Key Features

- Uses the Syncfusion Blazor In-Place Editor (`SfInPlaceEditor`) component for inline editing of user profile information.
- Demonstrates two-way data binding using the `@bind-Value` property on the In-Place Editor component.
- Integrates a Syncfusion TextBox (`SfTextBox`) as a custom editor through the `EditorComponent` template for editing a user name.
- Integrates a Syncfusion DatePicker (`SfDatePicker`) as a custom editor through the `EditorComponent` template for selecting a date of birth.
- Configures the In-Place Editor with `TValue="string"` and `TValue="DateTime?"` to support different data types.
- Demonstrates the use of the `Type="InputType.Date"` property for date-based editing scenarios.
- Initializes editable values using component-level properties (`TextValue` and `DateValue`) and updates them automatically through two-way binding.
- Includes a client-side weather forecast page that retrieves data from a server-side API using `HttpClient.GetFromJsonAsync<T>()`.
- Demonstrates asynchronous data loading in the `OnInitializedAsync()` lifecycle method.
- Uses an ASP.NET Core Web API controller (`WeatherForecastController`) to generate and return forecast data to the Blazor WebAssembly client.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download this repository.
2. Open the solution file:

   `AddingInplaceEditor.sln`

3. Restore all NuGet packages.
4. Ensure the Client project is configured as the startup project if required by your environment.
5. Build the solution.
6. Run the application using `Ctrl+F5`.

**Visual Studio Code**

1. Open the repository folder.
2. Navigate to the project directory that contains the Blazor WebAssembly application.
3. Restore packages:

```bash
dotnet restore
```

4. Run the application:

```bash
dotnet run
```

5. Open the URL displayed in the terminal after the application starts.

## Project Structure

`Client/Pages/Index.razor` - Main sample page demonstrating Syncfusion `SfInPlaceEditor` with embedded `SfTextBox` and `SfDatePicker` editors for inline editing.

`Client/Pages/FetchData.razor` - Weather forecast page that consumes data from the server-side API using `HttpClient` and displays the results in a table.

`Server/Controllers/WeatherForecastController.cs` - ASP.NET Core Web API controller that generates and returns weather forecast data.

`Shared/WeatherForecast.cs` - Shared model containing the weather forecast data structure used by both the Client and Server projects.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- For feature documentation, refer to the Syncfusion Blazor In-Place Editor documentation: https://blazor.syncfusion.com/documentation/in-place-editor/getting-started

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.