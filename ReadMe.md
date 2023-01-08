# Integrate Blazor in ASP.net Core MVC app

- add nuget package ```Microsoft.AspNetCore.Components``` 

- add blazor service in DI container using AddServerSideBlazor property i.e.
    ``` builder.services.AddServerSideBlazor(); ```

- add blazor hub endpoint  i.e. 
```e.MapBlazorHub(); ```    

- In layout file add blazor servide side script reference ```<script src="_framework/blazor.server.js"></script>```

- In blazor component add reference at top ``` @using Microsoft.AspNetCore.Components.Web ```

- In cshtml add component using code ```@(await Html.RenderComponentAsync<HybridBlazor.Views.Shared.Components.DataViewComponent>(RenderMode.ServerPrerendered,new {data="parmeter val1",style="param val2"}))```
wrap above code in a div

