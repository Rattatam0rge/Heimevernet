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
