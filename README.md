# Black Wedding Theme

A modern black-and-white wedding website for Melvin and Trisha, built with Blazor and mirrored as a static GitHub Pages site.

## Features

- Responsive luxury editorial design for desktop, tablet, and mobile
- Animated hero, section reveals, and responsive Story layout
- Wedding details and gallery with an image popup
- StaticForms RSVP flow with loading, validation, error, and success states
- Matching Blazor and static `docs/` versions

## Project structure

- `BlackWeddingTheme/` - .NET 10 Blazor application
- `BlackWeddingTheme/Components/Pages/Home.razor` - homepage markup and gallery state
- `BlackWeddingTheme/wwwroot/app.css` - primary Blazor styling
- `BlackWeddingTheme/wwwroot/gallery.js` - Blazor animation, gallery, and RSVP JavaScript
- `docs/` - static GitHub Pages-compatible version
- `docs/assets/js/site.js` - static animation, gallery, and RSVP behavior

## Run locally

Requires the .NET 10 SDK.

```powershell
dotnet run --project BlackWeddingTheme\BlackWeddingTheme.csproj
```

Default launch URLs:

- `https://localhost:7038`
- `http://localhost:5109`

## Build

```powershell
dotnet build BlackWeddingTheme.slnx -c Release
```

## Static site

The `docs/` folder uses relative asset paths and can be published through GitHub Pages. Keep its HTML, CSS, images, and JavaScript aligned with the Blazor implementation.

## StaticForms configuration

The committed RSVP configuration intentionally uses this placeholder:

```text
__STATIC_FORMS_API_KEY__
```

Create a GitHub repository secret named `STATIC_FORMS_API_KEY` and inject it only into a temporary deployment artifact. Never commit the real API key.