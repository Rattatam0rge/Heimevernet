# FeedbackMap – Kriseberedskap, ressurs- og behovsportal

ASP.NET Core MVC (.NET 10) + MariaDB, kjørt med Docker Compose.

## Kjøre

1. Kopier `.env.example` til `.env` og sett passord.
2. `docker compose up --build`
3. Åpne http://localhost:8080

Databasemigrasjoner kjøres automatisk ved oppstart (`RunMigrationsOnStartup=true`).

## Utvikling

- Ny migrasjon: `cd FeedbackMap` og `dotnet ef migrations add <Navn>`
- Roller: `PublicActor` og `ResourceProvider` opprettes ved oppstart.


mkdir FeedbackMap
cd FeedbackMap
git init
dotnet new sln -n FeedbackMap
dotnet new mvc -n FeedbackMap -o FeedbackMap
dotnet sln add FeedbackMap/FeedbackMap.csproj
dotnet new gitignore
Add-Content .gitignore "`n.env"


cd FeedbackMap
dotnet add package Microsoft.AspNetCore.Identity.EntityFrameworkCore --version "10.0."
dotnet add package Microsoft.EntityFrameworkCore.Design --version "10.0."
dotnet add package Microting.EntityFrameworkCore.MySql --version "10.0.*"
dotnet tool install --global dotnet-ef
cd ..


## Starte Docker
docker compose up --build
ELLER
Starte rett fra Docker om du har Containeren fra før
