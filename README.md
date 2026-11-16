# Timesheet Management Portal

Timesheet Management Portal is a planned web application for tracking weekly
organization and client timesheet submissions. It is intended to give project
managers a clear view of submitted timesheets, missing files, and reasons that
a timesheet was not submitted.

The repository currently contains an early browser-based prototype. The
production application will be developed incrementally from the agreed React,
.NET, and PostgreSQL stack.

## Planned features

- Create projects and add, rename, or manage teammates.
- Track organization and client timesheets by week.
- Attach a timesheet file or record a reason when it was not submitted.
- View pending, submitted, and reason-recorded statuses on a dashboard.
- Choose weeks with a calendar and preview supported image or PDF attachments.
- Switch between light and dark themes.

## Planned technology

- **Frontend:** React and TypeScript
- **API:** ASP.NET Core Web API
- **Database:** PostgreSQL, accessed through Entity Framework Core and Npgsql
- **Attachments:** Store file content in PostgreSQL `bytea` columns in a
  separate attachment table. PostgreSQL manages internal chunking for large
  values; the application will not split files into its own chunk records.

## Development status

This project is in its planning and prototype stage. Setup instructions,
database schema, and deployment guidance will be added as the production
application is built.

## Security considerations

Timesheet files and submission records are intended for authorized team members
only. Before team-wide use, the production application will need sign-in,
project-level access controls, upload size and file-type validation, and
protected attachment access. Database backups will also contain the stored
attachment content and should be protected accordingly.
