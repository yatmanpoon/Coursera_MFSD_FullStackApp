# Microsoft Copilot Full-Stack Integration Demo

A small full-stack demo that pairs a Blazor WebAssembly client with an ASP.NET Core API.

## Overview

InventoryHub demonstrates how to:
- build a browser-based interface with Blazor WebAssembly
- call a separate ASP.NET Core API from the client
- display product and category data returned as JSON
- handle loading, timeout, and request-error states in the client

The API returns sample data from memory. The project does not use a database or persist changes.

## Tech Stack

- C#
- .NET 10
- Blazor WebAssembly
- ASP.NET Core minimal API
- Bootstrap

## Project Structure

- `InventoryHub/ClientApp/` - Blazor WebAssembly client, pages, layout, and static assets
- `InventoryHub/ServerApp/` - ASP.NET Core API, including the `/api/productlist` endpoint
- `InventoryHub/FullStackSolution.slnx` - solution containing the client and server projects

## How to Run

1. Install the [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0).
2. From the repository root, open two terminal windows.
3. In the first terminal, start the API:

   ```powershell
   dotnet run --project InventoryHub/ServerApp/ServerApp.csproj
   ```

   The API's HTTP launch profile listens on `http://localhost:5041`.

4. In the second terminal, start the client:

   ```powershell
   dotnet run --project InventoryHub/ClientApp/ClientApp.csproj
   ```

   The client’s HTTP launch profile listens on `http://localhost:5299`.

5. Open `http://localhost:5299/fetchproducts` to view the product list.

To build both projects from the repository root, run:

```powershell
dotnet build InventoryHub/FullStackSolution.slnx
```

## Course

This is the final assignment for the Coursera course: Microsoft Full-Stack Developer Professional Certificate - Full-Stack Integration

## License

This project is for educational purposes.
