# CURSO: APRENDE BLAZOR

# LECCIÓN 25: Pasar Parámetros en una Ruta

1. Abrir la aplicación con Visual Studio 2022 o VSCode

2. Pasar un sólo parámetro en una ruta. Modificamos el componente Home.razor e incluimos el siguiente código

```razor
@page "/"

@page "/home/{id}"

<PageTitle>Home</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.

<p>Product ID: @Id</p>

@code {
    [Parameter]
    public string? Id { get; set; }
}
```

3. Pasar múltiples parámetros en una ruta

```razor
@page "/"

@page "/home/{id1}"

@page "/home/{id1}/{id2}"

<PageTitle>Home</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.

<p>Product ID1: @Id1</p>

<p>Product ID2: @Id2</p>

@code {
    [Parameter]
    public string? Id1 { get; set; }

    [Parameter]
    public string? Id2 { get; set; }
}
```

4. Pasar un parámetro opcional en una ruta

```razor
@page "/"

@page "/home/{userId?}"

<PageTitle>Home</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.

<p>User ID: @UserId</p>

@code {
    [Parameter]
    public string UserId { get; set; } = "Guest";
}
```
