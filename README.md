# Heroku Suave / .NET Core Buildpack

This is a [Heroku buildpack](https://devcenter.heroku.com/articles/buildpacks) for [Suave](https://suave.io/) and [dotnet core](https://github.com/dotnet/core).

## Usage

The buildpack will search through the repository's folders to locate a `Program.fs` file. If found, the `.fsproj` in the containing folder will be used in the `dotnet publish <project>.fsproj` command.

If repository contains **multiple** Web Applications (multiple `Program.fs`), `PROJECT_FILE` and `PROJECT_NAME` environment variables allow to choose project for publishing.

```
heroku buildpacks:set https://github.com/lxmedina/dotnetcore-buildpack
```

## Acknowledgement

This project is basically [@jincod's buildpack](https://github.com/jincod/dotnetcore-buildpack) merged with [@ademar's modifications](https://github.com/ademar/dotnetcore-buildpack). Thanks to both of you!
